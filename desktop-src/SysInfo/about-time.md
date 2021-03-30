---
description: Las funciones relacionadas con el tiempo devuelven el tiempo en uno de varios formatos. Puede usar las funciones de tiempo para realizar la conversión entre algunos formatos de hora para facilitar la comparación y la visualización. En la tabla siguiente se resumen los formatos de hora.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Acerca del tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a95571637bb480920f82e90011a72f6eba9e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082768"
---
# <a name="about-time"></a>Acerca del tiempo

Las funciones relacionadas con el tiempo devuelven el tiempo en uno de varios formatos. Puede usar las funciones de tiempo para realizar la conversión entre algunos formatos de hora para facilitar la comparación y la visualización. En la tabla siguiente se resumen los formatos de hora.



| Formato          | Tipo                                                                     | Descripción                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Sistema          | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | Año, mes, día, hora, segundo y milisegundo, tomado del reloj de hardware interno.                                            |
| Local           | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) o [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) | Hora del sistema o hora de archivo convertida en la zona horaria local del sistema.                                                               |
| Archivo            | [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | El número de intervalos de 100 a nanosegundos desde el 1 de enero de 1601.                                                                       |
| MS-DOS          | **WORD**                                                                 | Una palabra empaquetada para la fecha, otra para el tiempo.                                                                                   |
| Windows         | **DWORD** o **ULONGLONG**                                               | Número de milisegundos desde la última vez que se inició el sistema. Cuando se recupera como un valor DWORD, la hora de Windows se recorre cada 49,7 días. |
| Recuento de interrupciones | **ULONGLONG**                                                            | El número de intervalos de 100 segundos desde la última vez que se inició el sistema.                                                           |



 

Para obtener más información, vea los temas siguientes:

-   [Hora del sistema](system-time.md)
-   [Hora local](local-time.md)
-   [Horas de archivo](file-times.md)
-   [Fecha y hora de MS-DOS](ms-dos-date-and-time.md)
-   [Hora de Windows](windows-time.md)
-   [Tiempo de interrupción](interrupt-time.md)

 

 
