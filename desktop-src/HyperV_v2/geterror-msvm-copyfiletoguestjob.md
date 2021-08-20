---
description: 'Msvm_CopyFileToGuestJob::GetError: recupera el objeto de error para el trabajo, si existe uno.'
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: Msvm_CopyFileToGuestJob::GetError (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c5ef377dfd655c21137bbb0c7d34dfcb047054652afe162d75f2400acee045ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149808"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a>Método Msvm \_ CopyFileToGuestJob::GetError

Recupera el objeto de error para el trabajo, si existe uno. Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve un objeto [**\_ cim error.**](/previous-versions//cc150671(v=vs.85)) Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque un cliente ha terminado el trabajo, se devuelve una instancia **\_ de error** de CIM.

## <a name="syntax"></a>Sintaxis


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Error* \[ out\]
</dt> <dd>

Si el estado operativo del trabajo no es 2 (Correcto), este método devuelve una instancia incrustada de la clase Error de [**Msvm, \_**](msvm-error.md) en formato CIM-XML. Si el estado operativo del trabajo es 2 (correcto), **se devuelve Null.**

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

