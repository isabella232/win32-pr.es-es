---
description: Consulta de información del clúster desde el host de Hyper-V al invitado.
ms.assetid: 28983984-a2af-4eab-8b1f-2f7d6a3d70ea
title: Método QueryGuestClusterInformation de la Msvm_VssService clase
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
ms.openlocfilehash: 6c3b58aefb5d821eec114010ea5f878d407d3b7474778b12ca74250bf5f757a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117993783"
---
# <a name="queryguestclusterinformation-method-of-the-msvm_vssservice-class"></a>Método QueryGuestClusterInformation de la clase \_ VssService de Msvm

Consulta de información del clúster desde el host de Hyper-V al invitado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 QueryGuestClusterInformation(
  [out] Msvm_GuestClusterInformation GuestClusterInformation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*GuestClusterInformation* \[ out\]
</dt> <dd>

Si se ejecuta correctamente, contiene [**un \_ elemento GuestClusterInformation de Msvm**](msvm-guestclusterinformation.md) que describe el clúster invitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0 (Completado sin error) o 4096 (trabajo iniciado); De lo contrario, devuelve un error.

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

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está** disponible (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**VssService de Msvm \_**](msvm-vssservice.md)
</dt> </dl>

 

 




