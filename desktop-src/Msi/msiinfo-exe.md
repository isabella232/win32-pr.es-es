---
description: Msiinfo.exe es una utilidad de línea de comandos que usa funciones de base de datos y funciones de instalador para editar o mostrar el flujo de información de Resumen de una base de datos.
ms.assetid: 3f60146e-12bf-4755-bbca-93bb1c300fb7
title: Msiinfo.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98291c26678efa8b17b42c08bb34c0d1df16c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912533"
---
# <a name="msiinfoexe"></a>Msiinfo.exe

Msiinfo.exe es una utilidad de línea de comandos que usa [funciones de base de datos](database-functions.md) y funciones de [instalador](installer-functions.md) para editar o mostrar el flujo de [información de Resumen](summary-information-stream.md) de una base de datos.

## <a name="syntax"></a>Sintaxis

**MsiInfo** *{base de \[ \[ datos}/b \] /d \] {opción} {Data}*

-   La base de datos no puede ser una base de datos de solo lectura.
-   Si no hay datos después de una opción, se quita la propiedad correspondiente.
-   Se puede especificar un máximo de 20 opciones en la línea de comandos. Se pueden especificar las mismas propiedades varias veces.
-   Si los datos contienen un espacio, inclúyalo entre comillas. Por ejemplo, como/T "mi título".

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msiinfo.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión. Para obtener más información, vea [conjunto de propiedades de flujo de información de Resumen](summary-information-stream-property-set.md).



| Opción | Descripción                                                                                                                                                                                                                                                                                                                                                      | Id. de propiedad        | PID |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----|
| *Ninguna* | Si no se especifica ninguna opción, la utilidad muestra los valores actuales de las propiedades de información de resumen.                                                                                                                                                                                                                                                      |                    |     |
| -b     | Muestra información sobre cada cadena en el grupo de cadenas. La opción-b solo es válida si también se usa-d y-b debe ser anterior a la opción-d.                                                                                                                                                                                                                 |                    |     |
| -d     | Muestra información sobre el grupo de cadenas. Valida el grupo de cadenas y proporciona información sobre la página de códigos de la base de datos. Tenga en cuenta que la página de códigos de la base de datos es diferente de la página de códigos de la secuencia de información de resumen (página de códigos de PID \_ ). Esta opción también comprueba en cada cadena los caracteres que no son válidos en la página de códigos de la base de datos. |                    |     |
| -i     | No es aplicable. Reservado.                                                                                                                                                                                                                                                                                                                                        | Diccionario de PID \_    | 0   |
| -c     | Establece la [**propiedad de Resumen**](codepage-summary.md)de la página de códigos.                                                                                                                                                                                                                                                                                                  | Página de códigos de PID \_      | 1   |
| -T     | Establece la [**propiedad de Resumen título**](title-summary.md).                                                                                                                                                                                                                                                                                                        | Título del PID \_         | 2   |
| -j     | Establece la [**propiedad de resumen del asunto**](subject-summary.md).                                                                                                                                                                                                                                                                                                    | asunto de identificador de PID \_    | 3   |
| -a     | Establece la [**propiedad de resumen del autor**](author-summary.md).                                                                                                                                                                                                                                                                                                      | autor del PID \_        | 4   |
| -k     | Establece la [**propiedad de Resumen Keywords**](keywords-summary.md).                                                                                                                                                                                                                                                                                                  | \_palabras clave de PID      | 5   |
| -o     | Establece la [**propiedad de Resumen comentarios**](comments-summary.md).                                                                                                                                                                                                                                                                                                  | Comentarios de PID \_      | 6   |
| -p     | Establece la [**propiedad de Resumen**](template-summary.md)de la plantilla.                                                                                                                                                                                                                                                                                                  | plantilla de PID \_      | 7   |
| -l     | Establece la [**última propiedad guardada por Resumen**](last-saved-by-summary.md).                                                                                                                                                                                                                                                                                        | PID \_ LASTAUTHOR    | 8   |
| -v     | Establece la [**propiedad de resumen del número de revisión**](revision-number-summary.md).                                                                                                                                                                                                                                                                                    | PID \_ REVNUMBER     | 9   |
| -E     | No es aplicable. Reservado.                                                                                                                                                                                                                                                                                                                                        | PID \_ EDITTIME      | 10  |
| -S     | Establece la [**última propiedad de Resumen impresa**](last-printed-summary.md). Para especificar el año, el mes, el día, la hora, el minuto y el segundo, use el formato "AAAA/MM/DD HH: mm: SS". Por ejemplo, "1997/06/20 03:25:59".                                                                                                                                                     | PID \_ LASTPRINTED   | 11  |
| -r     | Establece la [**propiedad de Resumen de fecha y hora de creación**](create-time-date-summary.md). Para especificar el año, el mes, el día, la hora, el minuto y el segundo, use el formato "AAAA/MM/DD HH: mm: SS". Por ejemplo, "1997/06/20 03:25:59".                                                                                                                                             | PID \_ Create \_ DTM   | 12  |
| -q     | Establece la [**propiedad de Resumen de fecha y hora de la última vez**](last-saved-time-date-summary.md)que se ha guardado. Para especificar el año, el mes, el día, la hora, el minuto y el segundo, use el formato "AAAA/MM/DD HH: mm: SS". Por ejemplo, "1997/06/20 03:25:59".                                                                                                                                     | PID \_ LASTSAVE \_ DTM | 13  |
| -g     | Establece la [**propiedad de Resumen de recuento de páginas**](page-count-summary.md).                                                                                                                                                                                                                                                                                              | PID \_ PAGECOUNT     | 14  |
| -w     | Establece la [**propiedad de Resumen de recuento de palabras**](word-count-summary.md).                                                                                                                                                                                                                                                                                              | PID \_ WORDCOUNT     | 15  |
| -H     | Establece la [**propiedad de Resumen de recuento de caracteres**](character-count-summary.md).                                                                                                                                                                                                                                                                                    | CHARCOUNT de PID \_     | 16  |
|        | No es aplicable. Reservado.                                                                                                                                                                                                                                                                                                                                        | miniatura de PID \_     | 17  |
| -n     | Establece la [**propiedad de Resumen**](creating-application-summary.md)de la aplicación de creación.                                                                                                                                                                                                                                                                          | PID \_ APPNAME       | 18  |
| -U     | Establece la [**propiedad de Resumen de seguridad**](security-summary.md).                                                                                                                                                                                                                                                                                                  | seguridad de PID \_      | 19  |



 

Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



