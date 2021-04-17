---
description: Las posibles razones para una sesión entrante, como la que se transfirió, se enumeran en las \_ constantes LINECALLREASON.
ms.assetid: 94cc1a79-7ce4-47ec-bdd8-ee7f0d9f48ed
title: Motivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b3bfbbaded05853b447d1291a150113c75bbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688136"
---
# <a name="reason"></a>Motivo

Las posibles razones para una sesión entrante, como la que se transfirió, se enumeran en [las \_ constantes LINECALLREASON](./linecallreason--constants.md).

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2. x: **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** miembro dwReason** de *lpCallInfo*)

**TAPI 3. x: **[**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** miembro del \_ motivo de CIL** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))

 

 
