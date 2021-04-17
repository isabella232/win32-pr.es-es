---
description: Recupera un error debido a un trabajo con error.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: Método GetError de la clase CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aa9ed87f2d484286d91d14c4183d2ce3b6f41cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687047"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a>Método GetError de la \_ clase ConcreteJob de CIM

Recupera un error debido a un trabajo con error. Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna instancia de [**\_ error de CIM**](cim-error.md) . Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, se devuelve una instancia de **\_ error de CIM** .

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Error* \[ de enuncia\]
</dt> <dd>

Devuelve una instancia de [**\_ error de CIM**](cim-error.md) si el valor de **OperationalStatus** en el trabajo no es "OK"; en caso contrario, devuelve **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error no especificado** (2)
</dt> <dt>

**Tiempo de espera** (3)
</dt> <dt>

**Error** (4)
</dt> <dt>

**Parámetro no válido** (5)
</dt> <dt>

**Acceso denegado** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_CONCRETEJOB CIM**](cim-concretejob.md)
</dt> </dl>

 

 




