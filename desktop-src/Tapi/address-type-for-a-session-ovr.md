---
description: El tipo de dirección identifica el formato necesario para una dirección. Por ejemplo, si el tipo es LINEADDRESSTYPE \_ PHONENUMBER, la dirección que se usa para marcar en la sesión debe ser un número de teléfono.
ms.assetid: bea48bde-927a-400a-9a7e-a77e30ba35eb
title: Tipo de dirección de una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42499c19a08d67ce2e6e7ea5741053686c32aa6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677954"
---
# <a name="address-type-for-a-session"></a>Tipo de dirección de una sesión

El [**tipo de dirección**](lineaddresstype--constants.md) identifica el formato necesario para una dirección. Por ejemplo, si el tipo es LINEADDRESSTYPE \_ PHONENUMBER, la dirección que se usa para marcar en la sesión debe ser un número de teléfono.

Un dispositivo y un proveedor de servicios determinados admiten uno o varios tipos de direcciones. Consulte los [tipos de direcciones de un dispositivo](address-type-ovr.md) para obtener información sobre cómo sondear un dispositivo en busca de los formatos de dirección que admite.

**TAPI 2. x:** Vea [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), miembro **dwAddressType** de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).

**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), llamado con el miembro de CIL **\_ CALLERIDADDRESSTYPE**, **CIL \_ CALLEDIDADDRESSTYPE** o **CIL \_ CONNECTEDIDADDRESSTYPE** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).

 

 
