---
description: 'Método GetErrorEx de la Msvm_CollectionReferencePointExportJob clase : recupera información adicional sobre un error.'
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Método GetErrorEx de la Msvm_CollectionReferencePointExportJob clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3b84c41776c081c302078773d9402145b0fe41e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112093"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a>Método GetErrorEx de la clase \_ CollectionReferencePointExportJob de Msvm

Recupera información adicional sobre un error. Cuando el trabajo se está ejecutando o ha finalizado sin errores, **GetErrorEx** no devuelve ninguna [**instancia de \_ error de Msvm.**](msvm-error.md) Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque un cliente ha finalizado el trabajo, **GetErrorEx** devuelve una o varias instancias de error de **\_ Msvm.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Errores* \[ out\]
</dt> <dd>

Si el estado operativo del trabajo no es "Correcto", este parámetro devuelve una matriz de instancias de error de [**Msvm. \_**](msvm-error.md) De lo contrario, si el trabajo es "OK", este parámetro contiene **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve uno de los siguientes valores de error:

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
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




