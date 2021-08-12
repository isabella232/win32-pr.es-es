---
description: Se usa para registrar proveedores de eventos con Windows Management Instrumentation (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: __EventProviderRegistration clase
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
ms.openlocfilehash: ce973f05aec0a1c859598c558ef8c2cc637a8faec22fd1d7f2ad2aaf383bd201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557949"
---
# <a name="__eventproviderregistration-class"></a>\_\_EventProviderRegistration (clase)

La **\_ \_ clase del sistema EventProviderRegistration** se usa para registrar proveedores de eventos con Windows Management Instrumentation (WMI).

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

La **\_ \_ clase EventProviderRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase EventProviderRegistration** tiene estas propiedades.

<dl> <dt>

**EventQueryList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Una o varias consultas Windows lenguaje de consulta de instrumentación de administración de administración (WQL) que describen los eventos que admite el proveedor de eventos.

</dd> <dt>

**Proveedor**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ Proveedor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del objeto al proveedor de eventos. Esta propiedad se hereda de [**\_ \_ ProviderRegistration.**](--providerregistration.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Solo los administradores pueden registrar o eliminar un proveedor de eventos mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ EventProviderRegistration**](--eventconsumerproviderregistration.md). La **\_ \_ clase EventProviderRegistration** se deriva de [**\_ \_ ProviderRegistration.**](--providerregistration.md)

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

[Registro de un proveedor de eventos](registering-an-event-provider.md)
</dt> <dt>

[Escribir un proveedor de eventos](writing-an-event-provider.md)
</dt> </dl>

 

