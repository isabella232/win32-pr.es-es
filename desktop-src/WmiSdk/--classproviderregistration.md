---
description: Registra proveedores de clase en WMI.
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: __ClassProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 32442122624035ec376bed3be8b3ef20c80f8524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818971"
---
# <a name="__classproviderregistration-class"></a>\_\_Clase ClassProviderRegistration

La clase del sistema **\_ \_ ClassProviderRegistration** registra los proveedores de clases en WMI.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ ClassProviderRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ ClassProviderRegistration** tiene estas propiedades.

<dl> <dt>

**CacheRefreshInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el proveedor de clase o instancia proporciona datos o si se basa en WMI y en el repositorio Modelo de información común (CIM). Los proveedores de extracción admiten el acceso dinámico a los datos, y los proveedores de inserción almacenan los datos en el repositorio CIM y se basan en WMI para proporcionar acceso a ellos. El valor predeterminado es 0 (cero). Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md). Para obtener más información, vea [determinar el estado de inserción o extracción](determining-push-or-pull-status.md).

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Extracción** (0)


</dt> <dd>

El proveedor es un proveedor de extracción.

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Inserte** (1)


</dt> <dd>

El proveedor es un proveedor de inserciones.

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)


</dt> <dd>

El proveedor es un proveedor de comprobación de inserciones. Tenga en cuenta que en este momento no se admiten los proveedores de **PushVerify** .

</dd> </dl>

</dd> <dt>

**PerUserSchema**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**presta**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ proveedor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del objeto a un proveedor de clases. Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Matriz de los tipos de compatibilidad incluida en el proveedor para el procesamiento de consultas. Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md). Se requieren proveedores de clases para admitir al menos un tipo de consulta. Los proveedores de instancias pueden establecer **QuerySupportLevels** en **null** si no admiten el procesamiento de consultas. Los proveedores que admiten consultas implementan el método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) y establecen esta propiedad en uno o varios de los valores siguientes:

<dt>



 ("WQL: UnarySelect")


</dt> <dd></dd> <dt>



 ("WQL: References")


</dt> <dd></dd> <dt>



 ("WQL: Associatorsers")


</dt> <dd></dd> <dt>



 ("WQL: V1ProviderDefined")


</dt> <dd></dd> </dl>

</dd> <dt>

**ReferencedSetQueries**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Una o más consultas que describen el conjunto de clases a las que se hace referencia que admite un proveedor de clases. Los proveedores que pueden proporcionar clases de asociación deben incluir al menos una consulta en esta propiedad.

</dd> <dt>

**ResultSetQueries**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Una o más consultas que describen el conjunto de todas las clases que puede proporcionar el proveedor de clases o un superconjunto de esas clases. Esta propiedad nunca especifica un subconjunto de clases admitidas.

</dd> <dt>

**ReSynchroniseOnNamespaceOpen**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**SupportsBatching**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, el proveedor admite la eliminación de datos. Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 Reales


</dt> <dd>

El proveedor admite la eliminación de la clase o la instancia implementando uno de los [**eleteclassasync de IWbemServices::D**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (proveedores de clases) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (proveedores de instancias).

</dd> <dt>



 Es


</dt> <dd>

El proveedor no admite la eliminación de datos y devuelve **el \_ proveedor WBEM e \_ no es \_ \_ capaz** de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) o [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsEnumeration**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, el proveedor admite la enumeración de datos. Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 Reales


</dt> <dd>

El proveedor admite la enumeración de datos mediante la implementación de uno de los proveedores [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (clase) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (proveedores de instancias).

</dd> <dt>



 Es


</dt> <dd>

El proveedor no admite la enumeración de datos y devuelve el **\_ proveedor WBEM e \_ no es \_ \_ capaz** de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) o [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).

</dd> </dl>

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, el proveedor de la clase o la instancia admite la recuperación de datos. Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 Reales


</dt> <dd>

El proveedor admite la recuperación de datos mediante la implementación de [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>



 Es


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

Si **es true**, el proveedor de clase o instancia admite la modificación de datos. Esta propiedad se hereda de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).

<dt>



 Reales


</dt> <dd>

El proveedor admite la modificación de la clase o la instancia implementando uno de los [**utclassasync de IWbemServices::P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (proveedores de clases) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (proveedores de clases).

</dd> <dt>



 Es


</dt> <dd>

El proveedor no admite la modificación de datos y devuelve el **\_ proveedor WBEM e \_ no es \_ \_ capaz** de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsTransactions**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**SuppportsBatching**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**UnsupportedQueries**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Una o más consultas que describen el conjunto de clases que no admite el proveedor de clases. Utilice esta propiedad para restar del conjunto de clases implícitas por **ResultSetQueries**.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Versión de este proveedor de clases.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ ClassProviderRegistration** se deriva de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), que se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md).

Las propiedades heredadas de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) indican si el proveedor de clases admite o no la recuperación de datos, la modificación, la eliminación, la enumeración y el procesamiento de consultas. La propiedad **InteractionType** especifica si el proveedor de clases está diseñado como un proveedor de extracción o de inserción. Para obtener más información, vea [determinar el estado de inserción o extracción](determining-push-or-pull-status.md).

La clase [**\_ \_ ProviderRegistration**](--providerregistration.md) define la propiedad del [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) . Solo los administradores pueden registrar un proveedor mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y **\_ \_ ClassProviderRegistration**. Solo los administradores pueden eliminar un proveedor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ObjectProviderRegistration**](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrar un proveedor de clases](registering-a-class-provider.md)
</dt> <dt>

[Registrar un proveedor de instancias](registering-an-instance-provider.md)
</dt> <dt>

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 

