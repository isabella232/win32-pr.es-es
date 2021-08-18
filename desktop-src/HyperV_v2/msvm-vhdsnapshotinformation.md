---
description: Proporciona información sobre una instantánea dentro de un archivo de conjunto de VHD.
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Msvm_VHDSnapshotInformation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c256ee2d3fb277fc98fa440403cf385377d7f64160267ff39a2d905c59f9d3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068455"
---
# <a name="msvm_vhdsnapshotinformation-class"></a>Clase \_ VHDSnapshotInformation de Msvm

Proporciona información sobre una instantánea dentro de un archivo de conjunto de VHD.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a>Miembros

La **clase \_ VHDSnapshotInformation de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ VHDSnapshotInformation de Msvm** tiene estas propiedades.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DATETIME**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora de creación de esta instantánea.

</dd> <dt>

**FilePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del archivo de conjunto de VHD.

</dd> <dt>

**ParentPathsList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de rutas de acceso de archivo que representan todos los archivos de los que depende esta instantánea. Este campo estará vacío a menos que se solicite específicamente. La primera entrada es el elemento primario inmediato del archivo, siendo la última entrada la raíz.

</dd> <dt>

**ResilientChangeTrackingId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de seguimiento de cambios resistente, si lo hay, asociado a esta instantánea.

</dd> <dt>

**SnapshotId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID que identifica de forma única esta instantánea en el archivo de conjunto de VHD.

</dd> <dt>

**SnapshotPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del archivo representado por esta instantánea. Este campo puede estar vacío si no hay ningún archivo asociado a esta instantánea.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




