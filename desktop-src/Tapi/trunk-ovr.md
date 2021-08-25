---
description: Número del tronco sobre el que se enruta la llamada. Este miembro se usa para las llamadas entrantes y salientes.
ms.assetid: e57e1aac-a2f1-42b7-9a0c-c74009a75305
title: Tronco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676721df074d0fe84efbe3256da3e111e94932e0b99d5614d792ddbb0c860ca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872565"
---
# <a name="trunk"></a>Tronco

Número del tronco sobre el que se enruta la llamada. Este miembro se usa para las llamadas entrantes y salientes.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwTrunk** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

**TAPI 3.x: **[**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), llamado con el miembro **CIL \_ TRUNK** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

 

 
