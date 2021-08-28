---
title: Clase \_ InstalledStoreProgram de Win32
description: La clase InstalledStoreProgram de Win32 \_ representa una aplicación Windows store instalada.
ms.assetid: 154c19c7-f2e5-48bd-b05b-3022e45f2aa4
keywords:
- Win32_InstalledStoreProgram de inventario de aplicaciones y dispositivos
- Win32_InstalledStoreProgram clase Application and Device Inventory Provider , descrita
topic_type:
- apiref
api_name:
- Win32_InstalledStoreProgram
- Win32_InstalledStoreProgram.ProgramId
- Win32_InstalledStoreProgram.Name
- Win32_InstalledStoreProgram.Vendor
- Win32_InstalledStoreProgram.Version
- Win32_InstalledStoreProgram.Language
- Win32_InstalledStoreProgram.Architecture
api_location:
- Root\CIMv2
api_type:
- Schema
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 613baba9990da8403417aa4f8639ed7e9b5a7a5f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917943"
---
# <a name="win32_installedstoreprogram-class"></a>Clase \_ InstalledStoreProgram de Win32

La **clase \_ InstalledStoreProgram de Win32 representa** una aplicación Windows store instalada.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_InstalledStoreProgram
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string Architecture;
};
```

## <a name="members"></a>Miembros

La **clase \_ InstalledStoreProgram de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ InstalledStoreProgram de Win32** tiene estas propiedades.

<dl> <dt>

**Arquitectura**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Arquitecturas de procesador admitidas para la Windows de almacenamiento.

</dd> <dt>

**Lenguaje**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los idiomas admitidos para la Windows de almacenamiento.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la aplicación Windows almacén.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identificador único de la aplicación Windows almacén.

</dd> <dt>

**Proveedor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Publicador de la aplicación Windows store.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión de la aplicación Windows store.

</dd> </dl>

## <a name="requirements"></a>Requisitos



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv.mof</dt> </dl> |



 

 





