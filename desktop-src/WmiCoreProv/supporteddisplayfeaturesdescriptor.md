---
description: Representa las características de visualización admitidas del monitor.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: SupportedDisplayFeaturesDescriptor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a9e71eeda4ab47cba5e88a548421c89815b7d0d87d511709b9a73573e2582077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321541"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a>SupportedDisplayFeaturesDescriptor (clase)

**SupportedDisplayFeaturesDescriptor representa** las características de visualización admitidas del monitor. La información de esta clase corresponde a los datos del estándar Definición de entrada de vídeo del estándar Detección de pantalla extendida mejorada (E-EDID) de Video Electronics Standard Association (VESA).

## <a name="syntax"></a>Sintaxis

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a>Miembros

La **clase SupportedDisplayFeaturesDescriptor** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SupportedDisplayFeaturesDescriptor** tiene estas propiedades.

<dl> <dt>

**ActiveOffSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Compatibilidad con apagado activo y muy baja potencia. La pantalla consume menos energía cuando recibe una señal de tiempo que está fuera del intervalo operativo activo declarado. La pantalla volverá al funcionamiento normal si la señal de tiempo vuelve al intervalo de funcionamiento normal. Ejemplos de señales de control de tiempo fuera del intervalo de funcionamiento normal son ninguna señal de sincronización o ninguna señal DE.

</dd> <dt>

**Displaytype**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de pantalla para el monitor. En la tabla siguiente se enumeran los valores posibles.



| Valor                                                                              | Significado                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Pantalla monocromática/escala de grises<br/> |
| <dl> <dt>1 (0x1)</dt> </dl> | Pantalla de color RGB<br/>            |
| <dl> <dt>2 (0x2)</dt> </dl> | Pantalla de rgb no rgb<br/>   |



 

</dd> <dt>

**GTFSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla tiene compatibilidad con GTF. Si **es True,** la pantalla admite intervalos basados en el estándar GTF mediante valores de parámetro GTF predeterminados.

</dd> <dt>

**HasPreferredTimingMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla tiene un modo de control de tiempo preferido. Si **es True,** el primer bloque de control de tiempo detallado contiene el modo de control de tiempo preferido del monitor. EDID v.1.3 y superior requiere el uso del modo de control de tiempo preferido.

</dd> <dt>

**sRGBSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es True,** la pantalla admite sRGB.

</dd> <dt>

**StandbySupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla admite la señal de administración de energía de pantalla VESA (DPMS) en espera. Si **es True,** se admite el modo en espera de DPMS.

</dd> <dt>

**SuspendSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la pantalla admite la suspensión de la señalización de administración de energía de la pantalla VESA (DPMS). Si **es True,** se admite la suspensión de DPMS.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




