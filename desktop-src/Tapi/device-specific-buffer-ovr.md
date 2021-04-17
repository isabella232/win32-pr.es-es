---
description: Los búferes específicos del dispositivo pueden formar parte de una implementación de proveedores de servicios de operaciones extendidas. El proveedor de servicios define el significado de estos búferes.
ms.assetid: 5783f892-ec11-4340-afad-44f2ef55fd18
title: Búfer específico del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628ee93e4f88fc733e744b3c52af3c0a1c31ecf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677813"
---
# <a name="device-specific-buffer"></a>Búfer específico del dispositivo

Los búferes específicos del dispositivo pueden formar parte de la implementación de operaciones extendidas de un proveedor de servicios. El proveedor de servicios define el significado de estos búferes.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwDevSpecificSize** y **dwDevSpecificOffset** miembros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)).

**TAPI 3. x:** Vea [**ITCallInfo:: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer) (**CIB \_ DEVSPECIFICBUFFER** member of [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)).

 

 
