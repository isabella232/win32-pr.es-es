---
description: Los desarrolladores que crean aplicaciones para tablet PC pueden aprovechar la información de contexto y el ámbito de entrada.
ms.assetid: 74e4e4b2-6ceb-4044-84df-2fff0788267a
title: Uso del contexto en la plataforma de tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c586bf3ffcff8fc92b02bc0b4f5aff79c6bd0bbd66e6f048eab35a78d3be9676
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709285"
---
# <a name="how-the-tablet-pc-platform-uses-context"></a>Uso del contexto en la plataforma de tablet PC

Los desarrolladores que crean aplicaciones para tablet PC pueden aprovechar la información de contexto y el ámbito de entrada. Las mejores soluciones posibles para establecer información de contexto sobre los controles en las aplicaciones dependen de si el control está habilitado para la entrada de lápiz y de si la aplicación se ha lanzado al mercado. Un control habilitado para entrada de lápiz es aquel que se ha diseñado específicamente para la entrada de lápiz y en el que los datos de entrada de lápiz se recopilan y conservan principalmente como entrada de lápiz. Algunos ejemplos de aplicaciones habilitadas para lápiz son Microsoft Windows Journal o un programa de bocetos. En un control que no está habilitado para la entrada de lápiz, los datos de entrada se recopilan y se conservan como texto, normalmente mediante el panel de entrada de Tablet PC cuando la aplicación se ejecuta en un tablet PC. Las soluciones para habilitar la información de contexto dentro de los controles son:

-   Las [API SetInputScope:](/windows/win32/api/inputscope/nf-inputscope-setinputscope) una solución de programación de bajo nivel para controles y aplicaciones no habilitados para entrada de lápiz. Los archivos binarios de la aplicación se verán afectados y se deben redistribuir.
-   Propiedades [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) y [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto [**RecognizerContext:**](inkrecognizercontext-class.md) una solución mediante programación para aplicaciones con controles habilitados para la entrada de lápiz. Los archivos binarios de la aplicación se verán afectados y se deben redistribuir.

El panel de entrada de Tablet PC se ha actualizado a partir de Windows Vista para aprovechar la información de contexto que se proporciona al usar las API [SetInputScope.](/windows/win32/api/inputscope/nf-inputscope-setinputscope) En la tabla siguiente se proporcionan detalles sobre qué motores de reconocimiento de Microsoft admiten los ámbitos de entrada. Una "X" en la fila de un ámbito de entrada indica que el reconocedor de esa columna admite el ámbito de entrada.



| Nombre de la propiedad                                     | Inglés (Estados Unidos) | Inglés (Reino Unido) | Alemán       | Francés       | Japonés     | Coreano       | Chino (simplificado) | Chino (tradicional) |
|---------------------------------------------------|-------------------------|--------------------------|--------------|--------------|--------------|--------------|----------------------|-----------------------|
| **IS \_ ADDRESS \_ FULLPOSTALADDRESS**<br/>     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ POSTALCODE**<br/>            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ STREET**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ STATEORPROVINCE**<br/>       | X<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ CITY**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ COUNTRYNAME**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ LA DIRECCIÓN \_ COUNTRYSHORTNAME**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ CURRENCY \_ AMOUNTANDSYMBOL**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES LA \_ CANTIDAD DE \_ MONEDA**<br/>               | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ DATE \_ FULLDATE**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ FECHA \_ MES**<br/>                    | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ DATE \_ DAY**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ DATE \_ YEAR**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ DATE \_ MONTHNAME**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ DATE \_ DAYNAME**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ EL VALOR PREDETERMINADO**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES EL NOMBRE \_ DE USUARIO DEL CORREO \_ ELECTRÓNICO**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ EMAIL \_ SMTPEMAILADDRESS**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ FILE \_ FULLFILEPATH**<br/>             | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ FILE \_ FILENAME**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ LOGINNAME**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DIGITS**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ NUMBER**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ ONECHAR**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PASSWORD**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PERSONALNAME \_ FULLNAME**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PREFIJO \_ PERSONALNAME**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PERSONALNAME \_ GIVENNAME**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ PERSONALNAME \_ MIDDLENAME**<br/>       | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PERSONALNAME \_ SURNAME**<br/>          | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ EL SUFIJO \_ PERSONALNAME**<br/>           | X<br/>            | -<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TELEPHONE \_ FULLTELEPHONENUMBER**<br/> | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TELEPHONE \_ COUNTRYCODE**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TELEPHONE \_ AREACODE**<br/>            | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TELEPHONE \_ LOCALNUMBER**<br/>         | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TIME \_ FULLTIME**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES HORA \_ \_ DE LA HORA**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TIME \_ MINORSEC**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **DIRECCIÓN \_ URL DE IS**<br/>                            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ NUMBER \_ FULLWIDTH**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ALPHANUMERIC \_ HALFWIDTH**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ALPHANUMERIC \_ FULLWIDTH**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ MONEDA \_ CHINA**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ BOPOMOFO**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ HIRAGANA**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ KATAKANA \_ HALFWIDTH**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ KATAKANA \_ FULLWIDTH**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ HANJA**<br/>                          | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |



 

Cuando se usan las API [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) o la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) para establecer el contexto, el intento de establecer un ámbito de entrada para un idioma que no es compatible con el reconocedor de ese idioma hace que el Panel de entrada de Tablet PC use el modelo de lenguaje predeterminado como contexto para el control. Por ejemplo, el reconocedor francés no admite el ámbito de entrada **IS \_ ADDRESS \_ STATEORPROVINCE.** Si establece el contexto en un campo como

`(!IS_ADDRESS_STATEORPROVINCE)|(!IS_ADDRESS_POSTALCODE)`

cuando se usa el reconocedor de francés, el contexto resultante es el modelo de lenguaje predeterminado. Para evitar este problema, detecte el idioma del reconocedor en uso y establezca los ámbitos de entrada en consecuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeración InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)
</dt> </dl>

 

