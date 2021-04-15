---
description: El tipo de medio (o modo) describe el tipo de información que se intercambia, como la voz interactiva. Una sesión de comunicaciones determinada puede incluir varios tipos de medios.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Tipo de medio para una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc8f5c7743a5d5a85003c99b2ac1abbf13f54168
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547374"
---
# <a name="media-type-for-a-session"></a>Tipo de medio para una sesión

El tipo de medio (o modo) describe el tipo de información que se intercambia, como la voz interactiva. Una sesión de comunicaciones determinada puede incluir varios tipos de medios.

Los proveedores de servicios exponen a TAPI y a las aplicaciones el tipo de medios o los tipos que admiten. Consulte información general sobre el [tipo de medios](media-type-ovr.md) de dispositivo para obtener información sobre la adquisición de estos datos.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**line \_ MONITORMEDIA**](./line-monitormedia.md) Message, [LINEMEDIAMODE \_ constantes](./linemediamode--constants.md).

**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent:: get \_ cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (devuelve [**CALLINFOCHANGE \_ causa**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) de un de **CIC \_**), [TAPIMEDIATYPE \_ constantes](tapimediatype--constants.md).

 

 
