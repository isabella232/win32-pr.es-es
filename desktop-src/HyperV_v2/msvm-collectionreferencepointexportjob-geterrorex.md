---
description: Recupera información adicional sobre un error.
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Método GetErrorEx de la clase Msvm_CollectionReferencePointExportJob
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
ms.openlocfilehash: c056f7c8a05d8d06d136219fb55699ed5e146bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669943"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a>Método GetErrorEx de la \_ clase CollectionReferencePointExportJob de MSVM

Recupera información adicional sobre un error. Cuando el trabajo se está ejecutando o ha finalizado sin errores, **GetErrorEx** no devuelve ninguna instancia de [**\_ error MSVM**](msvm-error.md) . Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, **GetErrorEx** devuelve una o varias instancias de **\_ error MSVM** .

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Errores* \[ de enuncia\]
</dt> <dd>

Si el estado operativo del trabajo no es "correcto", este parámetro devuelve una matriz de instancias [**de \_ error de MSVM**](msvm-error.md) . De lo contrario, si el trabajo es "OK", este parámetro contiene **null**.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




