---
description: Las marcas de parámetros ofrecen información sobre diversas marcas de estado relativas a una sesión de comunicaciones, como si se debe bloquear la identificación del autor de la llamada. Vea LINECALLPARAMFLAGS Constants (Constantes LINECALLPARAMFLAGS) para \_ obtener una lista de marcas definidas por TAPI.
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: Marcas de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf663ea4ff6121f3e130f9c2a2e4c3c1f86f8611be8cc3fef3762adc535e84bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959865"
---
# <a name="parameter-flags"></a>Marcas de parámetros

Las marcas de parámetros ofrecen información sobre diversas marcas de estado relativas a una sesión de comunicaciones, como si se debe bloquear la identificación del autor de la llamada. Vea [LINECALLPARAMFLAGS \_ Constants (Constantes LINECALLPARAMFLAGS)](./linecallparamflags--constants.md) para obtener una lista de marcas definidas por TAPI.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) **(miembro dwCallParamFlags** de *lpCallInfo).*

**TAPI 3.x:** Vea [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**miembro CIL \_ CALLPARAMSFLAGS** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
