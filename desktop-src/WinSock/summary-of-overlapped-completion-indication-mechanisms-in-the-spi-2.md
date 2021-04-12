---
description: Resumen de los mecanismos de indicación de finalización superpuestos en el SPI de Windows Sockets (Winsock).
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Resumen de los mecanismos de indicación de finalización superpuestos en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154245"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a>Resumen de los mecanismos de indicación de finalización superpuestos en el SPI

En la tabla siguiente se resume la semántica de finalización de un socket superpuesto, que muestra la combinación de *lpOverlapped*, **hEvent** y *lpCompletionRoutine*.



| *lpOverlapped* | **hEvent**     | *lpCompletionRoutine* | Indicación de finalización                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | No aplicable | Omitido               | La operación se completa de forma sincrónica, es decir, se comporta como si fuera un socket nonoverlapped.                                                                                                                                 |
| no NULL       | NULL           | NULL                  | La operación se completa superpuesta, pero no hay ningún mecanismo de finalización compatible con Windows Sockets 2. En este caso, se puede usar el mecanismo de puerto de finalización (si se admite); de lo contrario, no habrá ninguna notificación de finalización. |
| no NULL       | no NULL       | NULL                  | La operación se completa y se notifica mediante un objeto de evento de señalización.                                                                                                                                                      |
| no NULL       | Omitido        | no NULL              | La operación se completa y se notifica mediante la programación de la rutina de finalización.                                                                                                                                               |



 

 

 



