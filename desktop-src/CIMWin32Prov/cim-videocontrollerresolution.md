---
description: La clase CIM VideoControllerResolution representa los distintos modos de vídeo que puede admitir un \_ controlador de vídeo.
ms.assetid: 954ac3fe-9777-460c-8929-853f19379256
ms.tgt_platform: multiple
title: CIM_VideoControllerResolution clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoControllerResolution
- CIM_VideoControllerResolution.Caption
- CIM_VideoControllerResolution.Description
- CIM_VideoControllerResolution.SettingID
- CIM_VideoControllerResolution.HorizontalResolution
- CIM_VideoControllerResolution.MaxRefreshRate
- CIM_VideoControllerResolution.MinRefreshRate
- CIM_VideoControllerResolution.NumberOfColors
- CIM_VideoControllerResolution.RefreshRate
- CIM_VideoControllerResolution.ScanMode
- CIM_VideoControllerResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d448d92d79163bc6a4e1056e88434081c5878159
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968868"
---
# <a name="cim_videocontrollerresolution-class"></a>Cim \_ VideoControllerResolution (clase)

La **clase CIM \_ VideoControllerResolution** representa los distintos modos de vídeo que puede admitir un controlador de vídeo. Los modos de vídeo se definen mediante las posibles resoluciones horizontales y verticales, la frecuencia de actualización, el modo de examen y el número de configuraciones de color compatibles con un controlador. Las resoluciones reales en uso son los valores especificados en el [**objeto \_ VideoController de CIM.**](cim-videocontroller.md)

El hardware que no es compatible con Windows modelo de controlador de pantalla (WDDM) devuelve valores de propiedad inexactos para instancias de esta clase.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEA-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoControllerResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint64 NumberOfColors;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a>Members

La **clase CIM \_ VideoControllerResolution** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ VideoControllerResolution** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DmTF \| Monitor Resolutions \| 002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")
</dt> </dl>

Resolución horizontal, en píxeles.

</dd> <dt>

**MaxRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Monitor Resolutions \| 002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")
</dt> </dl>

Frecuencia de actualización máxima cuando se admite un intervalo de tarifas en las resoluciones especificadas, en hercios.

</dd> <dt>

**MinRefreshRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Monitor Resolutions \| 002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")
</dt> </dl>

Frecuencia de actualización mínima cuando se admite un intervalo de tarifas en las resoluciones especificadas, en hercios.

</dd> <dt>

**NumberOfColors**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")
</dt> </dl>

Número de colores admitidos en la resolución actual.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Monitor Resolutions \| 002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")
</dt> </dl>

Frecuencia de actualización, en hercios. Si se admite un intervalo de tarifas, use las propiedades **MinRefreshRate** y **MaxRefreshRate** y establezca esta propiedad en 0.

</dd> <dt>

**ScanMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Resoluciones del monitor DMTF \| \| 002.5")
</dt> </dl>

Modo de examen en el que funciona el controlador.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (3)


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Operación sin entrelazado** (4)


</dt> <dd>

Operación no entrelazada

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Operación entrelazada** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador que actúa como parte de la clave de la instancia actual.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Monitor Resolutions \| 002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")
</dt> </dl>

Resolución vertical del controlador, en píxeles.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI implementa la **clase \_ CIM VideoControllerResolution.** La **clase CIM \_ VideoControllerResolution** es una clase dinámica.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

Tenga en cuenta que esta clase es una clase base. Si está intentando acceder al controlador de vídeo a través de WMI, puede usar [**\_ VideoController win32**](win32-videocontroller.md) en su lugar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> </dl>

 

