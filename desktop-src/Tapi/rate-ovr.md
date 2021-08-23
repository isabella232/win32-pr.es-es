---
description: La velocidad o ancho de banda de una llamada especifica la velocidad de transmisión de datos. Tres puntos de datos identifican la velocidad actual de la velocidad máxima para un modo de portador especificado y la velocidad mínima para el modo de portador.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Tarifa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0af0b2dd6dfe34759753f52773bafe0bdf2bf8f4472ed863dcc6c8b0f10a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060563"
---
# <a name="rate"></a>Tarifa

La velocidad (o ancho de banda) de una llamada especifica la velocidad de transmisión de datos. Tres puntos de datos identifican la velocidad: la velocidad actual, la velocidad máxima para un modo de portador especificado y la velocidad mínima para el modo de portador.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x: **[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo,**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) **dwMinRate** o **dwMaxRate** miembro de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p ut \_ CallInfoLong,**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) **CIL \_ MAXRATE,** **CIL \_ MINRATE** o **miembro CIL \_ RATE** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

**TSPI: **[**Mensaje \_ LINE CALLINFO,**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) con *dwParam1* establecido en LINECALLINFOSTATE \_ RATE

 

 
