---
description: Consultar la información del clúster desde el host de Hyper-V hasta el invitado.
ms.assetid: 28983984-a2af-4eab-8b1f-2f7d6a3d70ea
title: Método QueryGuestClusterInformation de la clase Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService.QueryGuestClusterInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 36f88441729cc1e6e36bcad9ca84b46049bce2a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540262"
---
# <a name="queryguestclusterinformation-method-of-the-msvm_vssservice-class"></a>Método QueryGuestClusterInformation de la \_ clase VssService de MSVM

Consultar la información del clúster desde el host de Hyper-V hasta el invitado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 QueryGuestClusterInformation(
  [out] Msvm_GuestClusterInformation GuestClusterInformation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*GuestClusterInformation* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, contiene un [**MSVM \_ GuestClusterInformation**](msvm-guestclusterinformation.md) que describe el clúster invitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve un 0 (completado sin errores) o 4096 (trabajo iniciado). de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ VssService**](msvm-vssservice.md)
</dt> </dl>

 

 




