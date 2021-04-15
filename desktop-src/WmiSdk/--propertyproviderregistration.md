---
description: Registra proveedores de propiedades en WMI.
ms.assetid: 24792884-3fb9-4974-83d5-1c5fc1fa72a1
ms.tgt_platform: multiple
title: __PropertyProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderRegistration
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6d618a62eab4ba799a2d0e152763fcef6567fd42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545766"
---
# <a name="__propertyproviderregistration-class"></a>\_\_Clase PropertyProviderRegistration

La clase del sistema **\_ \_ PropertyProviderRegistration** registra proveedores de propiedades en WMI.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __PropertyProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
  boolean        SupportsPut = False;
  boolean        SupportsGet = False;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ PropertyProviderRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ PropertyProviderRegistration** tiene estas propiedades.

<dl> <dt>

**presta**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ proveedor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de [**\_ \_ Provider**](--provider.md) que representa la ruta de acceso del objeto del proveedor de propiedades. Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Describe si el proveedor de clase o instancia admite la recuperación de datos.

<dt>

True
</dt> <dd>

El proveedor admite la recuperación de datos mediante la implementación de [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>

False
</dt> <dd>

El proveedor no admite la recuperación de datos y devuelve **el \_ proveedor WBEM e \_ no es \_ \_ compatible** con [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> </dl>

</dd> <dt>

**SupportsPut**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Describe si el proveedor de clase o instancia admite la modificación de datos.

<dt>

True
</dt> <dd>

El proveedor admite la modificación de la clase o la instancia implementando uno de los métodos siguientes:

-   [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (proveedores de clases)
-   [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (proveedores de clases)

</dd> <dt>

False
</dt> <dd>

El proveedor no admite la modificación de datos y devuelve el **\_ proveedor WBEM e \_ no es \_ \_ capaz** de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ PropertyProviderRegistration** se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md). Solo los administradores pueden registrar un proveedor de propiedades mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y **\_ \_ PropertyProviderRegistration**. Solo los administradores pueden eliminar un proveedor de propiedades.

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

[Registrar un proveedor de propiedades](registering-a-property-provider.md)
</dt> </dl>

 

