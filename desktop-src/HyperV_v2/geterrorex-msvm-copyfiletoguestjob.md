---
description: 'Msvm_CopyFileToGuestJob::GetErrorEx: recupera los objetos de error para el trabajo, si existe alguno.'
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: Msvm_CopyFileToGuestJob::GetErrorEx (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 81a570c42457257212e83f9c0c034c4a390e4c04
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109673"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a>Método Msvm \_ CopyFileToGuestJob::GetErrorEx

Recupera los objetos de error del trabajo, si existe alguno. Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna [**instancia de \_ error de Msvm.**](msvm-error.md) Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque un cliente ha finalizado el trabajo, se devuelven una o varias instancias de error de **Msvm. \_**

## <a name="syntax"></a>Sintaxis


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Errores* \[ out\]
</dt> <dd>

Si el estado operativo del trabajo no es 2 (correcto), este método devuelve una o varias instancias incrustadas de la clase Error de [**Msvm, \_**](msvm-error.md) en formato CIM-XML, que representan los errores encontrados en el trabajo. Si el estado operativo del trabajo es 2 (correcto), se **devuelve Null.**

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
| Cliente mínimo compatible<br/> | Windows 8.1 solo \[ aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




