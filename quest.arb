require 'date'

def difference(arr )
    # Превращаю время в минуты
    (0...arr.length).each do |i|
        arr[i] = DateTime.parse(arr[i]).strftime("%H:%M")

        if arr[i][0] == "0"
            hour = arr[i][1].to_i
        else
            hour = (arr[i][0] + arr[i][1]).to_i
        end
        hour = hour * 60

        if arr[i][3] == "0"
            minute = arr[i][1].to_i
        else
            minute = (arr[i][3] + arr[i][4]).to_i
        end
        

        my_times = hour + minute
        arr[i] = my_times
    end

    # Создаю переменную с разницей максимального и минимального, далее пробегаюсь по массиву и вычитаю значения
    min = arr.max - arr.min
    
    (0...arr.length).each do |i|
        (0...arr.length).each do |j|
          if i == j && arr[i] - arr[j] == 0
            next
          else
            score = arr[i] - arr[j]
            if score < -1
                score *= -1
            end
          end
          min = score if score < min
        end
    end

    return min
end
arr = ["2:10pm", "1:30pm","10:30am", "5:20pm"]


print difference(arr)