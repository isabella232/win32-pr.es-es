---
description: Los datos de llamada son un búfer de tamaño de variable que se puede usar para acumular información sobre una sesión de comunicaciones. Esta información está disponible para todas las aplicaciones que poseen o supervisan la sesión.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Datos de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedfd44a46518a58f3a3aeaec59326648669cb49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360551"
---
# <a name="call-data"></a>Datos de llamada

Los datos de llamada son un búfer de tamaño de variable que se puede usar para acumular información sobre una sesión de comunicaciones. Esta información está disponible para todas las aplicaciones que poseen o supervisan la sesión.

Por ejemplo, el controlador inicial de una sesión entrante podría solicitar y escribir la información de la cuenta de cliente en un búfer de datos de llamada y, a continuación, los controladores subsiguientes no tendrían que repetir la solicitud.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**dwCallDataSize** y **DwCallDataOffset** Members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**line \_ CALLINFO**](./line-callinfo.md) Message (*dwParam1* establecido en LINECALLINFOSTATE \_ CALLDATA).

**TAPI 3. x:** Vea [**ITCallInfo::p UT \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIB \_ CALLDATABUFFER** [**CALLINFO \_**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent:: get \_ Causa**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) devuelve el **miembro \_ CALLDATA de CIC** de [**CALLINFOCHANGE \_ causa**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).

 

 
