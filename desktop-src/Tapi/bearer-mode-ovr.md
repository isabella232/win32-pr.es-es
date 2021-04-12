---
description: El modo de portador corresponde a la calidad de la transmisión solicitada desde la red para establecer una llamada.
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: Modo de portador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276163"
---
# <a name="bearer-mode"></a>Modo de portador

El [**modo de portador**](./linebearermode--constants.md) corresponde a la calidad de la transmisión solicitada desde la red para establecer una llamada. Es importante mantener el concepto de modo de portador independiente del [**tipo de medio**](tapimediatype--constants.md). Por ejemplo, la red de teléfono analógica (PSTN) solo proporciona un modo de portador de voz de 3,1 kHz, pero las llamadas que lo usan pueden admitir tipos de medios como voz, fax o módem de datos.

El modo de portador de una llamada se especifica cuando se configura la llamada o se proporciona cuando se ofrece la llamada. Con los dispositivos de línea capaces de representar grupos de canales, es posible que un proveedor de servicios permita que las llamadas se establezcan con un ancho de banda mayor.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x:** Consulte [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).

**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ BEARERMODE** miembro de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

**TSPI:** Vea el mensaje [**line \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) con *dwParam1* establecido en LINECALLINFOSTATE \_ BEARERMODE.

 

 
