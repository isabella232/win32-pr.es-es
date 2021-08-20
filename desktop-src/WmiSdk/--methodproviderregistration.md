---
description: Registra proveedores de métodos con WMI.
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: __MethodProviderRegistration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2a778e2d94c39448020d5a1b4a99e9030320dee4c8604d390c6008f29fabff4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820943"
---
# <a name="__methodproviderregistration-class"></a>\_\_Clase MethodProviderRegistration

La **\_ \_ clase del sistema MethodProviderRegistration** registra proveedores de métodos con WMI.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase MethodProviderRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase MethodProviderRegistration** tiene estas propiedades.

<dl> <dt>

**Proveedor**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ Proveedor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de [**\_ \_ Provider que**](--provider.md) representa la ruta de acceso del objeto del proveedor de métodos. Esta propiedad se hereda de [**\_ \_ ProviderRegistration.**](--providerregistration.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase MethodProviderRegistration** se deriva de [**\_ \_ ProviderRegistration.**](--providerregistration.md) Solo los administradores pueden registrar o eliminar un proveedor de métodos mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y **\_ \_ MethodProviderRegistration**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[Registrar un proveedor de métodos](registering-a-method-provider.md)
</dt> </dl>

 

