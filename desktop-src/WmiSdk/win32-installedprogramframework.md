---
title: Clase InstalledProgramFramework de Win32 \_
description: La clase Win32 InstalledProgramFramework representa un marco de tecnología en el que se compila o usa una instancia \_ \_ de Win32 InstalledWin32Program en tiempo de ejecución.
ms.assetid: bb5c18c7-ec71-4579-8190-942de4fccd9e
keywords:
- Win32_InstalledProgramFramework de inventario de aplicaciones y dispositivos
- Win32_InstalledProgramFramework clase Application and Device Inventory Provider , descrita
topic_type:
- apiref
api_name:
- Win32_InstalledProgramFramework
- Win32_InstalledProgramFramework.FrameworkName
- Win32_InstalledProgramFramework.FrameworkPublisher
- Win32_InstalledProgramFramework.FrameworkVersion
- Win32_InstalledProgramFramework.FrameworkVersionActual
- Win32_InstalledProgramFramework.ProgramId
- Win32_InstalledProgramFramework.IsPrivate
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
ms.openlocfilehash: 3e447544dbfdebd6e4f4dd12752171089b8da041
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917928"
---
# <a name="win32_installedprogramframework-class"></a>Clase InstalledProgramFramework de Win32 \_

La **clase Win32 \_ InstalledProgramFramework** representa un marco de tecnología en el que se compila o usa una instancia [**de \_ Win32 InstalledWin32Program**](win32-installedwin32program.md) en tiempo de ejecución. Los marcos que esta clase puede notificar actualmente son OpenSSL, Visual Basic, Visual C++ .Net, Visual C++, Java (solo detecta los archivos binarios en tiempo de ejecución de Java) y CLR.

> [!Note]  
> El conjunto de marcos que esta clase puede detectar se puede actualizar con el tiempo.

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_InstalledProgramFramework
{
  string  FrameworkName;
  string  FrameworkPublisher;
  string  FrameworkVersion;
  string  FrameworkVersionActual;
  string  ProgramId;
  boolean IsPrivate;
};
```

## <a name="members"></a>Miembros

La **clase \_ InstalledProgramFramework de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ InstalledProgramFramework de Win32** tiene estas propiedades.

<dl> <dt>

**FrameworkName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Nombre del marco de trabajo del que depende la aplicación identificada **por ProgramId.**

</dd> <dt>

**FrameworkPublisher**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Publicador del marco.

</dd> <dt>

**FrameworkVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

La versión del marco de trabajo de la que depende la aplicación.

</dd> <dt>

**FrameworkVersionActual**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

La versión del marco que la aplicación usa realmente en tiempo de ejecución, si se puede detectar el marco.

</dd> <dt>

**IsPrivate**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

TRUE si la aplicación agrupa una copia privada del marco.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identificador único de la [**instancia de Win32 \_ InstalledWin32Program,**](win32-installedwin32program.md) al que están asociados los datos del marco.

</dd> </dl>

## <a name="requirements"></a>Requisitos



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv.mof</dt> </dl> |



 

 





