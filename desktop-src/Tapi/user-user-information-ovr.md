---
description: La información de usuario es un búfer que se puede transmitir desde un extremo de una conexión a otra. Esta información es específica del estándar de p. 931 de ISDN. Consulte la documentación de los proveedores de servicios sobre el significado y el uso de estos datos.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Información de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546299"
---
# <a name="user-user-information"></a>Información de usuario

La información de usuario es un búfer que se puede transmitir desde un extremo de una conexión a otra. Esta información es específica del estándar de p. 931 de ISDN. Consulte la documentación del proveedor de servicios sobre el significado y el uso de estos datos.

No todos los proveedores de servicios admiten el uso de esta información.

* * TAPI 2. x: * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** y **dwCallDataOffset** miembros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

* * TAPI 3. x: * *[**ITCallInfo:: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), llamado con el miembro **CIB \_ USERUSERINFO** del [**\_ búfer CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo:: ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
