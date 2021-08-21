---
description: El tipo de medio (o modo) describe el tipo de información que se intercambia, como la voz interactiva. Una sesión de comunicaciones determinada puede implicar varios tipos de medios.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Tipo de medio para una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974935baf17652c0376386eea63028ba04eeb886d1f48eba1aaf7f8469a9c374
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002883"
---
# <a name="media-type-for-a-session"></a>Tipo de medio para una sesión

El tipo de medio (o modo) describe el tipo de información que se intercambia, como la voz interactiva. Una sesión de comunicaciones determinada puede implicar varios tipos de medios.

Los proveedores de servicios exponen a TAPI y a las aplicaciones el tipo de medio o los tipos que admiten. Consulte la introducción al [tipo de medio de](media-type-ovr.md) dispositivo para obtener información sobre la adquisición de estos datos.

**TAPI 2.x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia,**](/windows/win32/api/tapi/nf-tapi-linemonitormedia) [**LINE \_ MONITORMEDIA**](./line-monitormedia.md) message, [LINEMEDIAMODE \_ Constants](./linemediamode--constants.md).

**TAPI 3.x:** Vea [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) con **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfo::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) con **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent::get \_ Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (devuelve [**CALLINFOCHANGE \_ CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) de **CIC \_ MEDIATYPE**), [TAPIMEDIATYPE \_ Constants](tapimediatype--constants.md).

 

 
