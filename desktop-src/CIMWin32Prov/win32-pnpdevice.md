---
description: La clase WMI de asociación PnPDevice win32 relaciona un dispositivo (conocido Administrador de configuración como PNPEntity) y la función \_ que realiza.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Win32_PnPDevice clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a136c86c0fd0744c555af2071943d99ca8569a33ce9c59d9d22191c4a78d2a32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972045"
---
# <a name="win32_pnpdevice-class"></a>Clase PnPDevice de Win32 \_

La clase [WMI](../wmisdk/retrieving-a-class.md) de asociación **\_ PnPDevice win32** relaciona un dispositivo (conocido por Administrador de configuración como PNPEntity) y la función que realiza. Su función se representa mediante una subclase del dispositivo lógico que describe su uso. Por ejemplo, una [**instancia de Win32 \_ Keyboard**](win32-keyboard.md) o [**Win32 \_ DiskDrive.**](win32-diskdrive.md) Ambos objetos a los que se hace referencia representan el mismo dispositivo del sistema subyacente; Los cambios en la asignación de recursos en el lado PNPEntity surtendrán efecto en el dispositivo asociado.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a>Miembros

La **clase \_ PnPDevice de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Win32 \_ PnPDevice** tiene estas propiedades.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| \_ LogicalDevice")
</dt> </dl>

Referencia a la [**instancia \_ logicalDevice**](cim-logicaldevice.md) de CIM que representa las propiedades del dispositivo lógico asociadas con el Plug and Play dispositivo.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ PnPEntity**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PnPEntity")
</dt> </dl>

Referencia a la [**instancia de Win32 \_ PnPEntity**](win32-pnpentity.md) que representa Plug and Play dispositivo asociado al dispositivo lógico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
