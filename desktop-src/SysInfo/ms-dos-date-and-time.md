---
description: La fecha y la hora de ms-dos son valores de 16 bits empaquetados que especifican el mes, el día, el año y la hora del día en que se escribió por última vez en un archivo de MS-DOS.
ms.assetid: 948e6d77-dd01-4c90-9ef0-af143972c3fa
title: Fecha y hora de MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d401c731c9a3f5127511e28adf846c929a89a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666638"
---
# <a name="ms-dos-date-and-time"></a>Fecha y hora de MS-DOS

La **fecha** y la **hora** de ms-dos son valores de 16 bits empaquetados que especifican el mes, el día, el año y la hora del día en que se escribió por última vez en un archivo de ms-dos. MS-DOS registra la fecha y la hora en que una aplicación MS-DOS crea o escribe en un archivo. Las aplicaciones MS-DOS recuperan esta fecha y hora mediante funciones de MS-DOS. Cuando se usa la función [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) para recuperar las horas de archivo de los archivos creados por ms-dos, **GetFileTime** convierte automáticamente las fechas y horas de ms-dos en horas basadas en UTC.

Si encuentra una fecha y una hora de MS-DOS que no se han convertido, puede convertirla a una hora basada en UTC mediante la función [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) . Esta función copia la fecha y hora convertidas en una estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) . Puede volver a convertir el valor en una fecha y hora de MS-DOS mediante la función [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) .

 

 
