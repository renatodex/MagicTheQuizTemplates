<?php
header('Access-Control-Allow-Origin: *');
?>

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html>
    <head>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
        <title>Magic the Experience Quiz - Qual planinalta você seria?</title>
    </head>

    <body>	
        <div id="site">
            <div class="logo">Magic the Experience</div>
            <h1>Qual planinalta você seria?</h1>
            <h2>Responda as perguntas e descubra qual Planinauta você seria na vida real.</h2>


            <div class="questions">
                Carregando Quiz...
            </div>


            <input type="button" name="enviar" class="send_button" value="Enviar Respostas" />

            <p class="progress">1 de 10 perguntas</p>            
            <hr />
        </div>

        <script src="jquery.js" type="text/javascript"></script>
        <script type="text/javascript">
            var Constants = {
                QUESTIONS_URL : 'http://localhost:5454/questions',
                QUIZ_URL : 'http://localhost:5454/plainswalker'
            }
            
            var HttpJSON = {
                get_request : function(url, call_ok, call_nok) {
                    $.ajax({
                        url: url,
                        method: 'GET',
                        dataType: 'jsonp',
                        timeout: 5000,
                        success: call_ok,
                        error : call_nok
                    });
                }
            }
            
            
            var UIDFactory = {
                create : function (){
                    var idstr=String.fromCharCode(Math.floor((Math.random()*25)+65));
                    do {                
                        var ascicode=Math.floor((Math.random()*42)+48);
                        if (ascicode<58 || ascicode>64){
                            idstr+=String.fromCharCode(ascicode);    
                        }                
                    } while (idstr.length<32);

                    return (idstr);
                }
            }       
            
            var AnswerUI = {
                create : function(target, text, uid, value) {
                    var question_label = $("<label />").text(text);
                    var question_label_input = $("<input />").attr({name: uid, type: 'radio', value : value})
                    target.append(question_label.prepend(question_label_input));                 
                
                    return this;
                }
            }
        
            var QuestionUI = {
                question_with_p : '',
                unique_id : '',
            
                create : function(question_text) {
                    this.unique_id = UIDFactory.create();
                    var question = $("<div />").addClass('question');
                    var question_p = $("<p />").text(question_text);
                    this.question_with_p = question.append(question_p);
                
                    return this;
                },
            
                add : function(text, value) {
                    AnswerUI.create(this.question_with_p, text, this.unique_id, value);
                    return;
                },
            
                appendTo : function(parent) {
                    $(parent).append(this.question_with_p);
                }
            }
            
            var QuizWS = {
                getQuestions : function(success_callback, error_callback) {
                    success_callback = success_callback || function() {};
                    error_callback = error_callback || function() {};
                    
                    $.ajax({
                        url: Constants.QUESTIONS_URL,
                        method: 'GET',
                        dataType: 'jsonp',
                        success: success_callback,
                        error : error_callback
                    });
                }
            }
            
            var ValidateUI = {
                checkIfAnswerIsFilled : function() {
                    if($('input[type=radio]:checked').length < 5) {
                        return false;
                    }
                    return true;
                }
            }
            
            var SubmitUI = {
                getParams : function() {
                    var params = '';
                    var radio_value = 0;
                    $('input[type=radio]:checked').each(function() {
                        radio_value = $(this).val();
                        params += ['&answers[]=', radio_value].join('');
                    });
                    var final_params = params.substring(1,params.length);

                    return final_params;                    
                },
                
                sendAction : function() {
                    
                    if(ValidateUI.checkIfAnswerIsFilled() == false) {
                        alert('Você precisa responder todas as perguntas!');
                        return;
                    }
                    
                    var request_url = [Constants.QUIZ_URL, '?', SubmitUI.getParams()].join('');
                    console.log(request_url);
                    
                    HttpJSON.get_request(request_url, function(data) {
                        console.log(data);
                        console.log('Enviado'); 
                    }, function() {
                        alert('Não foi possível se conectar com o servidor!');
                    });
                }
            }
            
            var JQueryEvents = {
                init : function() {
                    $('.send_button').bind('click', SubmitUI.sendAction);
                }
            }
            
            
            var Dispatch = {
                init : function() {
                    QuizWS.getQuestions(function(questions) {
                        $('.questions').html('');
                        
                        for(var i in questions) {
                            var question_item = questions[i];
                            var question_text = question_item.question;
                            var question_ui = QuestionUI.create(question_text);
                            
                            for(var j in question_item.answers) {
                                var answer_item = question_item.answers[j];
                                question_ui.add(answer_item, parseInt(j)+1)
                            }
                            
                            question_ui.appendTo('.questions');                            
                        }
                        
                    }), function() {
                        
                    };
                }
            }
        
            
        
            var Bootstrap = {
                init : function() {
                    Dispatch.init();
                    JQueryEvents.init();
                }
            };
        
            $(document).ready(function() {Bootstrap.init() });
        </script>        

        <script>        
            var question_text = 'De onde voce retira sua mana?';
        </script>        

    </body>
</html>