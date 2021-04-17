---
description: Los marcadores de parámetros proporcionan información sobre diversas marcas de estado en relación con una sesión de comunicaciones, por ejemplo, si se debe bloquear la identificación del autor de la llamada. Vea \_ constantes LINECALLPARAMFLAGS para obtener una lista de las marcas definidas por TAPI.
ms.assetid: 30511328-a310-42b7-a81e-3ef2abf586ed
title: Marcas de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3adcb8b430045dc41afea4e7f55e5fa4458530b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687505"
---
# <a name="parameter-flags"></a>Marcas de parámetros

Los marcadores de parámetros proporcionan información sobre diversas marcas de estado en relación con una sesión de comunicaciones, por ejemplo, si se debe bloquear la identificación del autor de la llamada. Vea [ \_ constantes LINECALLPARAMFLAGS](./linecallparamflags--constants.md) para obtener una lista de las marcas definidas por TAPI.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (miembro **dwCallParamFlags** de *lpCallInfo*).

**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL \_ CALLPARAMSFLAGS** member of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
