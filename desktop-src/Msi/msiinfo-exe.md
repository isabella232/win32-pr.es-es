---
description: Msiinfo.exe es una utilidad de línea de comandos que usa Funciones de base de datos y Funciones del instalador para editar o mostrar el flujo de información de resumen de una base de datos.
ms.assetid: 3f60146e-12bf-4755-bbca-93bb1c300fb7
title: Msiinfo.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57487406533b060d9343d4afbdf7e5254c32e15149bb3385f81cc7dc3923fc71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628127"
---
# <a name="msiinfoexe"></a>Msiinfo.exe

Msiinfo.exe es una utilidad de [](database-functions.md) línea de [](installer-functions.md) comandos que usa funciones de base de datos y funciones del instalador para editar o mostrar el flujo de información de [resumen](summary-information-stream.md) de una base de datos.

## <a name="syntax"></a>Syntax

**MsiInfo** *{database} \[ \[ /B \] /D \] {option}{data}*

-   La base de datos no puede ser una base de datos de solo lectura.
-   Si ningún dato sigue una opción, se quita la propiedad correspondiente.
-   Se puede especificar un máximo de 20 opciones en la línea de comandos. Las mismas propiedades se pueden especificar varias veces.
-   Si los datos contienen un espacio, incluya los datos entre comillas. Por ejemplo, como /T "MY TITLE".

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msiinfo.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta las mayúsculas y minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión. Para obtener más información, [vea Summary Information Stream Property Set](summary-information-stream-property-set.md).



| Opción | Descripción                                                                                                                                                                                                                                                                                                                                                      | Id. de propiedad        | PID |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----|
| *Ninguna* | Si no se especifica ninguna opción, la utilidad muestra los valores actuales de las propiedades Información de resumen.                                                                                                                                                                                                                                                      |                    |     |
| -b     | Muestra información sobre cada cadena del grupo de cadenas. La opción -b solo es válida si también se usa -d y -b debe ir antes que la opción -d.                                                                                                                                                                                                                 |                    |     |
| -d     | Muestra información sobre el grupo de cadenas. Valida el grupo de cadenas y proporciona información sobre la página de códigos de la base de datos. Tenga en cuenta que la página de códigos de la base de datos es diferente de la página de códigos del flujo de información de resumen (PID \_ CODEPAGE). Esta opción también comprueba en cada cadena los caracteres que no son válidos en la página de códigos de la base de datos. |                    |     |
| -i     | No es aplicable. Reservado.                                                                                                                                                                                                                                                                                                                                        | DICCIONARIO \_ PID    | 0   |
| -c     | Establece la [**propiedad Resumen de página de códigos**](codepage-summary.md).                                                                                                                                                                                                                                                                                                  | PÁGINA DE CÓDIGOS DE PID \_      | 1   |
| -T     | Establece la [**propiedad Title Summary**](title-summary.md).                                                                                                                                                                                                                                                                                                        | TÍTULO \_ DE PID         | 2   |
| -j     | Establece la [**propiedad Subject Summary**](subject-summary.md).                                                                                                                                                                                                                                                                                                    | ASUNTO DE PID \_ DE IDENTIFICADOR    | 3   |
| -a     | Establece la [**propiedad Author Summary**](author-summary.md).                                                                                                                                                                                                                                                                                                      | AUTOR DE \_ PID        | 4   |
| -k     | Establece la [**propiedad Resumen de palabras clave**](keywords-summary.md).                                                                                                                                                                                                                                                                                                  | PALABRAS \_ CLAVE PID      | 5   |
| -o     | Establece la [**propiedad Resumen de comentarios**](comments-summary.md).                                                                                                                                                                                                                                                                                                  | COMENTARIOS \_ DE PID      | 6   |
| -p     | Establece la [**propiedad Resumen de plantilla**](template-summary.md).                                                                                                                                                                                                                                                                                                  | PLANTILLA DE \_ PID      | 7   |
| -l     | Establece la [**última propiedad Guardada por resumen**](last-saved-by-summary.md).                                                                                                                                                                                                                                                                                        | PID \_ LASTAUTHOR    | 8   |
| -v     | Establece la [**propiedad Resumen de número de revisión**](revision-number-summary.md).                                                                                                                                                                                                                                                                                    | PID \_ REVNUMBER     | 9   |
| -E     | No es aplicable. Reservado.                                                                                                                                                                                                                                                                                                                                        | PID \_ EDITTIME      | 10  |
| -S     | Establece la [**propiedad Last Printed Summary (Último resumen impreso).**](last-printed-summary.md) Para especificar el año, mes, día, hora, minuto y segundo, use el formato "yyyy/mm/dd hh:mm:ss". Por ejemplo, "1997/06/20 03:25:59".                                                                                                                                                     | PID \_ LASTPRINTED   | 11  |
| -r     | Establece la [**propiedad Create Time/Date Summary**](create-time-date-summary.md). Para especificar el año, mes, día, hora, minuto y segundo, use el formato "yyyy/mm/dd hh:mm:ss". Por ejemplo, "1997/06/20 03:25:59".                                                                                                                                             | PID \_ CREATE \_ DTM   | 12  |
| -q     | Establece la [**propiedad Resumen de fecha y hora guardadas por última vez.**](last-saved-time-date-summary.md) Para especificar el año, mes, día, hora, minuto y segundo, use el formato "yyyy/mm/dd hh:mm:ss". Por ejemplo, "1997/06/20 03:25:59".                                                                                                                                     | PID \_ LASTSAVE \_ DTM | 13  |
| -g     | Establece la [**propiedad Resumen de recuento de páginas**](page-count-summary.md).                                                                                                                                                                                                                                                                                              | PID \_ PAGECOUNT     | 14  |
| -w     | Establece la [**propiedad Resumen de recuento de palabras**](word-count-summary.md).                                                                                                                                                                                                                                                                                              | PID \_ WORDCOUNT     | 15  |
| -H     | Establece la [**propiedad Resumen de recuento de caracteres**](character-count-summary.md).                                                                                                                                                                                                                                                                                    | PID \_ CHARCOUNT     | 16  |
|        | No es aplicable. Reservado.                                                                                                                                                                                                                                                                                                                                        | MINIATURA DE \_ PID     | 17  |
| -n     | Establece la [**propiedad Creating Application Summary**](creating-application-summary.md).                                                                                                                                                                                                                                                                          | PID \_ APPNAME       | 18  |
| -U     | Establece la [**propiedad Resumen de seguridad**](security-summary.md).                                                                                                                                                                                                                                                                                                  | SEGURIDAD DE \_ PID      | 19  |



 

Esta herramienta solo está disponible en los componentes del [SDK Windows para Windows instalador de .](platform-sdk-components-for-windows-installer-developers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



