---
description: La \_ clase de Videoconfiguración de CIM asocia el \_ objeto de configuración VIDEOCONTROLLERRESOLUTION de CIM con el controlador al que se aplica.
ms.assetid: 1f6742ad-ab92-4723-b691-0c3e6c0d82fa
ms.tgt_platform: multiple
title: CIM_VideoSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoSetting
- CIM_VideoSetting.Setting
- CIM_VideoSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37fe8dd03738ae93f391a754caca84564dc6f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659730"
---
# <a name="cim_videosetting-class"></a>\_Clase de Videoconfiguración de CIM

La clase de **\_ videoconfiguración de CIM** asocia el objeto de configuración [**\_ VideoControllerResolution de CIM**](cim-videocontrollerresolution.md) con el controlador al que se aplica.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{1008CCEB-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoSetting : CIM_ElementSetting
{
  CIM_VideoControllerResolution REF Setting;
  CIM_VideoController           REF Element;
};
```

## <a name="members"></a>Miembros

La clase de **\_ videoconfiguración de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ Videoconfiguración de CIM** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ videocontroladora CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")
</dt> </dl>

Un [**\_ videocontrolador de CIM**](cim-videocontroller.md) que describe el controlador de vídeo.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ VideoControllerResolution**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuración")
</dt> </dl>

Un [**\_ VideoControllerResolution de CIM**](cim-videocontrollerresolution.md) que describe las resoluciones, las frecuencias de actualización, el modo de exploración y el número de colores que se pueden establecer para el controlador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase. Para las clases WMI que se derivan de la **\_ configuración** de VIDEODE CIM, vea [clases Win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> </dl>

 

