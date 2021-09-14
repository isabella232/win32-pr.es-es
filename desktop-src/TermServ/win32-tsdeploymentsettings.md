---
title: Win32_TSDeploymentSettings clase
description: Define la configuración predeterminada que el Administrador de RemoteApp usa al crear Protocolo de escritorio remoto (RDP).
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentSettings clase Servicios de Escritorio remoto
- Win32_TSDeploymentSettings clase Servicios de Escritorio remoto , descrita
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172781"
---
# <a name="win32_tsdeploymentsettings-class"></a>Clase \_ TSDeploymentSettings de Win32

Define la configuración predeterminada que el Administrador de RemoteApp usa al crear Protocolo de escritorio remoto (RDP). Esta configuración no afecta a las aplicaciones o escritorios publicados.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a>Members

La **clase \_ TSDeploymentSettings de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TSDeploymentSettings de Win32** tiene estas propiedades.

<dl> <dt>

**AllowFontSmoothing**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si se permite el suavizado de fuentes.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Descripción breve (cadena de una línea) del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CertificateExpiresOn**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Fecha en que expira el certificado. Este valor se almacena como un formato [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) de 64 bits.

</dd> <dt>

**CertificateHash**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Huella digital del certificado que se usa para firmar archivos RDP.

</dd> <dt>

**CertificateIssuedBy**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Especifica quién emite el certificado.

</dd> <dt>

**CertificateIssuedTo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Especifica a quién se emite el certificado.

</dd> <dt>

**ColorBitDepth**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Profundidad de bits de color de la pantalla. Los valores posibles son 4, 8, 15, 16, 24 y 32.

</dd> <dt>

**CustomRDPSettings**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Contenido del archivo RDP que se corresponde con el rdp personalizado Configuración en Administrador de RemoteApp.

</dd> <dt>

**DeploymentRDPSettings**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Contenido del archivo RDP que corresponde a la configuración de implementación de Administrador de RemoteApp. Si se establece este valor, la configuración de implementación de RDP sustituye a la configuración predeterminada de esta clase. Por ejemplo, si establece la propiedad **GatewayAuthMode** en esta clase y establece la propiedad **DeploymentRDPSettings,** se omitirá la propiedad **GatewayAuthMode** de esta clase y se usará el valor **GatewayAuthMode** de **DeploymentRDPSettings.**

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

El nombre del servidor host de sesión de Escritorio remoto o el nombre de dominio completo (FQDN) de la granja de servidores host de sesión de Escritorio remoto.

</dd> <dt>

**GatewayAuthMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

El método de autenticación de puerta de enlace de Escritorio remoto. Los siguientes valores son posibles.

<dt>

0
</dt> <dd>

Contraseña

</dd> <dt>

1
</dt> <dd>

Tarjeta inteligente

</dd> <dt>

4
</dt> <dd>

Permitir que el usuario seleccione durante la conexión.

</dd> </dl>

</dd> <dt>

**GatewayName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Nombre del servidor de puerta de enlace de Escritorio remoto que se usará.

</dd> <dt>

**GatewayUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si se debe usar un servidor de puerta de enlace de Escritorio remoto para conectarse al servidor host de sesión de Escritorio remoto de destino a través de un firewall. Los siguientes valores son posibles.

<dt>

0
</dt> <dd>

No use un servidor de puerta de enlace de Escritorio remoto.

</dd> <dt>

1
</dt> <dd>

Use un servidor de puerta de enlace de Escritorio remoto. Omita el servidor de puerta de enlace de Escritorio remoto para las direcciones locales.

</dd> <dt>

2
</dt> <dd>

Use un servidor de puerta de enlace de Escritorio remoto.

</dd> <dt>

3
</dt> <dd>

Detecte automáticamente la configuración del servidor de puerta de enlace de Escritorio remoto.

</dd> </dl>

</dd> <dt>

**GatewayUseCachedCreds**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Cuando sea posible, use las mismas credenciales de usuario para el servidor de puerta de enlace de Escritorio remoto y el servidor host de sesión de Escritorio remoto.

</dd> <dt>

**HasCertificate**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si se debe usar un certificado para firmar los archivos RDP.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Fecha en que se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Puerto**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Puerto RDP que se usará.

</dd> <dt>

**RedirectionOptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Especifica las opciones de redireccionamiento de dispositivos y recursos para las conexiones RemoteApp. Se pueden combinar **marcas para RedirectionOptions.** Los valores siguientes son posibles.

<dt>

0
</dt> <dd>

Sin redireccionamiento de dispositivos o recursos.

</dd> <dt>

1
</dt> <dd>

Redirigir unidades de disco.

</dd> <dt>

2
</dt> <dd>

Redirigir impresoras.

</dd> <dt>

4
</dt> <dd>

Redirija el Portapapeles.

</dd> <dt>

8
</dt> <dd>

Redirección compatible con Plug and Play dispositivos.

</dd> <dt>

16
</dt> <dd>

Redirigir tarjetas inteligentes.

</dd> <dt>

32
</dt> <dd>

Redirija el audio.

</dd> <dt>

64
</dt> <dd>

Redirigir puertos serie.

</dd> </dl>

</dd> <dt>

**RequireServerAuth**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si se debe requerir la autenticación del servidor.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente pero predecir un error en un futuro próximo). Los estados no operativo incluyen: "Error", "Starting", "Stopping" y "Service". El último, "Servicio", podría aplicarse durante la resilvering de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "correcto" ni está en uno de los demás estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>



 ("Ok")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconocido")


</dt> <dd></dd> <dt>



 ("Error previo")


</dt> <dd></dd> <dt>



 ("Starting")


</dt> <dd></dd> <dt>



 ("Deteniendo")


</dt> <dd></dd> <dt>



 ("Servicio")


</dt> <dd></dd> </dl>

</dd> <dt>

**UseMultimon**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si hay varios monitores habilitados para el escritorio.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para establecer propiedades mediante esta clase.

Si **RequireServerAuth está** establecido en **TRUE,** tenga en cuenta lo siguiente:

-   Si el programa RemoteApp es para uso de intranet y todos los equipos cliente ejecutan Windows Server 2008 o Windows Vista, no es necesario configurar el servidor host de sesión de Escritorio remoto para que use un certificado SSL. En este caso, se usa la Autenticación a nivel de red.
-   Debe especificar el FQDN del servidor o la granja para el valor de la **propiedad FarmName.**

Para conectarse al espacio de nombres \\ "CIMV2 TerminalServices", el nivel de autenticación debe incluir privacidad de paquetes. Para las llamadas de C/C++, se trata de un nivel de autenticación de **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**, que se puede establecer mediante la función COM [**CoSetProxyBlanket.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) Para Visual Basic y llamadas de scripting, se trata de un nivel de autenticación **de WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6. En el ejemplo Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Se instalan en el equipo cuando se agrega el rol asociado. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow.mof</dt> </dl>  |
| Archivo DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



 

