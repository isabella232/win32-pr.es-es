---
description: Un literal es una cadena de caracteres que representa un valor en una instrucción de consulta. Los literales se usan para comparar valores de columna o para especificar términos de búsqueda. Windows Search admite los siguientes tipos de literales.
ms.assetid: cc526174-3c91-402d-b7d0-69fc9a61c3f9
title: Literales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e066f62a39bc46ec2ff7bf44c187d33f3832ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720328"
---
# <a name="literals"></a>Literales

Un literal es una cadena de caracteres que representa un valor en una instrucción de consulta. Los literales se usan para comparar valores de columna o para especificar términos de búsqueda. Windows Search admite los siguientes tipos de literales.


-   Los **literales de cadena** pueden tener cualquier longitud y pueden contener caracteres ANSI o Unicode. Debe incluir los literales de cadena entre comillas simples ('). Para incluir una comilla simple dentro de un literal de cadena, use dos comillas simples (' '). Representa una cadena vacía como dos comillas simples consecutivas (' ').
-   Los **literales numéricos** pueden contener los dígitos 0-9, un punto y la letra e (o e). Los literales numéricos representan números, incluidos enteros positivos y negativos, números decimales y valores de moneda. Los literales numéricos se pueden definir mediante la notación científica (por ejemplo, 2.3 E-05). No incluya un literal numérico entre comillas simples o se interpretará como un literal de cadena y se comparará mediante técnicas de comparación de cadenas. Los valores de moneda no pueden contener símbolos de moneda.
-   Los **literales hexadecimales** pueden contener los dígitos 0-9 y las letras a-f y a-f. Un literal hexadecimal representa un entero sin signo especificado en notación hexadecimal. Los literales hexadecimales deben comenzar por 0x.
    > [!Note]  
    > El estándar SQL-92 requiere que los literales hexadecimales se incluyan entre comillas simples. sin embargo, Windows Search no admite esa notación.

     

-   Los **literales booleanos** representan valores lógicos y pueden ser **true** o **false**. No incluya un literal booleano entre comillas simples o se interpretará como un literal de cadena.
-   Los **literales de fecha** representan fechas específicas, marcas de tiempo o tiempos relativos y se incluyen entre comillas simples. Debe colocar las fechas con el formato año/mes/día horas: minutos: segundos o año-mes-día horas: minutos: segundos, donde el mes, el día y el año son números. Especifique el año con un valor de cuatro dígitos, por ejemplo, 2004. Los valores de hora deben tener el formato horas: minutos: segundos. La sintaxis de Time relative se basa en la [función DateAdd](-search-sql-dateadd.md).

 

 



