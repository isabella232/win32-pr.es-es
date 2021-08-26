---
description: Esta clase representa la asociación entre un sistema operativo y la configuración de autochk que se aplica a los discos de la máquina. Tenga en cuenta que la configuración está asociada al sistema operativo en lugar del sistema informático, ya que puede haber uno o varios sistemas operativos instalados en la máquina, cada uno con su propia configuración de autochk.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Win32_OperatingSystemAutochkSetting clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cfa6e90828935dda8aa163967985813526042b8800f91cb01825fbd158f8a63d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972545"
---
# <a name="win32_operatingsystemautochksetting-class"></a>Clase \_ OperatingSystemAutochkSetting de Win32

Esta clase representa la asociación entre un sistema operativo y la configuración de autochk que se aplica a los discos de la máquina. Tenga en cuenta que la configuración está asociada al sistema operativo en lugar del sistema informático, ya que puede haber uno o varios sistemas operativos instalados en la máquina, cada uno con su propia configuración de autochk.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a>Miembros

La **clase \_ OperatingSystemAutochkSetting de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ OperatingSystemAutochkSetting de Win32** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ OperatingSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**key**](../wmisdk/key-qualifier.md)
</dt> </dl>

Por determinar

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ AutochkSetting**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**key**](../wmisdk/key-qualifier.md)
</dt> </dl>

Por determinar

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ElementSetting**](cim-elementsetting.md)
</dt> </dl>

 

 
