---
description: Representa los generadores de activación que se registran mediante una llamada a la función RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705664"
---
# <a name="ro_registration_cookie"></a>\_cookie de registro de ro \_

Representa los generadores de activación que se registran mediante una llamada a la función [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) .


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Observaciones

La función [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) devuelve una **\_ \_ cookie de registro de ro** cuando se registran generadores de clases activables con el Windows Runtime. La función [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) usa la cookie para quitar los generadores de clases.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Roapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
