---
description: Detiene el servicio de invitado.
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: Msvm_GuestService::StopService (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f67234a09ad150f2f039a57b321797e03444c75defe2e83cfd06b60de320a664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050395"
---
# <a name="msvm_guestservicestopservice-method"></a>Método Msvm \_ GuestService::StopService

Detiene el servicio de invitado.

## <a name="syntax"></a>Sintaxis


```C++
uint32 StopService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                             | Descripción         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Completado sin error**</dt> <dt>0</dt> </dl> | Correcto.<br/> |
| <dl> <dt>**No compatible**</dt> <dt>con 1</dt> </dl>           |                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

 




