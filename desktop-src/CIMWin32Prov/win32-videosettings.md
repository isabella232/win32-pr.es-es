---
description: La \_ clase WMI de la Asociación Win32 Videosettings relaciona una configuración de vídeo y un controlador de vídeo que se puede aplicar a ella.
ms.assetid: 0cc42352-0a89-434d-a8b6-230c677de49c
ms.tgt_platform: multiple
title: Win32_VideoSettings (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoSettings
- Win32_VideoSettings.Setting
- Win32_VideoSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38e949b6b6501dc51b39448d72e6bf61f37fbecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659430"
---
# <a name="win32_videosettings-class"></a>\_Clase Win32 Videosettings

La [clase WMI](../wmisdk/retrieving-a-class.md) de la Asociación **Win32 \_ videosettings** relaciona una configuración de vídeo y un controlador de vídeo que se puede aplicar a ella.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEE-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoSettings : CIM_VideoSetting
{
  CIM_VideoControllerResolution REF Setting;
  Win32_VideoController         REF Element;
};
```

## <a name="members"></a>Miembros

La clase **Win32 \_ videosettings** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **Win32 \_ videosettings** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ videocontroladora Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ videocontroller")
</dt> </dl>

Un [**\_ videocontrolador de Win32**](win32-videocontroller.md) que contiene las propiedades del controlador de vídeo en el que se puede usar una configuración de vídeo.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ VideoControllerResolution**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("configuración"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ VideoControllerResolution")
</dt> </dl>

[**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) que contiene la configuración que se puede aplicar al controlador de vídeo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **Win32 \_ videosettings** se deriva de [**la \_ configuración**](cim-videosetting.md)de videoconfiguración de CIM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Videoconfiguración de CIM \_**](cim-videosetting.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
