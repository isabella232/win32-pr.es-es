---
description: La asociación SystemDevice de CIM representa una relación explícita en la que un sistema puede \_ agregar dispositivos lógicos.
ms.assetid: df624a9f-0c10-44a3-8075-908e5e481e3c
ms.tgt_platform: multiple
title: CIM_SystemDevice clase (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.PartComponent
- CIM_SystemDevice.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a7857425074326dc3de7985fb7ecfbb909948a6b7a975aaa3e019a4a56e36df6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119817605"
---
# <a name="cim_systemdevice-class-cimwin32-wmi-providers"></a>CIM_SystemDevice clase (proveedores WMI CIMWin32)

La **\_ asociación SystemDevice** de CIM representa una relación explícita en la que un sistema puede agregar dispositivos lógicos.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{4B2C30D7-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_LogicalDevice REF PartComponent;
  CIM_System        REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SystemDevice** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemDevice** de CIM tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Sistema CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Sistema [**CIM \_ que**](cim-system.md) describe el sistema primario de la asociación.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Un [**\_ dispositivo lógico CIM**](cim-logicaldevice.md) que describe el dispositivo lógico que es un componente de un sistema.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ SystemDevice** de CIM se deriva de [**\_ SYSTEMComponent de CIM.**](cim-systemcomponent.md)

WMI no implementa esta clase. Para las clases WMI derivadas de **CIM \_ SystemDevice**, vea [Clases win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> </dl>

 

