---
description: Los desarrolladores que crean aplicaciones para Tablet PC pueden aprovechar la información de contexto y el ámbito de entrada.
ms.assetid: 74e4e4b2-6ceb-4044-84df-2fff0788267a
title: Uso del contexto en la plataforma de Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd991a2ad8e76bb0a96ea5e41977b158cc30f5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468003"
---
# <a name="how-the-tablet-pc-platform-uses-context"></a>Uso del contexto en la plataforma de Tablet PC

Los desarrolladores que crean aplicaciones para Tablet PC pueden aprovechar la información de contexto y el ámbito de entrada. Las mejores soluciones posibles para establecer información de contexto sobre controles en aplicaciones dependen de si el control está habilitado para la entrada de lápiz y de si la aplicación se ha lanzado al mercado. Un control habilitado para lápiz es aquel que se ha diseñado específicamente para la entrada de lápiz y en el que los datos de entrada de lápiz se recopilan y conservan principalmente como entrada de lápiz. Algunos ejemplos de aplicaciones habilitadas para lápiz son Microsoft Windows Journal o un programa de bocetos. En un control que no está habilitado para la entrada de lápiz, los datos de entrada se recopilan y se conservan como texto, normalmente mediante el panel de entrada de Tablet PC cuando la aplicación se ejecuta en un pc tableta. Las soluciones para habilitar la información de contexto dentro de los controles son:

-   Api [SetInputScope:](/windows/win32/api/inputscope/nf-inputscope-setinputscope) una solución de programación de bajo nivel para controles y aplicaciones no habilitados para lápiz. Los archivos binarios de la aplicación se verán afectados y se deben redistribuir.
-   Propiedades [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) y [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto [**RecognizerContext:**](inkrecognizercontext-class.md) una solución mediante programación para aplicaciones con controles habilitados para lápiz. Los archivos binarios de la aplicación se verán afectados y se deben redistribuir.

El Panel de entrada de Tablet PC se ha actualizado a partir de Windows Vista para aprovechar la información de contexto que se proporciona al usar las API [SetInputScope.](/windows/win32/api/inputscope/nf-inputscope-setinputscope) En la tabla siguiente se proporcionan detalles sobre qué motores de reconocimiento de Microsoft admiten los ámbitos de entrada. Una "X" en la fila de un ámbito de entrada indica que el reconocedor de esa columna admite el ámbito de entrada.



| Nombre de la propiedad                                     | Inglés (Estados Unidos) | Inglés (Reino Unido) | Alemán       | Francés       | Japonés     | Coreano       | Chino (simplificado) | Chino (tradicional) |
|---------------------------------------------------|-------------------------|--------------------------|--------------|--------------|--------------|--------------|----------------------|-----------------------|
| **IS \_ ADDRESS \_ FULLPOSTALADDRESS**<br/>     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ POSTALCODE**<br/>            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ STREET**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ STATEORPROVINCE**<br/>       | X<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ CITY**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ COUNTRYNAME**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ COUNTRYSHORTNAME**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ CURRENCY \_ AMOUNTANDSYMBOL**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ CURRENCY \_ AMOUNT**<br/>               | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ FULLDATE**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ MES DE \_ FECHA**<br/>                    | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ DAY**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ YEAR**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ MONTHNAME**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ DAYNAME**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ EL VALOR PREDETERMINADO**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES EL NOMBRE \_ DE USUARIO DEL CORREO \_ ELECTRÓNICO**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ EMAIL \_ SMTPEMAILADDRESS**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ FILE \_ FULLFILEPATH**<br/>             | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ FILE \_ FILENAME**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ LOGINNAME**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DIGITS**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ NUMBER**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ONECHAR**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PASSWORD**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PERSONALNAME \_ FULLNAME**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PREFIJO \_ PERSONALNAME**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PERSONALNAME \_ GIVENNAME**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ PERSONALNAME \_ MIDDLENAME**<br/>       | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ NOMBRE PERSONAL \_ APELLIDO**<br/>          | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
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
| **ES \_ CHINO DE \_ MONEDA**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
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

 

