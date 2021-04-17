---
description: La velocidad o el ancho de banda de una llamada especifica la velocidad de transmisión de datos. Tres puntos de datos identifican la velocidad actual de la velocidad máxima de un modo de portador especificado y la tasa mínima del modo de portador.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Tarifa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40747c26a98d8eb69e8161fb04302c5187121dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678237"
---
# <a name="rate"></a>Tarifa

La velocidad (o ancho de banda) de una llamada especifica la velocidad de transmisión de datos. Frecuencia de identificación de tres puntos de datos: la velocidad actual, la velocidad máxima de un modo de portador especificado y la tasa mínima del modo de portador.

No todos los proveedores de servicios admiten el uso de esta información.

* * TAPI 2. x: * *[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **DwMinRate** o **dwMaxRate** miembro de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ MAXRATE**, **CIL \_ MINRATE** o **CIL \_ Rate** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

* * TSPI: * *[**line \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) Message, con *dwParam1* establecido en LINECALLINFOSTATE \_ Rate

 

 
