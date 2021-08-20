---
description: Los datos de llamada son un búfer de tamaño variable que se puede usar para acumular información sobre una sesión de comunicaciones. Esta información está disponible para todas las aplicaciones que poseen o supervisan la sesión.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Llamar a datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afac8e7263a08c0dbecd9c643c577cf4d705dd728b271398f921d1530acecced
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948129"
---
# <a name="call-data"></a>Llamar a datos

Los datos de llamada son un búfer de tamaño variable que se puede usar para acumular información sobre una sesión de comunicaciones. Esta información está disponible para todas las aplicaciones que poseen o supervisan la sesión.

Por ejemplo, el controlador inicial de una sesión entrante podría solicitar y escribir la información de la cuenta de cliente en un búfer de datos de llamada y, a continuación, los controladores posteriores no tendrían que repetir la solicitud.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** y **dwCallDataOffset** miembros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**LINE \_ CALLINFO**](./line-callinfo.md) message (*dwParam1* establecido en LINECALLINFOSTATE \_ CALLDATA).

**TAPI 3.x:** Vea [**ITCallInfo::p ut \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) **(miembro CIB \_ CALLDATABUFFER** de [**CALLINFO \_ BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent::get \_ La causa**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) devuelve el **miembro CIC \_ CALLDATA** de [**CALLINFOCHANGE \_ CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).

 

 
