---
title: Cadenas
description: En esta sección se de abordan las funciones de cadena.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- resources,strings
- cadenas
- funciones de cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3799c151b828dba1d687068da6f7f5924aded09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478901"
---
# <a name="strings"></a>Cadenas

En esta sección se describen las funciones de cadena y se explica cómo usarlas en las aplicaciones.

### <a name="in-this-section"></a>En esta sección



| Nombre                                     | Descripción                                             |
|------------------------------------------|---------------------------------------------------------|
| [Acerca de las cadenas](about-strings.md)       | Describe las funciones de cadena.<br/>              |
| [Acerca de Strsafe.h](strsafe-ovw.md)       | Describe las funciones de cadena en Strsafe.h.<br/> |
| [Referencia de cadena](string-reference.md) | Contiene la referencia de API.<br/>                  |



 

### <a name="string-functions"></a>Funciones de cadena




| Nombre | Descripción | 
|------|-------------|
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a> | Convierte una cadena de caracteres o un solo carácter en minúsculas. Si el operando es una cadena de caracteres, la función convierte los caracteres en su lugar. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a> | Convierte los caracteres en mayúsculas de un búfer en caracteres en minúsculas. La función convierte los caracteres en su lugar. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a> | Recupera un puntero al carácter siguiente de una cadena. Esta función puede controlar cadenas que constan de caracteres de uno o varios bytes.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a> | Recupera el puntero al carácter siguiente de una cadena. Esta función puede controlar cadenas que constan de caracteres de uno o varios bytes.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a> | Recupera un puntero al carácter anterior de una cadena. Esta función puede controlar cadenas que constan de caracteres de uno o varios bytes.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a> | Recupera el puntero al carácter anterior de una cadena. Esta función puede controlar cadenas que constan de caracteres de uno o varios bytes.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> | Convierte una cadena en el juego de caracteres definido por OEM.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a> | Convierte un número especificado de caracteres de una cadena en el juego de caracteres definido por OEM.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a> | Convierte una cadena de caracteres o un solo carácter en mayúsculas. Si el operando es una cadena de caracteres, la función convierte los caracteres en su lugar. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a> | Convierte los caracteres en minúsculas de un búfer en caracteres en mayúsculas. La función convierte los caracteres en su lugar. <br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a> | Compara dos cadenas de caracteres con la configuración regional especificada.<blockquote>[!Note]<br />Para la compatibilidad con Unicode, use <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> o la versión Unicode de <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString.</strong></a></blockquote><br /><br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> | Compara dos cadenas Unicode (caracteres anchos), utilizando la configuración regional especificada.<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a> | Mapas una cadena a otra, realizando una opción de transformación especificada. <br /> | 
| <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> | Recupera información de tipo de carácter para los caracteres de la cadena de origen especificada. Para cada carácter de la cadena, la función establece uno o varios bits en el elemento de 16 bits correspondiente de la matriz de salida. Cada bit identifica un tipo de carácter determinado, por ejemplo, si el carácter es una letra, un dígito o ninguno.<br /> | 
| <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> | Recupera información de tipo de carácter para los caracteres de la cadena de origen especificada. Para cada carácter de la cadena, la función establece uno o varios bits en el elemento de 16 bits correspondiente de la matriz de salida. Cada bit identifica un tipo de carácter determinado, por ejemplo, si el carácter es una letra, un dígito o ninguno. <br /> A diferencia de sus familiares <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>cercanos GetStringTypeA</strong></a> y <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW,</strong></a> <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> muestra un comportamiento estándar mediante el uso del #define <strong>modificador UNICODE.</strong> Es la función recomendada.<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a> | Recupera información de tipo de carácter para los caracteres de la cadena de origen especificada. Para cada carácter de la cadena, la función establece uno o varios bits en el elemento de 16 bits correspondiente de la matriz de salida. Cada bit identifica un tipo de carácter determinado, por ejemplo, si el carácter es una letra, un dígito o ninguno.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a> | Determina si un carácter es alfabético. Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través Panel de control. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a> | Determina si un carácter es alfabético o numérico. Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través Panel de control. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a> | Determina si un carácter está en minúsculas. Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través Panel de control. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a> | Determina si un carácter está en mayúsculas. Esta determinación se basa en la semántica del idioma seleccionado por el usuario durante la instalación o a través Panel de control. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a> | Carga un recurso de cadena desde el archivo ejecutable asociado a un módulo especificado, copia la cadena en un búfer y anexa un carácter NULL final.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a> | Anexa una cadena a otra.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a> | Compara dos cadenas de caracteres. La comparación distingue mayúsculas de minúsculas.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a> | Compara dos cadenas de caracteres. La comparación no distingue entre mayúsculas y minúsculas.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a> | Copia una cadena en un búfer.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a> | Copia un número especificado de caracteres de una cadena de origen en un búfer. <br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a> | Determina la longitud de la cadena especificada (sin incluir el carácter nulo de terminación).<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a> | Convierte una cadena del juego de caracteres definido por OEM en una cadena ANSI o de caracteres anchos.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a> | Convierte un número especificado de caracteres en una cadena del juego de caracteres definido por OEM en una cadena ANSI o de caracteres anchos.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a> | Escribe datos con formato en el búfer especificado.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a> | Escribe datos con formato en el búfer especificado mediante un puntero a una lista de argumentos.<br /> | 




 

### <a name="strsafe-functions"></a>Funciones strsafe



| Nombre                                             | Descripción                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | Concatena una cadena a otra.<br/>                                            |
| [**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | Concatena una cadena a otra.<br/>                                            |
| [**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | Concatena el número especificado de bytes de una cadena a otra.<br/>         |
| [**StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | Concatena el número especificado de bytes de una cadena a otra.<br/>         |
| [**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | Copia una cadena en otra.<br/>                                                         |
| [**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | Copia una cadena en otra.<br/>                                                         |
| [**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | Copia el número especificado de bytes de una cadena a otra.<br/>                      |
| [**StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | Copia el número especificado de bytes de una cadena a otra.<br/>                      |
| [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | Obtiene una línea de texto de stdin, hasta e incluye el carácter de nueva línea (' \\ n').<br/>  |
| [**StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | Obtiene una línea de texto de stdin, hasta e incluye el carácter de nueva línea (' \\ n').<br/>  |
| [**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | Determina si una cadena supera la longitud especificada, en bytes.<br/>                   |
| [**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | Escribe datos con formato en la cadena especificada.<br/>                                        |
| [**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | Escribe datos con formato en la cadena especificada.<br/>                                        |
| [**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | Escribe datos con formato en la cadena especificada mediante un puntero a una lista de argumentos.<br/> |
| [**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | Escribe datos con formato en la cadena especificada mediante un puntero a una lista de argumentos.<br/> |
| [**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | Concatena una cadena a otra.<br/>                                            |
| [**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | Concatena una cadena a otra.<br/>                                            |
| [**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | Concatena el número especificado de caracteres de una cadena a otra.<br/>    |
| [**StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | Concatena el número especificado de caracteres de una cadena a otra.<br/>    |
| [**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | Copia una cadena en otra.<br/>                                                         |
| [**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | Copia una cadena en otra.<br/>                                                         |
| [**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | Copia el número especificado de caracteres de una cadena a otra.<br/>                 |
| [**StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | Copia el número especificado de caracteres de una cadena a otra.<br/>                 |
| [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | Obtiene una línea de texto de stdin, hasta e incluye el carácter de nueva línea (' \\ n').<br/>  |
| [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | Obtiene una línea de texto de stdin, hasta e incluye el carácter de nueva línea (' \\ n').<br/>  |
| [**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | Determina si una cadena supera la longitud especificada, en caracteres.<br/>              |
| [**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | Escribe datos con formato en la cadena especificada.<br/>                                        |
| [**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | Escribe datos con formato en la cadena especificada.<br/>                                        |
| [**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | Escribe datos con formato en la cadena especificada mediante un puntero a una lista de argumentos.<br/> |
| [**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | Escribe datos con formato en la cadena especificada mediante un puntero a una lista de argumentos.<br/> |



 

 

