---
description: Recupera el objeto de error para el trabajo de migración, si existe uno.
ms.assetid: 83a68ded-086a-42d9-b76d-e46af70d9b43
title: Método GetError de la Msvm_MigrationJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 014c7ea203525247ede420dddd630f2b540305e71bcedf1318198a3cd98aeaef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392973"
---
# <a name="geterror-method-of-the-msvm_migrationjob-class"></a>Método GetError de la clase \_ MigrationJob de Msvm

Recupera el objeto de error para el trabajo de migración, si existe uno. Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve un [**objeto \_ Cim Error.**](/previous-versions//cc150671(v=vs.85)) Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque un cliente ha terminado el trabajo, se devuelve una instancia **\_ de error** de CIM.

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

Si el estado operativo del trabajo no es 2 (Correcto), este método devuelve una instancia incrustada de la clase Error de [**Msvm, \_**](msvm-error.md) en formato CIM-XML. Si el estado operativo del trabajo es 2 (Correcto), se **devuelve Null.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

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
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Msvm \_ MigrationJob**](msvm-migrationjob.md)
</dt> </dl>

 

