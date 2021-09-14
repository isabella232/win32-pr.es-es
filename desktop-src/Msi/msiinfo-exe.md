---
description: Msiinfo.exe es una utilidad de línea de comandos que usa funciones de base de datos y funciones del instalador para editar o mostrar el flujo de información de resumen de una base de datos.
ms.assetid: 3f60146e-12bf-4755-bbca-93bb1c300fb7
title: Msiinfo.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98291c26678efa8b17b42c08bb34c0d1df16c6e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071847"
---
# <a name="msiinfoexe"></a>Msiinfo.exe

Msiinfo.exe es una utilidad de línea [](database-functions.md) de [](installer-functions.md) comandos que usa funciones de base de datos y funciones del instalador para editar o mostrar el flujo de información [de resumen](summary-information-stream.md) de una base de datos.

## <a name="syntax"></a>Sintaxis

**MsiInfo** *{database} \[ \[ /B \] /D \] {option}{data}*

-   La base de datos no puede ser una base de datos de solo lectura.
-   Si no hay datos seguidos de una opción, se quita la propiedad correspondiente.
-   Se puede especificar un máximo de 20 opciones en la línea de comandos. Las mismas propiedades se pueden especificar varias veces.
-   Si los datos contienen un espacio, incluya los datos entre comillas. Por ejemplo, como /T "MY TITLE".

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msiinfo.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guion. Para obtener más información, [vea Summary Information Stream Property Set](summary-information-stream-property-set.md).



| Opción | Descripción                                                                                                                                                                                                                                                                                                                                                      | Id. de propiedad        | PID |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----|
| *Ninguna* | Si no se especifica ninguna opción, la utilidad muestra los valores actuales de las propiedades Información de resumen.                                                                                                                                                                                                                                                      |                    |     |
| -b     | Muestra información sobre cada cadena del grupo de cadenas. La opción -b solo es válida si también se usa -d y -b debe ir antes que la opción -d.                                                                                                                                                                                                                 |                    |     |
| -d     | Muestra información sobre el grupo de cadenas. Valida el grupo de cadenas y proporciona información sobre la página de códigos de la base de datos. Tenga en cuenta que la página de códigos de la base de datos es diferente de la página de códigos de la secuencia de información de resumen (PID \_ CODEPAGE). Esta opción también comprueba todos los caracteres que no son válidos en la página de códigos de la base de datos. |                    |     |
| -i     | No aplicable. Reservado.                                                                                                                                                                                                                                                                                                                                        | DICCIONARIO \_ PID    | 0   |
| -c     | Establece la [**propiedad Codepage Summary**](codepage-summary.md).                                                                                                                                                                                                                                                                                                  | PÁGINA \_ DE CÓDIGOS PID      | 1   |
| -T     | Establece la [**propiedad Title Summary**](title-summary.md).                                                                                                                                                                                                                                                                                                        | TÍTULO \_ DE PID         | 2   |
| -j     | Establece la [**propiedad Subject Summary**](subject-summary.md).                                                                                                                                                                                                                                                                                                    | ID PID SUBJECT (ASUNTO DE PID \_ DE IDENTIFICADOR)    | 3   |
| -a     | Establece la [**propiedad Author Summary**](author-summary.md).                                                                                                                                                                                                                                                                                                      | AUTOR DE \_ PID        | 4   |
| -k     | Establece la [**propiedad De resumen de palabras clave.**](keywords-summary.md)                                                                                                                                                                                                                                                                                                  | PALABRAS \_ CLAVE PID      | 5   |
| -o     | Establece la [**propiedad Resumen de comentarios**](comments-summary.md).                                                                                                                                                                                                                                                                                                  | COMENTARIOS \_ DE PID      | 6   |
| -p     | Establece la [**propiedad Resumen de plantilla**](template-summary.md).                                                                                                                                                                                                                                                                                                  | PLANTILLA \_ DE PID      | 7   |
| -l     | Establece la [**propiedad Last Saved By Summary**](last-saved-by-summary.md).                                                                                                                                                                                                                                                                                        | PID \_ LASTAUTHOR    | 8   |
| -v     | Establece la [**propiedad Resumen del número de revisión**](revision-number-summary.md).                                                                                                                                                                                                                                                                                    | PID \_ REVNUMBER     | 9   |
| -E     | No aplicable. Reservado.                                                                                                                                                                                                                                                                                                                                        | PID \_ EDITTIME      | 10  |
| -S     | Establece la [**propiedad Last Printed Summary (Último resumen impreso).**](last-printed-summary.md) Para especificar el año, el mes, el día, la hora, el minuto y el segundo, use el formato "yyyy/mm/dd hh:mm:ss". Por ejemplo, "1997/06/20 03:25:59".                                                                                                                                                     | PID \_ LASTPRINTED   | 11  |
| -r     | Establece la [**propiedad De resumen de fecha y hora de creación**](create-time-date-summary.md). Para especificar el año, el mes, el día, la hora, el minuto y el segundo, use el formato "yyyy/mm/dd hh:mm:ss". Por ejemplo, "1997/06/20 03:25:59".                                                                                                                                             | PID \_ CREATE \_ DTM   | 12  |
| -q     | Establece la [**propiedad Last Saved Time/Date Summary**](last-saved-time-date-summary.md). Para especificar el año, el mes, el día, la hora, el minuto y el segundo, use el formato "yyyy/mm/dd hh:mm:ss". Por ejemplo, "1997/06/20 03:25:59".                                                                                                                                     | PID \_ LASTSAVE \_ DTM | 13  |
| -g     | Establece la [**propiedad Resumen de recuento de páginas**](page-count-summary.md).                                                                                                                                                                                                                                                                                              | PID \_ PAGECOUNT     | 14  |
| -w     | Establece la [**propiedad Resumen de recuento de palabras**](word-count-summary.md).                                                                                                                                                                                                                                                                                              | RECUENTO DE PALABRAS DE PID \_     | 15  |
| -H     | Establece la [**propiedad Resumen de recuento de caracteres**](character-count-summary.md).                                                                                                                                                                                                                                                                                    | PID \_ CHARCOUNT     | 16  |
|        | No aplicable. Reservado.                                                                                                                                                                                                                                                                                                                                        | MINIATURA DE \_ PID     | 17  |
| -n     | Establece la [**propiedad Creating Application Summary**](creating-application-summary.md).                                                                                                                                                                                                                                                                          | PID \_ APPNAME       | 18  |
| -U     | Establece la [**propiedad Resumen de seguridad**](security-summary.md).                                                                                                                                                                                                                                                                                                  | SEGURIDAD DE \_ PID      | 19  |



 

Esta herramienta solo está disponible en los componentes del [SDK de Windows para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



