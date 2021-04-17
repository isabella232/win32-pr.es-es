---
description: Recupera información acerca de un archivo de VHD set.
ms.assetid: efdfd4c6-b762-4369-add3-e152652c6802
title: Método GetVHDSetInformation de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSetInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cdcf4a354e6d6b47b6a67c071daf8883905f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686941"
---
# <a name="getvhdsetinformation-method-of-the-msvm_imagemanagementservice-class"></a>Método GetVHDSetInformation de la \_ clase ImageManagementService de MSVM

Recupera información acerca de un archivo de VHD set.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetVHDSetInformation(
  [in]  string              VHDSetPath,
  [in]  uint32              AdditionalInformation[],
  [out] string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VHDSetPath* \[ de\]
</dt> <dd>

Una ruta de acceso completa que especifica la ubicación del archivo de VHD set.

</dd> <dt>

*AdditionalInformation* \[ de\]
</dt> <dd>

Una matriz que especifica la información adicional que se debe recopilar sobre el archivo de VHD set. Cada entrada de la matriz es un tipo de información adicional. Si este parámetro es NULL, no se recuperará información adicional.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Paths"></span><span id="paths"></span><span id="PATHS"></span>

**Rutas** de acceso (2)


</dt> <dd></dd> </dl> </dd> <dt>

*Información* \[ de enuncia\]
</dt> <dd>

Si se realiza correctamente, este objeto contiene la información del archivo de conjunto de VHD solicitado. Se trata de una instancia incrustada de [**MSVM \_ VHDSetInformation**](msvm-vhdsetinformation.md).

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Referencia al trabajo (puede ser null si se ha completado la tarea).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los siguientes valores:

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
</dt> <dt>

**No se encontró el archivo** (32779)
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

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




