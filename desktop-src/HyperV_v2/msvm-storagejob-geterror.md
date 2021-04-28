---
description: 'Método GetError de la Msvm_StorageJob : recupera el error.'
ms.assetid: 785b83c4-06f4-46b5-81f7-35c6fce16c92
title: Método GetError de la Msvm_StorageJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 00434ef529b7f26755f52833ff6f37310c7dc210
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109603"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a>Método GetError de la clase StorageJob de Msvm \_

Recupera el error.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Error* \[ out\]
</dt> <dd>

Error recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes valores:

<dl> <dt>

**Completado sin error** (0)
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

**Sistema en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Msvm \_ StorageJob**](msvm-storagejob.md)
</dt> </dl>

 

 




