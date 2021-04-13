---
description: Actúa como clase primaria para las clases que se utilizan para registrar proveedores de clases y de instancias en WMI.
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: __ObjectProviderRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
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
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360779"
---
# <a name="__objectproviderregistration-class"></a>\_\_Clase ObjectProviderRegistration

La clase de sistema abstracta **\_ \_ ObjectProviderRegistration** actúa como clase primaria para las clases que se usan para registrar proveedores de clases y de instancias en WMI.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ ObjectProviderRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ ObjectProviderRegistration** tiene estas propiedades.

<dl> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Indica si el proveedor de clase o instancia proporciona sus propios datos o si se basa en WMI y en el repositorio Modelo de información común (CIM). Los proveedores de extracción admiten el acceso dinámico a sus datos, y los proveedores de inserción almacenan sus datos en el repositorio CIM y dependen de WMI para proporcionar acceso a ellos. Para obtener más información, vea [determinar el estado de inserción o extracción](determining-push-or-pull-status.md). El valor predeterminado es 0 (cero).

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

El proveedor es un proveedor de comprobación de inserciones. Tenga en cuenta que en este momento no se admite la comprobación de inserciones.

</dd> </dl>

</dd> <dt>

**presta**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ proveedor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de [**\_ \_ Provider**](--provider.md) que representa una ruta de acceso de objeto al proveedor de objetos. Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Matriz de los tipos de compatibilidad incluida en el proveedor para el procesamiento de consultas. Los proveedores de clases no admiten ningún tipo de consultas. Los proveedores de instancias pueden establecer **QuerySupportLevels** en **null** si no admiten el procesamiento de consultas. Los proveedores que admiten consultas implementan el método [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) y establecen esta propiedad en uno o varios de los valores siguientes (el tipo de propiedad es una matriz).

"WQL: UnarySelect"

"WQL: References"

"WQL: Associatorsrs"

"WQL: V1ProviderDefined"

</dd> <dt>

**SupportsBatching**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, el proveedor admite la eliminación de datos.

<dt>

True
</dt> <dd>

El proveedor admite la eliminación de la clase o la instancia implementando uno de los [**eleteclassasync de IWbemServices::D**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (proveedores de clases) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (proveedores de instancias).

</dd> <dt>

False
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

Si **es true**, el proveedor admite la enumeración de datos.

<dt>

True
</dt> <dd>

El proveedor admite la enumeración de datos mediante la implementación de uno de los proveedores [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (clase) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (proveedores de instancias).

</dd> <dt>

False
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

Si **es true**, el proveedor de la clase o la instancia admite la recuperación de datos.

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

Si **es true**, el proveedor de clase o instancia admite la modificación de datos.

<dt>

True
</dt> <dd>

El proveedor admite la modificación de la clase o la instancia implementando uno de los [**utclassasync de IWbemServices::P**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (proveedores de clases) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (proveedores de clases).

</dd> <dt>

False
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

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ ObjectProviderRegistration** se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md).

Los proveedores de clases deben establecer la propiedad **SupportsEnumeration** en **true** , ya que los proveedores deben ser capaces de proporcionar a WMI una lista de sus clases. Si un proveedor de clases intenta establecer esta propiedad en **false**, WMI marca el registro como no válido. No es necesario que los proveedores de instancias admitan la enumeración y puede elegir establecer **SupportsEnumeration** en **true** o **false**.

Un proveedor que establece **QuerySupportLevels** en "WQL: UnarySelect" puede aceptar una consulta que consta de la instrucción SELECT básica, tal como se admite en la versión 1,0 de WMI. Se espera que los proveedores de clase y de instancia puedan controlar la propiedad del sistema de **\_ \_ clase** . También se espera que los proveedores de clases procesen la propiedad del sistema de la **\_ \_ superclase** y el operador ISA. El operador ISA se usa para expandir un conjunto de resultados a clases derivadas. Si a un proveedor se le proporciona una consulta que no puede interpretar, solicita que WMI lo controle devolviendo el valor de error de **WBEM \_ E \_ demasiado \_ complejo** . Para obtener una descripción de la sintaxis válida de WQL, vea [consultas con WQL](querying-with-wql.md).

Un proveedor que establece **QuerySupportLevels** en **WQL: V1ProviderDefined** puede intentar admitir un conjunto mayor de sintaxis SQL bajo su propio riesgo, como la `ORDER BY` cláusula. WMI no interpreta las cláusulas adicionales o intenta asegurarse de que el conjunto de resultados es correcto.

Solo los administradores pueden registrar o eliminar un proveedor mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y su registro.

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

[Registrar un proveedor](registering-a-provider.md)
</dt> </dl>

 

