---
description: Recupera un error debido a un trabajo con errores.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: Método GetError de la CIM_ConcreteJob clase
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
ms.openlocfilehash: 0b43d433bf9d2a3967efcc4a2e927d3bf687ebfa5ac67d7c7e34c48c34832c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813271"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a>Método GetError de la clase \_ ConcreteJob de CIM

Recupera un error debido a un trabajo con errores. Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna [**instancia de \_ error CIM.**](cim-error.md) Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque un cliente ha finalizado el trabajo, se devuelve una instancia **\_ de error** de CIM.

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

Devuelve una [**instancia \_ de error cim**](cim-error.md) si **operationalstatus** en el trabajo no es "correcto"; de lo contrario, devuelve **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error no especificado** (2)
</dt> <dt>

**Tiempo de** espera (3)
</dt> <dt>

**Error** (4)
</dt> <dt>

**Parámetro no válido** (5)
</dt> <dt>

**Acceso denegado** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ConcreteJob**](cim-concretejob.md)
</dt> </dl>

 

 




