---
title: ReplicationProvider1 (clase)
description: Clase base para la instancia del proveedor.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- ReplicationProvider1 (clase) Active Directory
- Clase ReplicationProvider1 Active Directory , descrito
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
ms.openlocfilehash: d3e8ca70d2bb5f37303c20117ddba59db6950d1dda58779179c6ef08c95abc4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025133"
---
# <a name="replicationprovider1-class"></a>ReplicationProvider1 (clase)

Clase base para la instancia del proveedor.

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

La **clase ReplicationProvider1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase ReplicationProvider1** tiene estas propiedades.

<dl> <dt>

**ClientLoadableCLSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identificador de clase que WMI usa para determinar si se debe cargar o no un proveedor de alto rendimiento en el proceso de cliente o en el proceso WMI. Si el proveedor y el cliente se encuentran en el mismo equipo, WMI carga el proveedor en proceso en el cliente mediante **ClientLoadableCLSID** como identificador de clase. Cuando el proveedor y el cliente se encuentran en equipos diferentes, WMI carga el proveedor en proceso en WMI. WMI también usa **ClientLoadableCLSID para** admitir operaciones de actualización.

Para obtener más información, [vea Registrar un proveedor High-Performance usuario.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

**GUID** que representa el identificador de clase **(CLSID)** del objeto COM del proveedor. Este objeto COM debe contener una implementación de la [**interfaz IWbemProviderInit.**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit)

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Concurrency**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**DefaultMachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identifica el equipo en el que se va a iniciar el proveedor. Si el proveedor se ejecuta en el equipo local, es **NULL.**

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Habilitado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es TRUE,** esta instancia está habilitada y se puede usar para completar las solicitudes de cliente.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

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

Tipo de acceso: lectura y escritura
</dt> </dl>

Reservado. El valor predeterminado es cero (0).

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**InitializationReentrancy**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Conjunto de marcas que proporcionan información sobre la serialización. El valor predeterminado es cero (0).

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Se debe serializar toda la inicialización de este proveedor.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Se deben serializar todas las inicializaciones de este proveedor en el mismo espacio de nombres.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


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

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**InitializeAsAdminFirst**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

**Windows Server 2003:** Esta propiedad está deshabilitada.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Nombre del proveedor.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**OperationTimeoutInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**PerLocaleInitialization**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es TRUE,** el proveedor se inicializa para cada configuración regional cuando un usuario se conecta al mismo espacio de nombres más de una vez mediante configuraciones regionales diferentes. El valor predeterminado es **FALSE**.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**PerUserInitialization**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es TRUE,** el proveedor se inicializa una vez para cada usuario de NT LAN Manager (NTLM) que realiza solicitudes al proveedor. Si **es FALSE** (valor predeterminado), el proveedor se inicializa una vez para todos los usuarios.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Pura**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Si **es TRUE,** el proveedor acepta prepararse para la descarga mediante una llamada a [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en todos los puntos de interfaz pendientes cuando WMI llama al método **Release** de su interfaz principal. Los proveedores que deben seguir siendo clientes de WMI después de que no funcionen como proveedores deben **establecer Pure** en **FALSE.** El valor predeterminado es **TRUE.** Para obtener más información, vea la sección Comentarios de este tema.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Descriptor de seguridad (SD) en el lenguaje de definición de descriptores de seguridad (SDDL) que determina el conjunto de usuarios que pueden llamar correctamente a [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) para el proveedor desacoplado. Para más información, consulte el tema [Lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) de la sección Seguridad del SDK Windows seguridad. Este descriptor de seguridad solo se usa para los proveedores desacoplados y no afecta a otros proveedores. Para obtener más información, vea [Incorporación de un proveedor en una aplicación](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).

WMI realiza comprobaciones de acceso para proveedores desacoplados que usan las interfaces [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) [**e IWbemObjectSink.**](/windows/desktop/WmiSdk/iwbemobjectsink) Si el descriptor de seguridad es **NULL,** solo las aplicaciones o servicios que se ejecutan en las cuentas LocalSystem, NetworkService y LocalService pueden ejecutar un proveedor desacoplado.

En la cadena siguiente se muestra un proveedor desacoplado que solo deben ejecutar los administradores integrados". O:BAG:BAD:(A;;0 x1;;; BA)"

Para obtener más información sobre cómo establecer la **propiedad SecurityDescriptor,** vea [Mantener la seguridad wmi.](/windows/desktop/WmiSdk/maintaining-wmi-security)

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsExplicitShutdown**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsExtendedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsQuotas**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsSendStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsShutdown**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**SupportsThrottling**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

No se usa.

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**UnloadTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

[Formato de fecha y hora](/windows/desktop/WmiSdk/date-and-time-format) que especifica cuánto tiempo WMI permite que el proveedor permanezca inactivo antes de que se descargue. Normalmente, los proveedores solicitan que WMI no espere más de cinco minutos.

Para la versión actual de WMI, se omite el valor de esta propiedad. WMI descarga el proveedor en función del valor de tiempo de espera de una clase interna en el espacio \\ de nombres raíz. Se recomienda que los proveedores **establezcan UnloadTimeout.** Para obtener más información, [vea Descargar un proveedor](/windows/desktop/WmiSdk/unloading-a-provider).

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Versión del proveedor. Las versiones admitidas son 1 y 2. La versión 2 refuerza las comprobaciones de validez de todos los registros de propiedades asociados, específicamente la [**propiedad ImpersonationLevel.**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel)

Esta propiedad se hereda de [**\_ \_ Win32Provider.**](/windows/desktop/WmiSdk/--win32provider)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una instancia de esta clase representa el proveedor WMI para Dominio de Active Directory servicios. Los valores predeterminados son los siguientes:

-   Name = "ReplProv1"
-   ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"
-   HostingModel = "NetworkServiceHost"

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

