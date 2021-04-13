---
title: Win32_TSDiscoveredLicenseServer (clase)
description: Proporciona detalles sobre el servidor de licencias Escritorio remoto detectado.
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Win32_TSDiscoveredLicenseServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSDiscoveredLicenseServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSDiscoveredLicenseServer
- Win32_TSDiscoveredLicenseServer.LicenseServer
- Win32_TSDiscoveredLicenseServer.HowDiscovered
- Win32_TSDiscoveredLicenseServer.IsLSAvailable
- Win32_TSDiscoveredLicenseServer.IsAdminOnLS
- Win32_TSDiscoveredLicenseServer.IssuingCALs
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d633031df533068f2cf5da65f2f6820a93c78513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492718"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a>\_Clase Win32 TSDiscoveredLicenseServer

Proporciona detalles sobre el servidor de licencias Escritorio remoto detectado.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, AMENDMENT]
class Win32_TSDiscoveredLicenseServer
{
  string LicenseServer;
  uint32 HowDiscovered;
  uint32 IsLSAvailable;
  uint32 IsAdminOnLS;
  uint32 IssuingCALs;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSDiscoveredLicenseServer de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TSDiscoveredLicenseServer de Win32** tiene estas propiedades.

<dl> <dt>

**HowDiscovered**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Este propiedad ya no se admite.

**Windows Server 2008:** Método de detección del servidor de licencias Escritorio remoto.

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)


</dt> <dd>

El servidor de licencias se ha detectado mediante la Directiva de grupo.

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)


</dt> <dd>

El servidor de licencias se ha detectado mediante una configuración del registro.

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)


</dt> <dd>

El servidor de licencias se ha detectado mediante el ámbito de detección de grupo de trabajo.

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)


</dt> <dd>

El servidor de licencias se ha detectado mediante el ámbito de detección de dominios.

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)


</dt> <dd>

El servidor de licencias se ha detectado mediante el ámbito de detección de bosque.

</dd> </dl>

</dd> <dt>

**IsAdminOnLS**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la cuenta que se usa para ejecutar el script o el archivo. exe que está utilizando la clase **Win32 \_ TSDiscoveredLicenseServer** tiene acceso de administrador al servidor de licencias.

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span id="No"></span><span id="no"></span><span id="NO"></span>**No** (0)


</dt> <dd>

La cuenta que se está usando no tiene acceso de administrador al servidor de licencias.

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Sí** (1)


</dt> <dd>

La cuenta que se está usando tiene acceso de administrador al servidor de licencias.

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>No **sé** (2)


</dt> <dd>

No se puede determinar si la cuenta que se está usando tiene acceso de administrador al servidor de licencias.

</dd> </dl>

</dd> <dt>

**IsLSAvailable**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servidor de licencias está disponible (si se \[ puede establecer una conexión RPC de llamada a procedimiento remoto \] en el servidor).

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)


</dt> <dd>

El servidor de licencias no está disponible.

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponible** (1)


</dt> <dd>

El servidor de licencias está disponible.

</dd> </dl>

</dd> <dt>

**IssuingCALs**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se permite que el servidor de licencias emita Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS) en el servidor host de sesión de escritorio remoto.

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**No permitido** (0)


</dt> <dd>

No se permite que el servidor de licencias emita cal de RDS en el servidor host de sesión de escritorio remoto.

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Permitido** (1)


</dt> <dd>

El servidor de licencias puede emitir cal de RDS para el servidor host de sesión de escritorio remoto.

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>No **sé** (2)


</dt> <dd>

No se puede determinar si el servidor de licencias tiene permiso para emitir cal de RDS en el servidor host de sesión de escritorio remoto.

</dd> </dl>

</dd> <dt>

**LicenseServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nombre del servidor de licencias Escritorio remoto detectado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes. En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C. En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6. En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



 

