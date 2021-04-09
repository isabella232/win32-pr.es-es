---
title: Clase ReplicationProvider1
description: La clase base para la instancia del proveedor.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- Active Directory de la clase ReplicationProvider1
- Active Directory de la clase ReplicationProvider1, descrito
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0098556fcbc1400ccd1042198903fec7e018ed57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079278"
---
# <a name="replicationprovider1-class"></a>Clase ReplicationProvider1

La clase base para la instancia del proveedor.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
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
  string   HostingModel;
};
```

## <a name="members"></a>Miembros

La clase **ReplicationProvider1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **ReplicationProvider1** tiene estas propiedades.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Identificador de clase que WMI usa para determinar si se carga o no un proveedor de alto rendimiento en el proceso de cliente o en el proceso WMI. Si el proveedor y el cliente se encuentran en el mismo equipo, WMI carga el proveedor en proceso en el cliente mediante **ClientLoadableCLSID** como identificador de clase. Cuando el proveedor y el cliente se encuentran en equipos diferentes, WMI carga el proveedor en proceso en WMI. WMI también usa **ClientLoadableCLSID** para admitir las operaciones de actualización.

Para obtener más información, vea [registrar un proveedor de High-Performance.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

**GUID** que representa el identificador de clase (**CLSID**) del objeto com del proveedor. Este objeto COM debe contener una implementación de la interfaz [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) .

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Simultaneidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Identifica el equipo en el que se va a iniciar el proveedor. Si el proveedor se ejecuta en el equipo local, es **null**.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, esta instancia está habilitada y se puede usar para completar las solicitudes de cliente.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**HostingModel**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")
</dt> </dl>

Contiene el modelo de hospedaje del proveedor.

</dd> <dt>

**ImpersonationLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Reservado. El valor predeterminado es cero (0).

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Conjunto de marcas que proporcionan información sobre la serialización. El valor predeterminado es cero (0).

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

Toda la inicialización de este proveedor debe estar serializada.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Todas las inicializaciones de este proveedor en el mismo espacio de nombres se deben serializar.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


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

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

**Windows Server 2003:** Esta propiedad está deshabilitada.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Nombre del proveedor.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, el proveedor se inicializa para cada configuración regional cuando un usuario se conecta al mismo espacio de nombres más de una vez con diferentes configuraciones regionales. El valor predeterminado es **FALSE**.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si es **true**, el proveedor se inicializa una vez por cada usuario de NT LAN Manager (NTLM) que realiza solicitudes al proveedor. Si es **false** (valor predeterminado), el proveedor se inicializa una vez para todos los usuarios.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Pura**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Si **es true**, el proveedor acuerda preparar la descarga llamando a [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en todos los puntos de interfaz pendientes cuando WMI llama al método de **versión** de su interfaz principal. Los proveedores que deben seguir siendo clientes de WMI después de no funcionar como proveedores deberían establecer **puro** en **false**. El valor predeterminado es **true**. Para obtener más información, consulte la sección Comentarios de este tema.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Descriptor de seguridad (SD) en el lenguaje de definición de descriptores de seguridad (SDDL) que determina el conjunto de usuarios que pueden llamar correctamente a [**IWbemDecoupledRegistrar: Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) para el proveedor desacoplado. Para obtener más información, vea el tema [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) en la sección seguridad de la Windows SDK. Este descriptor de seguridad solo se usa para los proveedores desacoplados y no afecta a otros proveedores. Para obtener más información, vea [incorporación de un proveedor en una aplicación](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).

WMI realiza comprobaciones de acceso para los proveedores desacoplados que usan las interfaces [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) y [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) . Si el descriptor de seguridad es **null**, solo las aplicaciones o servicios que se ejecutan en las cuentas LocalSystem, NetworkService y LocalService pueden ejecutar un proveedor desacoplado.

La siguiente cadena muestra un proveedor desacoplado que solo deben ejecutar los administradores integrados ". O:BAG: BAD: (A;; 0 x1;;; BA) "

Para obtener más información acerca de cómo establecer la propiedad **SecurityDescriptor** , vea [mantener la seguridad de WMI](/windows/desktop/WmiSdk/maintaining-wmi-security).

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

No se utiliza.

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

[Formato de fecha y hora](/windows/desktop/WmiSdk/date-and-time-format) que especifica el tiempo que WMI permite que el proveedor permanezca inactivo antes de que se descargue. Normalmente, los proveedores solicitan que WMI espere más de cinco minutos.

Para la versión actual de WMI, se omite el valor de esta propiedad. WMI descarga el proveedor basándose en el valor de tiempo de espera de una clase interna en el \\ espacio de nombres raíz. Se recomienda que los proveedores establezcan **UnloadTimeout**. Para obtener más información, vea [descargar un proveedor](/windows/desktop/WmiSdk/unloading-a-provider).

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Versión del proveedor. Las versiones admitidas son 1 y 2. La versión 2 fortalece las comprobaciones de validez de todos los registros de propiedades asociados, en concreto la propiedad [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) .

Esta propiedad se hereda de [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una instancia de esta clase representa el proveedor WMI para Dominio de Active Directory Services. Los valores predeterminados son los siguientes:

-   Name = "ReplProv1"
-   ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"
-   HostingModel = "NetworkServiceHost"

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\MicrosoftActiveDirectory raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

