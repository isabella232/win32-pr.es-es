---
description: La especificación TSPI está estrechamente relacionada con las especificaciones de TAPI 2,2 (TAPI/C).
ms.assetid: 2c51f7e3-c741-4736-9611-2327d65b427e
title: Comparación general con TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce81d569d042cdd3eeb87088b1b7027858ca806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677941"
---
# <a name="overall-comparison-with-tapi"></a>Comparación general con TAPI

La especificación TSPI está estrechamente relacionada con las especificaciones de TAPI 2,2 (TAPI/C). La mayoría de las funciones de una tienen una función correspondiente en la otra. La correspondencia habitual es la siguiente:

-   Las funciones TSPI tienen los mismos nombres que las funciones TAPI, salvo que se anteponen a "**TSPI \_**". Por ejemplo, la función [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept) de TAPI corresponde a la función TSPI [**TSPI \_ lineAccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept).
-   Los procedimientos que permiten la operación asincrónica insertan un parámetro *dwRequestID* de tipo [DRV \_ REQUESTID](drv-requestid.md) como su primer parámetro. Este parámetro especifica el valor que se va a devolver para indicar la operación asincrónica y para notificar la finalización asincrónica.
-   los parámetros de *hCall* de tipo hCall se reemplazan por los parámetros *HdCall* de tipo [HDRVCALL](hdrvline.md), lo que indica el identificador del proveedor de servicios para la llamada.
-   los parámetros de *hLine* de tipo hLine se reemplazan por los parámetros *hdLine* de-Type [HDRVLINE](hdrvline.md), que indican el identificador del proveedor de servicios de la línea.
-   los parámetros de *hPhone* de tipo hPhone se reemplazan por los parámetros *HdPhone* del tipo [HDRVPHONE](hdrvphone.md), que indica el identificador del proveedor de servicios para el teléfono.
-   Los procedimientos que crean una nueva llamada, como [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), reemplazan un único parámetro *lphCall* con dos parámetros: un *htCall* de tipo [HTAPICALL](htapicall.md) parámetro que pasa el identificador de TAPI para la llamada y un *lphdCall* de tipo LPHDRVCALL que indica la ubicación en la que el proveedor de servicios debe escribir su nuevo identificador para la llamada. Se produce una división similar de parámetros en [**TSPI \_ LineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) y [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen).
-   En el nivel TSPI, no hay ninguna noción de "privilegio" asociada a los identificadores de dispositivo. Además, en el nivel de API, cada aplicación que tiene un dispositivo o identificador de llamada tiene un identificador diferente, pero TAPI los combina en un único identificador en el lado del proveedor de servicios. Como consecuencia, los códigos de error y los mensajes de estado relacionados con el privilegio y el número de clientes que usan un dispositivo no aparecen en el nivel TSPI.

El conjunto de funciones TAPI no asigna una a una al conjunto de funciones TSPI. En concreto, las funciones relacionadas con el privilegio, la traducción del número de teléfono y la comunicación entre aplicaciones se controlan mediante TAPI y no tienen ninguna función correspondiente en TSPI. Otras funciones, como las que se usan para la inicialización y configuración del proveedor de servicios, no tienen funciones correspondientes en TAPI.

 

 
