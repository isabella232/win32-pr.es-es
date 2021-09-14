---
description: La información del usuario es un búfer que se puede transmitir desde un extremo de una conexión a otro. Esta información es específica del estándar ISDN Q.931. Consulte la documentación de los proveedores de servicios sobre el significado y el uso de estos datos.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Información del usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073460"
---
# <a name="user-user-information"></a>Información del usuario

La información del usuario es un búfer que se puede transmitir desde un extremo de una conexión a otro. Esta información es específica del estándar ISDN Q.931. Consulte la documentación del proveedor de servicios sobre el significado y el uso de estos datos.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** y **dwCallDataOffset** miembros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

**TAPI 3.x: **[**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), llamado con el miembro **\_ CIB USERUSERINFO** de [**CALLINFO \_ BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
