---
title: Win32_TSVmMetadataAssociation clase
description: Representa una asociación entre una Escritorio remoto virtual y sus propiedades de metadatos.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataAssociation clase Servicios de Escritorio remoto
- Win32_TSVmMetadataAssociation clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe3389bb03c9e3f33a2cc3e33450318b68171f7ac35fffeaaa3976cb5ae3a33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119420005"
---
# <a name="win32_tsvmmetadataassociation-class"></a>Clase \_ TSVmMetadataAssociation de Win32

Representa una asociación entre una Escritorio remoto virtual y sus propiedades de metadatos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSVmMetadataAssociation de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TSVmMetadataAssociation de Win32** tiene estas propiedades.

<dl> <dt>

**MetadataItem**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Instancia de la clase [**\_ TSVmMetadataItem de Win32**](win32-tsvmmetadataitem.md) que representa los metadatos de la máquina virtual.

</dd> <dt>

**TSVm**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Win32 \_ TSVm**](win32-tsvm.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Instancia de la [**clase \_ TSVm Win32**](win32-tsvm.md) que representa la máquina virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                             |
| Espacio de nombres<br/>                | \\TerminalServices cimv2 \\ raíz<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

