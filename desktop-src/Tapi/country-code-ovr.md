---
description: El código de país o región solo es relevante cuando el tipo de dirección es LINEADDRESSTYPE \_ PHONENUMBER. Identifica un área del mundo.
ms.assetid: d838c2ac-4ee3-4314-8573-deed6c7430e3
title: Código de país o región
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5557e4d67b701fda2aa05ad81686ae474b172063
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073508"
---
# <a name="country-or-region-code"></a>Código de país o región

El código de país o región solo es relevante cuando el tipo de dirección es LINEADDRESSTYPE \_ PHONENUMBER. Identifica un área del mundo.

Todos los proveedores de servicios que admiten el uso de números de teléfono deben admitir el uso de esta información.

**TAPI 2.x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCountryCode** member of *lpCallInfo*).

**TAPI 3.x:** Vea [**ITCallInfo::get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**miembro \_ CIL COUNTRYCODE** de [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)).

 

 
