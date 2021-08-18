---
description: La información del usuario es un búfer que se puede transmitir desde un extremo de una conexión a otro. Esta información es específica del estándar ISDN Q.931. Consulte la documentación de los proveedores de servicios sobre el significado y el uso de estos datos.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Información del usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 203b0b466d1b0b3f9da93cfefc5da737865da3cf5d40921dae6c969bfc9b9752
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975295"
---
# <a name="user-user-information"></a>Información del usuario

La información del usuario es un búfer que se puede transmitir desde un extremo de una conexión a otro. Esta información es específica del estándar ISDN Q.931. Consulte la documentación del proveedor de servicios sobre el significado y el uso de estos datos.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** y **dwCallDataOffset** miembros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

**TAPI 3.x: **[**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), al que se llama con el miembro **\_ CIB USERUSERINFO** de [**CALLINFO \_ BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
