---
description: Los desarrolladores que crean aplicaciones para Tablet PC pueden aprovechar el ámbito de entrada y la información de contexto.
ms.assetid: 74e4e4b2-6ceb-4044-84df-2fff0788267a
title: Cómo usa la plataforma de Tablet PC el contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd991a2ad8e76bb0a96ea5e41977b158cc30f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648207"
---
# <a name="how-the-tablet-pc-platform-uses-context"></a>Cómo usa la plataforma de Tablet PC el contexto

Los desarrolladores que crean aplicaciones para Tablet PC pueden aprovechar el ámbito de entrada y la información de contexto. Las mejores soluciones posibles para establecer la información de contexto en los controles de las aplicaciones dependen de si el control está habilitado para tinta y de si la aplicación se ha lanzado al mercado. Un control habilitado para tinta es el que se ha diseñado específicamente para la entrada manuscrita y en la que los datos de tinta se recopilan y se conservan como tinta. Algunos ejemplos de aplicaciones habilitadas para tinta son Microsoft Windows Journal o un programa de boceto. En un control que no está habilitado para tinta, los datos de entrada se recopilan y se conservan como texto, normalmente mediante el panel de entrada de Tablet PC cuando la aplicación se ejecuta en un Tablet PC. Las soluciones para habilitar la información de contexto dentro de los controles son:

-   Las API de [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) : solución de bajo nivel de programación para aplicaciones y controles no habilitados para la entrada de lápiz. Los archivos binarios de la aplicación se ven afectados y deben redistribuirse.
-   Las propiedades [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) y de la [**palabras de palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) : una solución de programación para aplicaciones con controles que tienen habilitada la tinta. Los archivos binarios de la aplicación se ven afectados y deben redistribuirse.

El panel de entrada de Tablet PC se ha actualizado a partir de Windows Vista para aprovechar la información de contexto que se proporciona al usar las API de [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) . En la tabla siguiente se proporcionan detalles sobre los motores de reconocimiento de Microsoft que admiten los ámbitos de entrada. Una "X" en la fila de un ámbito de entrada indica que el reconocedor de esa columna admite el ámbito de entrada.



| Nombre de la propiedad                                     | Spanish (Traditional Sort) - Spain | Inglés (Reino Unido) | Alemán       | Francés       | Japonés     | Coreano       | Chino (simplificado) | Chino (tradicional) |
|---------------------------------------------------|-------------------------|--------------------------|--------------|--------------|--------------|--------------|----------------------|-----------------------|
| **ES la \_ dirección \_ FULLPOSTALADDRESS**<br/>     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ dirección \_ CódigoPostal**<br/>            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_dirección \_ calle**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES la \_ dirección \_ STATEORPROVINCE**<br/>       | X<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_dirección \_ ciudad**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES la \_ dirección \_ COUNTRYNAME**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES la \_ dirección \_ COUNTRYSHORTNAME**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ AMOUNTANDSYMBOL de moneda \_**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_importe de moneda \_**<br/>               | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_fecha \_ FULLDATE**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES el mes de la \_ fecha \_**<br/>                    | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES el día de la \_ fecha \_**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES el año de la \_ fecha \_**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES la \_ fecha \_ MONTHNAME**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_fecha \_ DAYNAME**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES el \_ valor predeterminado**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES el \_ nombre de usuario de correo electrónico \_**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ SMTPEMAILADDRESS de correo electrónico \_**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES el \_ archivo \_ FULLFILEPATH**<br/>             | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ \_ filename File**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ LoginName**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_dígitos**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_número**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ ONECHAR**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_contraseña**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PERSONALNAME \_ FULLNAME**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **Prefijo de \_ PERSONALNAME \_**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_PERSONALNAME \_ GIVENNAME**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PERSONALNAME \_ MIDDLENAME**<br/>       | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ PERSONALNAME \_ apellidos**<br/>          | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_sufijo PERSONALNAME \_**<br/>           | X<br/>            | -<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ teléfono \_ FULLTELEPHONENUMBER**<br/> | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ el \_ COUNTRYCODE del teléfono**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES el \_ teléfono \_ AREACODE**<br/>            | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ teléfono \_ LOCALNUMBER**<br/>         | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ el tiempo \_ FULLTIME**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **hora \_ hora \_**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_hora \_ MINORSEC**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_dirección URL**<br/>                            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES el \_ número de \_ ancho completo**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ alfanumérico de \_ ancho medio**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **TIENE \_ un \_ ancho completo alfanumérico**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ chino de moneda \_**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ BOPOMOFO**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_hiragana**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ katakana katakana \_**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ de \_ ancho completo katakana**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ES \_ hanja**<br/>                          | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |



 

Cuando se usan las API de [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) o la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) para establecer el contexto, el intento de establecer un ámbito de entrada para un idioma que no es compatible con el reconocedor de ese idioma hace que el panel de entrada de Tablet PC use el modelo de idioma predeterminado como contexto del control. Por ejemplo, el reconocedor francés de la **\_ dirección \_ STATEORPROVINCE** no es compatible con el ámbito de entrada. Si establece el contexto en un campo como

`(!IS_ADDRESS_STATEORPROVINCE)|(!IS_ADDRESS_POSTALCODE)`

al usar el reconocedor francés, el contexto resultante es el modelo de idioma predeterminado. Para evitar este problema, detecte el idioma del reconocedor en uso y establezca los ámbitos de entrada en consecuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[InputScope (enumeración)](/windows/win32/api/inputscope/ne-inputscope-inputscope)
</dt> </dl>

 

