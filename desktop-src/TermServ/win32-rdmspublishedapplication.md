---
title: Win32_RDMSPublishedApplication clase
description: Administra una aplicación publicada.
ms.assetid: 7a529f1d-1aaf-42fb-8469-92d38a7b0ffc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSPublishedApplication clase Servicios de Escritorio remoto
- Win32_RDMSPublishedApplication clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_RDMSPublishedApplication
- Win32_RDMSPublishedApplication.AppAlias
- Win32_RDMSPublishedApplication.PoolName
- Win32_RDMSPublishedApplication.DisplayName
- Win32_RDMSPublishedApplication.ShowInPortal
- Win32_RDMSPublishedApplication.SecurityDescriptor
- Win32_RDMSPublishedApplication.AppPath
- Win32_RDMSPublishedApplication.VirtualPath
- Win32_RDMSPublishedApplication.CommandLineSetting
- Win32_RDMSPublishedApplication.RequiredCommandLine
- Win32_RDMSPublishedApplication.Folder
- Win32_RDMSPublishedApplication.IconPath
- Win32_RDMSPublishedApplication.IconIndex
- Win32_RDMSPublishedApplication.IconContents
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9fe777caf6d1308821fc74e4453839624bcf047811bcfe67275861586a85c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868105"
---
# <a name="win32_rdmspublishedapplication-class"></a>Clase RDMSPublishedApplication de Win32 \_

Administra una aplicación publicada.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSPublishedApplication
{
  string  AppAlias;
  string  PoolName;
  string  DisplayName;
  boolean ShowInPortal;
  string  SecurityDescriptor;
  string  AppPath;
  string  VirtualPath;
  uint32  CommandLineSetting;
  string  RequiredCommandLine;
  string  Folder;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
};
```

## <a name="members"></a>Miembros

La **clase \_ RDMSPublishedApplication de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ RDMSPublishedApplication de Win32** tiene estas propiedades.

<dl> <dt>

**AppAlias**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene y establece el alias de la aplicación.

</dd> <dt>

**AppPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece la ruta de acceso a la aplicación.

</dd> <dt>

**CommandLineSetting**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece la configuración de la línea de comandos para la aplicación.

Esta propiedad puede definirse en uno de los valores siguientes:

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)


</dt> <dd>

No permita argumentos de línea de comandos.

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Permitir** (1)


</dt> <dd>

Permitir argumentos de línea de comandos.

</dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Requerir** (2)


</dt> <dd>

Requerir argumentos de línea de comandos.

</dd> </dl>

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece el nombre para mostrar de la aplicación.

</dd> <dt>

**Carpeta**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece la ruta de acceso a la aplicación.

</dd> <dt>

**IconoContents**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece una matriz que contiene el icono de aplicación.

</dd> <dt>

**IconIndex**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece el índice del icono de aplicación.

</dd> <dt>

**IconPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece la ruta de acceso al icono de esta aplicación.

</dd> <dt>

**PoolName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene y establece el nombre del grupo de aplicaciones de la aplicación.

</dd> <dt>

**RequiredCommandLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece los argumentos de línea de comandos necesarios para la aplicación.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Obtiene y establece el descriptor de seguridad que controla el acceso a la aplicación, en formato de lenguaje de definición de descriptores de seguridad (SDDL).

</dd> <dt>

**ShowInPortal**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si se va a mostrar la aplicación en Terminal Services Web Access (TS Web Access). **TRUE** para mostrar la aplicación en TS Web Access; de lo contrario, **FALSE**.

</dd> <dt>

**VirtualPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Obtiene y establece la ruta de acceso virtual a la aplicación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ cimv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Escritorio remoto Management Services Provider](rdms-api-reference.md)
</dt> </dl>

 

