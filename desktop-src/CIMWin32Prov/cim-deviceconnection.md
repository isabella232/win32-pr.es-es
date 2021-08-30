---
description: La clase de \_ asociación Cim DeviceConnection representa dos o más dispositivos conectados.
ms.assetid: 82095cd6-1843-4db2-9fe8-3e225611bd3b
ms.tgt_platform: multiple
title: CIM_DeviceConnection clase (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.NegotiatedDataWidth
- CIM_DeviceConnection.NegotiatedSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: da27b652058a6205cb7dcc6ffa6527beac066482eb331aefd79351a3ee1fc113
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924535"
---
# <a name="cim_deviceconnection-class-cimwin32-wmi-providers"></a>CIM_DeviceConnection clase (proveedores WMI CIMWin32)

La **clase de \_ asociación Cim DeviceConnection** representa dos o más dispositivos conectados.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{8502C53C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
};
```

## <a name="members"></a>Miembros

La **clase \_ Cim DeviceConnection** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Cim DeviceConnection** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Un [**dispositivo \_ lógico CIM**](cim-logicaldevice.md) que describe un dispositivo lógico.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un [**dispositivo \_ lógico CIM**](cim-logicaldevice.md) que describe un segundo dispositivo lógico conectado al dispositivo antecedente.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Cuando son posibles varios anchos de datos de conexión o bus, esta propiedad define el que se usa entre los dispositivos. El ancho de los datos se especifica en bits. Si no se negocia el ancho de los datos, o si esta información no está disponible o no es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")
</dt> </dl>

Cuando son posibles varias velocidades de conexión o bus, esta propiedad define la que se usa entre los dispositivos. La velocidad se especifica en bits por segundo. Si no se negocian las velocidades de conexión o bus, o si esta información no está disponible o es importante para la administración de dispositivos, la propiedad debe establecerse en 0 (cero).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ Cim DeviceConnection** se deriva de la [**dependencia \_ CIM**](cim-dependency.md).

WMI no implementa esta clase. Para obtener más información sobre las clases derivadas de **CIM \_ DeviceConnection**, vea [Clases win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

