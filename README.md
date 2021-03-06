"Agile" What ?
=============

Agile je "cool" izraz u developerskom svijetu posljednjih godina.

Međutim, kao i svi "hype" izrazi često se agilno upotrebljava a da se i
ne razumije previše.

Malo **developera**, a još manje **projekata** koji u cjelini razumiju ovaj
koncept.

Ja, nažalost, pripadam većini. 

Naslućujem, na osnovu čitanja na tu temu, da je agilni pristup razvoju software-a dobar. 

Ali, kako to staviti u svakodnevnu praksu ? Kako to primjenjivati u realnom kontekstu ? Da li u
mojoj ultra-small-size firmi uopšte ima smisla razmatrati taj koncept ?

Sve su to pitanja na koja nemam odgovor.

Na ovom mjestu ću ta pitanja pokušati barem djelimično doći do odgovora.

Započeću sa uspostavom agilnog razvojnog okruženja.


## Agile project management

## Continous integration CI - Jenkins

Jenkins je najpoznatiji OSS CI server. Sadrži plugin-ove za gotovo sve
poznate project management sisteme, SCM (source code management), programske jezike:

![plugins install](https://raw.github.com/hernad/agile_dev_env/master/img/jenkins_plugins.png)

### Primjer: PHP projekat

projekat sa testovima:

https://github.com/hernad/php-timer/blob/master/Tests/TimerTest.php

kreiranje jenkinks job-a (na osnovu
[php-template](http://jenkins-php.org)): 

![create job](https://raw.github.com/hernad/agile_dev_env/master/img/jenkings_create_job_from_php_template.png)

Na kraju dobijamo:

![agile php](https://raw.github.com/hernad/agile_dev_env/master/img/jenkins_agile_php.png)

Namjerno pravimo [test koji je neuspješan](https://github.com/hernad/php-timer/commit/ae3b1b2ccbeccbe65938c0aaba20e8b6249275f9) :

![test fail](https://raw.github.com/hernad/agile_dev_env/master/img/jenkins_test_fail.png)


## Case study: Adobe "brackets" projekat

Adobe brackets projekat primjenjuje "scrum" agile development metode. 

![sprint history](https://raw.github.com/hernad/agile_dev_env/master/img/brackets_trello_sprint_history.png)

![sprint card](https://raw.github.com/hernad/agile_dev_env/master/img/brackets_trello_card.png)

Gornji prikazi prikazuju način na koji developeri "brackets"-a obezbjeđuju efikasan uvid u trenutno stanje projekata, ali i uvid u istoriju ranijih operacija ("sprint"-ovi su iteracije)

Github "issues" se koristi u kombinaciji sa "trello"-om. Na prvi pogled,
tu bi moglo biti konfuzije, u smislu "nadležnosti" (šta se prijavljuje
na trello a šta na github issues. Na github-u su logično samo "code
related" stavke, a na trello-u svi zadaci razvojnog ciklusa). 

Ono što je pravo interesantno jeste kako je sistem labeliranja pomogao u
preglednosti i snalaženju po stavkama:
 
![github](https://raw.github.com/hernad/agile_dev_env/master/img/brakcets_github_issues.png)

#Analiza i dizajn toolset

## Dijagrami

### [PlantUML](http://plantuml.sourceforge.net)

![plantuml qeditor](https://raw.github.com/hernad/agile_dev_env/master/img/plantuml_example.png)




