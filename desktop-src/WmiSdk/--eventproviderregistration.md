---
description: Se utiliza para registrar proveedores de eventos con Instrumental de administración de Windows (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: __EventProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697370"
---
# <a name="__eventproviderregistration-class"></a>\_\_Clase EventProviderRegistration

La clase del sistema **\_ \_ EventProviderRegistration** se utiliza para registrar proveedores de eventos con instrumental de administración de Windows (WMI).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ EventProviderRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ EventProviderRegistration** tiene estas propiedades.

<dl> <dt>

**EventQueryList**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Una o más consultas del lenguaje de consulta de Instrumental de administración de Windows (WQL) que describen los eventos que admite el proveedor de eventos.

</dd> <dt>

**presta**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ proveedor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del objeto al proveedor de eventos. Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Solo los administradores pueden registrar o eliminar un proveedor de eventos mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md). La clase **\_ \_ EventProviderRegistration** se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrar un proveedor de eventos](registering-an-event-provider.md)
</dt> <dt>

[Escribir un proveedor de eventos](writing-an-event-provider.md)
</dt> </dl>

 

