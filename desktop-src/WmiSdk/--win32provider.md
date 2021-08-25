---
description: Registra información sobre la implementación física de un proveedor en WMI. Los proveedores que no establecen la propiedad HostingModel se cargan, de forma predeterminada, para ejecutarse en un proceso Wmiprvse.exe como NetworkServiceHostOrSelfHost.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: __Win32Provider clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dd7c848e9c792bcff3c0af58143d404bda744a982daeedbff01895242407a7aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857695"
---
# <a name="__win32provider-class"></a>\_\_Clase Win32Provider

La **\_ \_ clase de sistema Win32Provider** registra información sobre la implementación física de un proveedor en WMI. Los proveedores que no establecen la **propiedad HostingModel** se cargan, de forma predeterminada, para ejecutarse en un proceso Wmiprvse.exe como **NetworkServiceHostOrSelfHost**.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase Win32Provider** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase Win32Provider** tiene estas propiedades.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identificador de clase que WMI usa para determinar si se debe cargar o no un proveedor de alto rendimiento en el proceso de cliente o en el proceso WMI. Si el proveedor y el cliente se encuentran en el mismo equipo, WMI carga el proveedor en proceso al cliente mediante **ClientLoadableCLSID** como identificador de clase. Cuando el proveedor y el cliente se encuentran en equipos diferentes, WMI carga el proveedor en proceso en WMI. WMI también usa **ClientLoadableCLSID para** admitir operaciones de actualización.

Para obtener más información, [vea Registrar un proveedor High-Performance datos.](registering-a-high-performance-provider.md)

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

**GUID** que representa el identificador de clase (**CLSID**) del objeto COM del proveedor. Este objeto COM debe contener una implementación de la [**interfaz IWbemProviderInit.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)

</dd> <dt>

**Concurrency**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identifica el equipo en el que se va a iniciar el proveedor. Si el proveedor se ejecuta en el equipo local, es **NULL.**

</dd> <dt>

**Habilitado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es TRUE,** esta instancia está habilitada y se puede usar para completar las solicitudes de cliente.

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Esta propiedad se compone de valores de las propiedades **HostingGroup** y **HostingSpecification de** proveedores [**msfT. \_**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) El valor de esta propiedad especifica cómo WMI carga el proveedor y la cuenta de seguridad con la que se ejecuta. Para obtener más información sobre cómo establecer **la propiedad HostingModel,** vea [Provider Hosting and Security](provider-hosting-and-security.md) y [Registering a Provider](registering-a-provider.md).

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Reservado. El valor predeterminado es cero (0).

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Conjunto de marcas que proporcionan información sobre la serialización. El valor predeterminado es cero (0).

<dt>

0
</dt> <dd>

Se debe serializar toda la inicialización de este proveedor.

</dd> <dt>

1
</dt> <dd>

Se deben serializar todas las inicializaciones de este proveedor en el mismo espacio de nombres.

</dd> <dt>

2
</dt> <dd>

No se necesita serialización de inicialización.

</dd> </dl>

</dd> <dt>

**InitializationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Por determinar

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **Clave**](standard-qualifiers.md)
</dt> </dl>

Nombre del proveedor.

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es TRUE,** el proveedor se inicializa para cada configuración regional cuando un usuario se conecta al mismo espacio de nombres más de una vez mediante configuraciones regionales diferentes. El valor predeterminado es **FALSE**.

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es TRUE,** el proveedor se inicializa una vez para cada usuario de NT LAN Manager (NTLM) que realiza solicitudes al proveedor. Si **es FALSE** (valor predeterminado), el proveedor se inicializa una vez para todos los usuarios.

</dd> <dt>

**Pura**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es TRUE,** el proveedor acepta prepararse para la descarga mediante una llamada a [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en todos los puntos de interfaz pendientes cuando WMI llama al **método Release** de su interfaz principal. Los proveedores que deben seguir siendo clientes de WMI después de que no funcionen como proveedores deben **establecer Pure** en **FALSE.** El valor predeterminado es **TRUE.** Para obtener más información, vea la sección Comentarios de este tema.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Descriptor de seguridad (SD) en el lenguaje de definición de descriptores de seguridad (SDDL) que determina el conjunto de usuarios que pueden llamar correctamente a [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) para el proveedor desacoplado. Para más información, consulte el tema [Lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) de la sección Seguridad del SDK Windows seguridad. Este descriptor de seguridad solo se usa para los proveedores desacoplados y no afecta a otros proveedores. Para obtener más información, vea [Incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md).

WMI realiza comprobaciones de acceso para proveedores desacoplados que usan las interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) [**e IWbemObjectSink.**](iwbemobjectsink.md) Si el descriptor de seguridad es **NULL,** solo las aplicaciones o servicios que se ejecutan en las cuentas LocalSystem, NetworkService y LocalService pueden ejecutar un proveedor desacoplado.

En la cadena siguiente se muestra un proveedor desacoplado que solo deben ejecutar los administradores integrados". O:BAG:BAD:(A;;0 x1;;; BA)"

Para obtener más información sobre cómo establecer la **propiedad SecurityDescriptor,** vea [Mantener la seguridad wmi.](maintaining-wmi-security.md)

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

[Formato de fecha y hora](date-and-time-format.md) que especifica cuánto tiempo WMI permite que el proveedor permanezca inactivo antes de que se descargue. Normalmente, los proveedores solicitan que WMI no espere más de cinco minutos.

Para la versión actual de WMI, se omite el valor de esta propiedad. WMI descarga el proveedor en función del valor de tiempo de espera de una clase interna en el espacio \\ de nombres raíz. Se recomienda que los proveedores **establezcan UnloadTimeout.** Para obtener más información, [vea Descargar un proveedor](unloading-a-provider.md).

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Versión del proveedor. Las versiones admitidas son 1 y 2. La versión 2 refuerza las comprobaciones de validez de todos los registros de propiedades asociados, específicamente la [**propiedad ImpersonationLevel.**](swbemsecurity-impersonationlevel.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase Win32Provider** se deriva del [**\_ \_ proveedor**](--provider.md).

La mayoría de los proveedores pueden aceptar los valores predeterminados para **la propiedad InitializationReentrancy.** Sin embargo, si un proveedor puede admitir la inicialización simultánea para usuarios independientes, esta propiedad se puede establecer en 1 (uno). Si es necesaria la inicialización serializada, **InitializationReentrancy** sigue siendo 0 (cero). En ambos casos, **PerUserInitialization** se establece en **TRUE.**

Un proveedor puro o un proveedor que establece la **propiedad Pure** en **TRUE** solo existe para las solicitudes de servicio de las aplicaciones y WMI. La mayoría de los proveedores son proveedores puros. Un proveedor nopure es la excepción. Los proveedores nopure se transiciónn al rol de cliente después de completar las solicitudes de mantenimiento.

Un ejemplo de un proveedor nopure es un proveedor de inserción que comienza a emitir consultas y realiza solicitudes de WMI una vez completada la inicialización. Un proveedor de inserción no tiene responsabilidades excepto actualizar el repositorio CIM con datos en el momento de la inicialización. Después de actualizar el repositorio, un proveedor de inserción puede esperar a que se descargue o realizar la transición al rol de cliente. El proveedor de inserción que espera a descargarse es un proveedor puro. El proveedor de inserción que participa en las actividades de cliente no espure.

WMI debe ser capaz de distinguir proveedores puros de proveedores no puros para que pueda determinar cuándo es seguro apagar. WMI debe esperar a que se completen todas las operaciones que implican proveedores no puros para poder cerrarse de forma segura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_Proveedor**](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registro de un proveedor](registering-a-provider.md)
</dt> </dl>

 

