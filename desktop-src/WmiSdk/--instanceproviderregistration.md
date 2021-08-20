---
description: Registra proveedores de instancias en WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: __InstanceProviderRegistration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
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
ms.openlocfilehash: 773bb54ec4d132e629f21513ffa617cbe3435d35941e7c98c55810d267f614c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821164"
---
# <a name="__instanceproviderregistration-class"></a>\_\_Clase InstanceProviderRegistration

La **\_ \_ clase del sistema InstanceProviderRegistration** registra proveedores de instancias en WMI.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase InstanceProviderRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase InstanceProviderRegistration** tiene estas propiedades.

<dl> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica que una clase o proveedor de instancias proporciona datos o recupera datos de WMI y el repositorio Modelo de información común (CIM). Los proveedores de extracción admiten el acceso dinámico a sus datos; y los proveedores de inserción almacenan sus datos en el repositorio CIM y usan WMI para proporcionar acceso a ellos. Para obtener más información, vea [Determinar el estado de inserción o extracción.](determining-push-or-pull-status.md) El valor predeterminado es 0 (cero).

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Extracción** (0)


</dt> <dd>

Provider es un proveedor de extracción.

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Inserción** (1)


</dt> <dd>

Provider es un proveedor de inserción.

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)


</dt> <dd>

Provider es un proveedor de inserción y comprobación. Tenga en cuenta que los proveedores de comprobación de inserción no se admiten actualmente.

</dd> </dl>

</dd> <dt>

**Proveedor**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ Proveedor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de [**\_ \_ Provider que**](--provider.md) representa la ruta de acceso del objeto al proveedor de instancias. Esta propiedad se hereda de [**\_ \_ ProviderRegistration.**](--providerregistration.md)

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Matriz de los tipos de compatibilidad incluida por el proveedor para el procesamiento de consultas. Los proveedores de clases no admiten todos los tipos de consultas. Los proveedores de instancias pueden **establecer QuerySupportLevels** en **NULL** si no admiten el procesamiento de consultas. Los proveedores que admiten consultas implementan el método [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) y establecen esta propiedad en uno o varios de los valores siguientes.

<dt>



 ("WQL:UnarySelect")


</dt> <dd></dd> <dt>



 ("WQL:References")


</dt> <dd></dd> <dt>



 ("WQL:Associators")


</dt> <dd></dd> <dt>



 ("WQL:V1ProviderDefined")


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsBatching**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es True**, el proveedor admite la eliminación de datos.

<dt>

Verdadero
</dt> <dd>

El proveedor admite la eliminación de clases o instancias mediante la implementación de [**IWbemServices::D eleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (proveedores de clases) o [**IWbemServices::D eleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (proveedores de instancias).

</dd> <dt>

Falso
</dt> <dd>

El proveedor no admite la eliminación de datos y devuelve **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** de [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) o [**DeleteInstanceAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)

</dd> </dl>

</dd> <dt>

**SupportsEnumeration**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es True**, el proveedor admite la enumeración de datos.

<dt>



 (True)


</dt> <dd>

El proveedor admite la enumeración de datos mediante la implementación de uno de los proveedores de clases [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (proveedores de clases) o [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (proveedores de instancias).

</dd> <dt>



 (False)


</dt> <dd>

El proveedor no admite la enumeración de datos y devuelve **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** de [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) o [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).

</dd> </dl>

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es True**, la clase o el proveedor de instancias admite la recuperación de datos.

<dt>

Verdadero
</dt> <dd>

El proveedor admite la recuperación de datos mediante [**la implementación de IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>

Falso
</dt> <dd>

El proveedor no admite la recuperación de datos y devuelve **WBEM \_ E PROVIDER \_ NOT \_ \_ CAPABLE** de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> </dl>

</dd> <dt>

**SupportsPut**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es True**, la clase o el proveedor de instancias admite la modificación de datos.

<dt>



 (True)


</dt> <dd>

El proveedor admite la modificación de clases o instancias mediante la implementación de uno de los métodos siguientes: [**IWbemServices::P utClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (proveedores de clases) o [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (proveedores de clases).

</dd> <dt>



 (False)


</dt> <dd>

El proveedor no admite la modificación de datos y devuelve **WBEM \_ E PROVIDER \_ NOT \_ \_ CAPABLE** de [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

</dd> </dl>

</dd> <dt>

**SupportsTransactions**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase InstanceProviderRegistration** se deriva de [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), que se deriva de [**\_ \_ ProviderRegistration.**](--providerregistration.md) Solo los administradores pueden registrar un proveedor de instancias mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) e **\_ \_ InstanceProviderRegistration**. Solo los administradores pueden eliminar un proveedor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[Registro de un proveedor de clases](registering-a-class-provider.md)
</dt> <dt>

[Registro de un proveedor de instancias](registering-an-instance-provider.md)
</dt> </dl>

 

