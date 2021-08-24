---
description: Proporciona información sobre un archivo de conjunto de VHD.
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Msvm_VHDSetInformation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8cef737c02629ac0a1a026a459adf6eb7060e0dbdf8c0f9ecb20c66fce1259e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789435"
---
# <a name="msvm_vhdsetinformation-class"></a>Clase \_ VHDSetInformation de Msvm

Proporciona información sobre un archivo de conjunto de VHD.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a>Miembros

La **clase \_ VHDSetInformation de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ VHDSetInformation de Msvm** tiene estas propiedades.

<dl> <dt>

**AllPaths**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de todos los archivos incluidos en el archivo de conjunto de VHD, incluidos los archivos sin referencia y los elementos raíz del disco duro virtual raíz. Todos los archivos enumerados después del disco duro virtual raíz no están administrados por este archivo de conjunto de discos duros virtuales. Este campo puede estar vacío si esta información no se solicitó específicamente.

</dd> <dt>

**Ruta de acceso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del archivo de conjunto de VHD.

</dd> <dt>

**SnapshotIdList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de GUID que representan todas las instantáneas contenidas en este archivo de conjunto de discos duros virtuales.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




