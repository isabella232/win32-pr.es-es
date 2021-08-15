---
description: Las funciones relacionadas con el tiempo devuelven el tiempo en uno de varios formatos. Puede usar las funciones de tiempo para convertir entre algunos formatos de tiempo para facilitar la comparación y la presentación. En la tabla siguiente se resumen los formatos de hora.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Ya era hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cb2cd140ada7033ebe7bf672e654dbf7227385509c676176ee8e936ff590ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765036"
---
# <a name="about-time"></a>Ya era hora

Las funciones relacionadas con el tiempo devuelven el tiempo en uno de varios formatos. Puede usar las funciones de tiempo para convertir entre algunos formatos de tiempo para facilitar la comparación y la presentación. En la tabla siguiente se resumen los formatos de hora.



| Formato          | Tipo                                                                     | Descripción                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Sistema          | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | Año, mes, día, hora, segundo y milisegundo, tomados del reloj de hardware interno.                                            |
| Local           | [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) o [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) | Hora del sistema o hora de archivo convertida en la zona horaria local del sistema.                                                               |
| Archivo            | [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | Número de intervalos de 100 nanosegundos desde el 1 de enero de 1601.                                                                       |
| MS-DOS          | **WORD**                                                                 | Palabra empaquetada para la fecha y otra para la hora.                                                                                   |
| Windows         | **DWORD** o **ULONGLONG**                                               | Número de milisegundos desde que se inició por última vez el sistema. Cuando se recupera como un valor DWORD, Windows de tiempo cada 49,7 días. |
| Recuento de interrupciones | **ULONGLONG**                                                            | Número de intervalos de 100 nanosegundos desde que se inició por última vez el sistema.                                                           |



 

Para obtener más información, vea los temas siguientes:

-   [Hora del sistema](system-time.md)
-   [Hora local](local-time.md)
-   [Horas de archivo](file-times.md)
-   [Fecha y hora de MS-DOS](ms-dos-date-and-time.md)
-   [Hora de Windows](windows-time.md)
-   [Hora de interrupción](interrupt-time.md)

 

 
