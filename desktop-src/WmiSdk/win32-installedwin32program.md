---
title: Clase \_ InstalledWin32Program de Win32
description: La clase Win32 \_ InstalledWin32Program representa una aplicación Win32 instalada.
ms.assetid: 2eef00da-8597-4852-b4fb-4276d05fd724
keywords:
- Win32_InstalledWin32Program de inventario de aplicaciones y dispositivos
- Win32_InstalledWin32Program clase Application and Device Inventory Provider , descrita
topic_type:
- apiref
api_name:
- Win32_InstalledWin32Program
- Win32_InstalledWin32Program.ProgramId
- Win32_InstalledWin32Program.Name
- Win32_InstalledWin32Program.Vendor
- Win32_InstalledWin32Program.Version
- Win32_InstalledWin32Program.Language
- Win32_InstalledWin32Program.MsiPackageCode
- Win32_InstalledWin32Program.MsiProductCode
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
ms.openlocfilehash: 51cfbf56591bca71f8364d97a9a4adb0d995c4c3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917935"
---
# <a name="win32_installedwin32program-class"></a>Clase \_ InstalledWin32Program de Win32

La **clase Win32 \_ InstalledWin32Program** representa una aplicación Win32 instalada.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_InstalledWin32Program
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string MsiPackageCode;
  string MsiProductCode;
};
```

## <a name="members"></a>Miembros

La **clase \_ InstalledWin32Program de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Win32 \_ InstalledWin32Program** tiene estas propiedades.

<dl> <dt>

**Lenguaje**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Idiomas admitidos para la aplicación Win32 instalada.

</dd> <dt>

**MsiPackageCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El código del paquete MSI, si la aplicación Win32 se instaló mediante una MSI.

</dd> <dt>

**MsiProductCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El código de producto MSI, si la aplicación Win32 se instaló mediante una MSI.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la aplicación Win32 instalada.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identificador único de la aplicación Win32 instalada. Este valor ayuda a **correlacionar Win32 \_ InstalledWin32Program** con [**Win32 \_ InstalledProgramFramework.**](win32-installedprogramframework.md)

</dd> <dt>

**Proveedor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Editor de la aplicación Win32 instalada.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión de la aplicación Win32 instalada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv.mof</dt> </dl> |



 

 





