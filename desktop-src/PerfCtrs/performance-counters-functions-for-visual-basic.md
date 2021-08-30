---
description: Puede usar las siguientes funciones para trabajar con datos de rendimiento en Visual Basic.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Funciones de contadores de rendimiento para Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68fa9b417f6db987110d03fc0c3c88a920adf8cd70cf0ff5f844f26c0ef5c35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033525"
---
# <a name="performance-counters-functions-for-visual-basic"></a>Funciones de contadores de rendimiento para Visual Basic

> [!IMPORTANT]
> Las funciones que describe este tema pueden modificarse o no estar disponibles en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Puede usar las siguientes funciones para trabajar con datos de rendimiento en Visual Basic.

- [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [**PdhVbAddCounter**](pdhvbaddcounter.md)
- [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
- [**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
- [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
- [**PdhVbGetDoubleCounterValue**](pdhvbgetdoublecountervalue.md)
- [**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
- [**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
- [**PdhVbIsStatus**](pdhvbisgoodstatus.md)
- [**PdhVbOpenLog**](pdhvbopenlog.md)
- [**PdhVbOpenQuery**](pdhvbopenquery.md)
- [**PdhVbUpdateLog**](pdhvbupdatelog.md)

> [!NOTE]
> Las funciones funcionan en una sesión por proceso y `PdhVb***` no son seguras para subprocesos. Estas funciones solo se deben usar desde aplicaciones sencillas de un solo subproceso.
