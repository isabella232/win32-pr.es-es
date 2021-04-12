---
description: Número del tronco sobre el que se enruta la llamada. Este miembro se utiliza para las llamadas entrantes y salientes.
ms.assetid: e57e1aac-a2f1-42b7-9a0c-c74009a75305
title: Tronco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4afea1387c6d43dc4d9a2f5a6a12f260a8daeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278095"
---
# <a name="trunk"></a>Tronco

Número del tronco sobre el que se enruta la llamada. Este miembro se utiliza para las llamadas entrantes y salientes.

No todos los proveedores de servicios admiten el uso de esta información.

* * TAPI 2. x: * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwTrunk** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), llamado con el miembro **\_ troncal de CIL** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

 

 
