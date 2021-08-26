---
description: Recupera información sobre una instantánea de VHD dentro de un archivo de conjunto de VHD.
ms.assetid: 43745935-9bc3-4a87-8762-54693b2cdef6
title: Método GetVHDSnapshotInformation de la Msvm_ImageManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: faac0c7b52d8e066ffa658a539a18d6423b50c861b772e536abca2aca010ea47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046635"
---
# <a name="getvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>Método GetVHDSnapshotInformation de la clase \_ Msvm ImageManagementService

Recupera información sobre una instantánea de VHD dentro de un archivo de conjunto de VHD.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetVHDSnapshotInformation(
  [in]  string              VHDSetPath,
  [in]  string              SnapshotIds[],
  [in]  uint32              AdditionalInformation[],
  [out] string              SnapshotInformation[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VHDSetPath* \[ En\]
</dt> <dd>

Ruta de acceso completa que especifica la ubicación del archivo de conjunto de VHD.

</dd> <dt>

*SnapshotIds* \[ En\]
</dt> <dd>

Lista de GUID que representan los identificadores de instantánea de cada instantánea para la que se solicita información. Si este parámetro es NULL, se recuperará la información de todas las instantáneas.

</dd> <dt>

*AdditionalInformation* \[ En\]
</dt> <dd>

Matriz que especifica qué información adicional se debe recopilar sobre cada instantánea de VHD. Cada entrada de la matriz es un tipo de información adicional. Si este parámetro es NULL, no se recuperará información adicional.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Parent_Paths"></span><span id="parent_paths"></span><span id="PARENT_PATHS"></span>

**Rutas de acceso** primarias (2)


</dt> <dd></dd> </dl> </dd> <dt>

*SnapshotInformation* \[ out\]
</dt> <dd>

Si se realiza correctamente, una matriz de información sobre cada instantánea solicitada. Cada elemento es una instancia incrustada de [**Msvm \_ VHDSnapshotInformation.**](msvm-vhdsnapshotinformation.md)

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Referencia al trabajo (puede ser NULL si se completa la tarea).

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
</dt> <dt>

**Archivo no encontrado** (32779)
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

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




