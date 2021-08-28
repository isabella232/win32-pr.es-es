---
description: Representa los generadores de activación registrados mediante una llamada a la función RoRegisterActivationFactories.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (Roapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8efc7d3364f02c11750e6b42ddec6d2a3dee3f83368d277bc979a22ea3a0854a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741602"
---
# <a name="ro_registration_cookie"></a>COOKIE \_ DE REGISTRO DE \_ RO

Representa los generadores de activación registrados mediante una llamada a la [**función RoRegisterActivationFactories.**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a>Comentarios

La [**función RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) devuelve una COOKIE **DE REGISTRO \_ DE \_ RO** cuando se registran generadores de clases activables con Windows Runtime. La [**función RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) usa la cookie para quitar los generadores de clases.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                     |
| Header<br/>                   | <dl> <dt>Roapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
