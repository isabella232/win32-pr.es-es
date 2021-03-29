---
description: Registra información sobre la implementación física de un proveedor en WMI. Los proveedores que no establecen la propiedad HostingModel se cargan, de forma predeterminada, para ejecutarse en un proceso de Wmiprvse.exe como NetworkServiceHostOrSelfHost.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: __Win32Provider (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002836"
---
# <a name="__win32provider-class"></a>\_\_Clase Win32Provider

La clase del sistema **\_ \_ Win32Provider** registra información sobre la implementación física de un proveedor en WMI. Los proveedores que no establecen la propiedad **HostingModel** se cargan, de forma predeterminada, para ejecutarse en un proceso de Wmiprvse.exe como **NetworkServiceHostOrSelfHost**.

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

La clase **\_ \_ Win32Provider** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ Win32Provider** tiene estas propiedades.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Identificador de clase que WMI usa para determinar si se carga o no un proveedor de alto rendimiento en el proceso de cliente o en el proceso WMI. Si el proveedor y el cliente se encuentran en el mismo equipo, WMI carga el proveedor en proceso en el cliente mediante **ClientLoadableCLSID** como identificador de clase. Cuando el proveedor y el cliente se encuentran en equipos diferentes, WMI carga el proveedor en proceso en WMI. WMI también usa **ClientLoadableCLSID** para admitir las operaciones de actualización.

Para obtener más información, vea [registrar un proveedor de High-Performance.](registering-a-high-performance-provider.md)

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

**GUID** que representa el identificador de clase (**CLSID**) del objeto com del proveedor. Este objeto COM debe contener una implementación de la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) .

</dd> <dt>

**Simultaneidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Identifica el equipo en el que se va a iniciar el proveedor. Si el proveedor se ejecuta en el equipo local, es **null**.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, esta instancia está habilitada y se puede usar para completar las solicitudes de cliente.

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Esta propiedad se compone de los valores de las propiedades **HostingGroup** y **HostingSpecification** de los [**\_ proveedores msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) . El valor de esta propiedad especifica cómo WMI carga el proveedor y la cuenta de seguridad con la que se ejecuta. Para obtener más información sobre cómo establecer la propiedad **HostingModel** , vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md) y [registro de un proveedor](registering-a-provider.md).

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Reservado. El valor predeterminado es cero (0).

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Conjunto de marcas que proporcionan información sobre la serialización. El valor predeterminado es cero (0).

<dt>

0
</dt> <dd>

Toda la inicialización de este proveedor debe estar serializada.

</dd> <dt>

1
</dt> <dd>

Todas las inicializaciones de este proveedor en el mismo espacio de nombres se deben serializar.

</dd> <dt>

2
</dt> <dd>

No es necesaria ninguna serialización de inicialización.

</dd> </dl>

</dd> <dt>

**InitializationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

TBD

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [ **clave**](standard-qualifiers.md)
</dt> </dl>

Nombre del proveedor.

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, el proveedor se inicializa para cada configuración regional cuando un usuario se conecta al mismo espacio de nombres más de una vez con diferentes configuraciones regionales. El valor predeterminado es **FALSE**.

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, el proveedor se inicializa una vez por cada usuario de NT LAN Manager (NTLM) que realiza solicitudes al proveedor. Si es **false** (valor predeterminado), el proveedor se inicializa una vez para todos los usuarios.

</dd> <dt>

**Pura**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, el proveedor acuerda preparar la descarga llamando a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en todos los puntos de interfaz pendientes cuando WMI llama al método de **versión** de su interfaz principal. Los proveedores que deben seguir siendo clientes de WMI después de no funcionar como proveedores deberían establecer **puro** en **false**. El valor predeterminado es **true**. Para obtener más información, consulte la sección Comentarios de este tema.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Descriptor de seguridad (SD) en el lenguaje de definición de descriptores de seguridad (SDDL) que determina el conjunto de usuarios que pueden llamar correctamente a [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) para el proveedor desacoplado. Para obtener más información, vea el tema [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) en la sección seguridad de la Windows SDK. Este descriptor de seguridad solo se usa para los proveedores desacoplados y no afecta a otros proveedores. Para obtener más información, vea [incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md).

WMI realiza comprobaciones de acceso para los proveedores desacoplados que usan las interfaces [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) y [**IWbemObjectSink**](iwbemobjectsink.md) . Si el descriptor de seguridad es **null**, solo las aplicaciones o servicios que se ejecutan en las cuentas LocalSystem, NetworkService y LocalService pueden ejecutar un proveedor desacoplado.

La siguiente cadena muestra un proveedor desacoplado que solo deben ejecutar los administradores integrados ". O:BAG: BAD: (A;; 0 x1;;; BA) "

Para obtener más información acerca de cómo establecer la propiedad **SecurityDescriptor** , vea [mantener la seguridad de WMI](maintaining-wmi-security.md).

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

[Formato de fecha y hora](date-and-time-format.md) que especifica el tiempo que WMI permite que el proveedor permanezca inactivo antes de que se descargue. Normalmente, los proveedores solicitan que WMI espere más de cinco minutos.

Para la versión actual de WMI, se omite el valor de esta propiedad. WMI descarga el proveedor basándose en el valor de tiempo de espera de una clase interna en el \\ espacio de nombres raíz. Se recomienda que los proveedores establezcan **UnloadTimeout**. Para obtener más información, vea [descargar un proveedor](unloading-a-provider.md).

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Versión del proveedor. Las versiones admitidas son 1 y 2. La versión 2 fortalece las comprobaciones de validez de todos los registros de propiedades asociados, en concreto la propiedad [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ Win32Provider** se deriva de [**\_ \_ Provider**](--provider.md).

La mayoría de los proveedores pueden aceptar los valores predeterminados para la propiedad **InitializationReentrancy** . Sin embargo, si un proveedor puede admitir la inicialización simultánea para usuarios independientes, esta propiedad se puede establecer en 1 (uno). Si es necesaria la inicialización serializada, **InitializationReentrancy** sigue siendo 0 (cero). En ambas instancias, **PerUserInitialization** se establece en **true**.

Un proveedor puro o un proveedor que establece la propiedad **Pure** en **true** solo existe para las solicitudes de servicio de las aplicaciones y WMI. La mayoría de los proveedores son proveedores puros. Un proveedor no puro es la excepción. Los proveedores no puros pasan al rol de cliente después de completar las solicitudes de servicio.

Un ejemplo de un proveedor no puro es un proveedor de inserciones que empieza a emitir consultas y realiza solicitudes de WMI después de completar la inicialización. Un proveedor de inserciones no tiene responsabilidades salvo para actualizar el repositorio CIM con datos en el momento de la inicialización. Después de actualizar el repositorio, un proveedor de inserciones puede esperar a que se descargue o pasar al rol de cliente. El proveedor de inserciones que espera que se descargue es un proveedor puro. El proveedor de inserciones que participa en las actividades del cliente no es puro.

WMI debe ser capaz de distinguir los proveedores puros de los proveedores no puros para que pueda determinar cuándo es seguro apagar. WMI debe esperar a que se completen todas las operaciones que implican proveedores no puros antes de poder cerrarse de forma segura.

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

[Registrar un proveedor](registering-a-provider.md)
</dt> </dl>

 

