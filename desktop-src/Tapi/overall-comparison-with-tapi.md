---
description: La especificación TSPI está muy relacionada con las especificaciones de TAPI 2.2 (TAPI/C).
ms.assetid: 2c51f7e3-c741-4736-9611-2327d65b427e
title: Comparación general con TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecedd5a53fd30e2a49b6d44e90d30f86ff8469f002166ca3328f3146a2748b78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002813"
---
# <a name="overall-comparison-with-tapi"></a>Comparación general con TAPI

La especificación TSPI está muy relacionada con las especificaciones de TAPI 2.2 (TAPI/C). La mayoría de las funciones de una tienen una función correspondiente en la otra. La correspondencia habitual es la siguiente:

-   Las funciones TSPI tienen los mismos nombres que las funciones TAPI, salvo que se anteponen con **\_ "TSPI".** Por ejemplo, la función TAPI [**lineAccept corresponde**](/windows/win32/api/tapi/nf-tapi-lineaccept) a la función [**TSPI \_ lineAccept de TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   Los procedimientos que permiten la operación asincrónica insertan *un parámetro dwRequestID* de tipo [DRV \_ REQUESTID](drv-requestid.md) como primer parámetro. Este parámetro especifica el valor que se va a devolver para indicar la operación asincrónica y para notificar la finalización asincrónica.
-   *Los parámetros hCall* del tipo HCALL se reemplazan por parámetros *hdCall* de tipo [HDRVCALL,](hdrvline.md)lo que indica el identificador del proveedor de servicios para la llamada.
-   *Los parámetros hLine* del tipo HLINE se reemplazan por parámetros *hdLine* de -type [HDRVLINE](hdrvline.md), lo que indica el identificador del proveedor de servicios para la línea.
-   *Los parámetros hPhone* de tipo HPHONE se reemplazan por parámetros *hdPhone* de tipo [HDRVPHONE,](hdrvphone.md)lo que indica el identificador del proveedor de servicios para el teléfono.
-   Los procedimientos que crean una nueva llamada, como [**TSPI \_ lineMakeCall,**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)reemplazan un único parámetro *lphCall* por dos parámetros: un *htCall* de tipo [HTAPICALL](htapicall.md) que pasa el identificador TAPI para la llamada y un *lphdCall* de tipo LPHDRVCALL que indica la ubicación en la que el proveedor de servicios debe escribir su nuevo identificador para la llamada. Se produce una división similar de parámetros en [**la línea \_ TSPIAbrir**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) y [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen).
-   En el nivel de TSPI, no hay ninguna noción de "privilegio" asociada a los identificadores de dispositivo. Además, en el nivel de API, cada aplicación que tiene un dispositivo o identificador de llamada tiene un identificador diferente, pero TAPI los combina en un único identificador en el lado del proveedor de servicios. Como consecuencia, los códigos de error y los mensajes de estado relacionados con el privilegio y el número de clientes que usan un dispositivo no aparecen en el nivel de TSPI.

El conjunto de funciones TAPI no asigna uno a uno al conjunto de funciones TSPI. En concreto, las funciones relacionadas con privilegios, traducción de números de teléfono y comunicación entre aplicaciones se controlan mediante TAPI y no tienen ninguna función correspondiente en TSPI. Otras funciones, como las que se usan para la configuración e inicialización del proveedor de servicios, no tienen ninguna función correspondiente en TAPI.

 

 
