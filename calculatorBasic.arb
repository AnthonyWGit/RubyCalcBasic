class Calculator
    def takeUserInput()
        @userInput = gets.chomp #take user input |chomp delete the /n creater by gets 
        #take chomp of and you will never see "string cannot be empty" ! 
    end

    def errorMsg()
        @errorMsg = "Only numbers are allowed with  basic arithmetic operations"
    end

    def detectOperation()
        if @userInput.empty? # this check has to be done before elval else it won't be detected and the msg string empty won't be displayed
            puts "String cannot be empty"
        else
            if @userInput == "e"
                puts "Do you want the value of mathematical e const ? (Euler's number)"
                puts "[yes] or [no] ?" 

                @answer = gets.chomp
                if (@answer == "yes")
                    puts Math::E
                else
                    puts "Terminating programm"
                    exit
                end
            else
                begin #we use begin like a try catch in php 
                @result = eval(@userInput) #the string the user writes is interpreted as ruby code so we can direcy use to do calculations 
                #that means operation like srqt should do
                puts @result
                rescue Exception => e
                    puts "This is not an arithmeric operation  "
                end #In ruby if else conditionals must be terminated by end                      
            end
        end
    end
end

calc = Calculator.new
calc.takeUserInput()
calc.detectOperation()
