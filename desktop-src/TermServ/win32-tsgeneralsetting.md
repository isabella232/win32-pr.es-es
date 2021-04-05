---
title: Win32_TSGeneralSetting class (Clase Win32_TSGeneralSetting)
description: Representa la configuración general del terminal como el nivel de cifrado y el protocolo de transporte.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Win32_TSGeneralSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGeneralSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172f18bbddd364d74dfcfb00e7e665628267af36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802480"
---
# <a name="win32_tsgeneralsetting-class"></a>\_Clase Win32 TSGeneralSetting

La clase WMI **\_ TSGeneralSetting de Win32** representa la configuración general del terminal como el nivel de cifrado y el protocolo de transporte.

La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético. Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a>Miembros

La **clase \_ TSGeneralSetting de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ TSGeneralSetting** tiene estos métodos.



| Método                                                                                        | Descripción                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)                       | Establece el nivel de cifrado.<br/>                                                                                                                                   |
| [**SetSecurityLayer**](win32-tsgeneralsetting-setsecuritylayer.md)                           | Establece el nivel de seguridad en uno de "nivel de seguridad RDP" (0), "Negotiate" (1) o "SSL" (2).<br/>                                                                   |
| [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) | Habilita o deshabilita el requisito de que los usuarios se deben autenticar en el momento de la conexión estableciendo el valor de la propiedad **UserAuthenticationRequired** .<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ TSGeneralSetting de Win32** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Descripción breve (cadena de una línea) del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**CertificateName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del nombre de sujeto del certificado personal del equipo local.

</dd> <dt>

**Certificados**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Contiene un almacén de certificados serializado que contiene todos los certificados del almacén de **cuentas de usuario** del equipo que son certificados de servidor válidos para su uso con la capa de sockets seguros (SSL).

</dd> <dt>

**Comentario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nombre descriptivo de la combinación de nivel de sesión y Protocolo de transporte.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Fecha en que se instaló el objeto. La falta de un valor no indica que el objeto no está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**MinEncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **bajo** ("solo los datos enviados del cliente al servidor están protegidos por cifrado según el nivel de clave estándar del servidor. Los datos enviados desde el servidor al cliente no están protegidos. "), **medio** (" todos los datos enviados entre el servidor y el cliente están protegidos por cifrado según el nivel de clave estándar del servidor. "), **alto** (" todos los datos enviados entre el servidor y el cliente están protegidos con el nivel máximo de clave del servidor basado en cifrado ").
</dt> </dl>

El nivel mínimo de cifrado.

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bajo** (1)


</dt> <dd>

Bajo nivel de cifrado. Solo los datos enviados desde el cliente al servidor se cifran mediante el cifrado de 56 bits. Tenga en cuenta que no se cifran los datos enviados desde el servidor al cliente.

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Medio/cliente compatible** (2)


</dt> <dd>

Nivel de cifrado compatible con el cliente. Todos los datos enviados del cliente al servidor y del servidor al cliente se cifran con el nivel de clave máximo admitido por el cliente.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (3)


</dt> <dd>

Alto nivel de cifrado. Todos los datos enviados del cliente al servidor y del servidor al cliente se cifran mediante cifrado de 128 bits seguro. Los clientes que no admiten este nivel de cifrado no se pueden conectar.

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Compatible con FIPS** (4)


</dt> <dd>

Cifrado compatible con FIPS. Todos los datos enviados del cliente al servidor y del servidor al cliente están cifrados y descifrados con los algoritmos de cifrado de Estándar federal de procesamiento de información (FIPS) mediante los módulos criptográficos de Microsoft. FIPS es un estándar titulado "requisitos de seguridad para los módulos criptográficos". FIPS 140-1 (1994) y FIPS 140-2 (2001) describen los requisitos gubernamentales para los módulos criptográficos de hardware y software que se usan en el gobierno de EE. UU.

</dd> </dl>

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**PolicySourceMinEncryptionLevel**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **MinEncryptionLevel** está configurada por el servidor, por la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceSecurityLayer**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **SecurityLayer** está configurada por el servidor, por la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**PolicySourceUserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la propiedad **UserAuthenticationRequired** está configurada por el servidor, por la Directiva de grupo o de forma predeterminada.

<dt>

0 (0X0)
</dt> <dd>

Servidor

</dd> <dt>

1 (0x1)
</dt> <dd>

Directiva de grupo

</dd> <dt>

2 (0X2)
</dt> <dd>

Valor predeterminado

</dd> </dl>

</dd> <dt>

**SecurityLayer**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **RDPSecurityLayer** ("capa de seguridad de RDP: comunicación entre serverand el cliente usará el cifrado RDP nativo"), **Negotiate** ("se usará la capa más segura compatible con el cliente. Si se admite, se usará TLS 1,0. "), se usará **SSL** (" SSL (TLS 1,0) para la autenticación del servidor, así como forencrypting todos los datos transferidos entre el servidor y el cliente. Esta configuración requiere que el servidor tenga un certificado compatible con SSL. "), **NEWTBD** (" un nuevo nivel de seguridad en Longhorn ").
</dt> </dl>

Especifica el nivel de seguridad utilizado entre el cliente y el servidor.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Nivel de seguridad de RDP** (1)


</dt> <dd>

La comunicación entre el servidor y el cliente usa el cifrado RDP nativo.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (2)


</dt> <dd>

Se usa la capa más segura compatible con el cliente. Si se admite, se usa SSL (TLS 1,0).

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (3)


</dt> <dd>

SSL (TLS 1,0) se utiliza para la autenticación de servidor y para el cifrado de todos los datos transferidos entre el servidor y el cliente. Esta configuración requiere que el servidor tenga un certificado compatible con SSL. Esta configuración no es compatible con un valor de **MinEncryptionLevel** de 1.

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)


</dt> <dd>

Un nuevo nivel de seguridad.

</dd> </dl>

</dd> <dt>

**SSLCertificateSHA1Hash**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica el hash SHA1 en formato hexadecimal del certificado SSL que va a usar el servidor de destino.

La huella digital de un certificado puede encontrarse con el complemento MMC certificados en la pestaña detalles de la página Propiedades del certificado.

</dd> <dt>

**SSLCertificateSHA1HashType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el estado de la propiedad **SSLCertificateSHA1Hash** .

<dt>

0 (0X0)
</dt> <dd>

No válido

</dd> <dt>

1 (0x1)
</dt> <dd>

Autofirmado predeterminado

</dd> <dt>

2 (0X2)
</dt> <dd>

Directiva de grupo predeterminada aplicada

</dd> <dt>

3 (0X3)
</dt> <dd>

Personalizados

</dd> </dl>

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Estado actual del objeto. Se pueden definir varios Estados operativos y no operativos. Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo). Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio". El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

<dt>



 ("Correcto")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconocido")


</dt> <dd></dd> <dt>



 ("Pred FAIL")


</dt> <dd></dd> <dt>



 ("Iniciando")


</dt> <dd></dd> <dt>



 ("Deteniéndose")


</dt> <dd></dd> <dt>



 ("Servicio")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del terminal.

Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> <dt>

**TerminalProtocol**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del Protocolo de capa de sesión; por ejemplo, Microsoft RDP 5,0.

</dd> <dt>

**Transporte**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tipo de transporte utilizado en la conexión; por ejemplo, TCP, NetBIOS o IPX/SPX.

</dd> <dt>

**UserAuthenticationRequired**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de autenticación de usuario que se usa para las conexiones remotas. Si se establece en 1, lo que significa habilitado, **UserAuthenticationRequired** requiere autenticación de usuario en el momento de la conexión para aumentar la protección del servidor frente a ataques de red. Solo los clientes [Protocolo de escritorio remoto](remote-desktop-protocol.md) (RDP) que admiten la versión 6,0 o posterior de RDP pueden conectarse. Para evitar interrupciones para los usuarios remotos, se recomienda que implemente los clientes RDP que admitan la versión de protocolo adecuada antes de habilitar la propiedad.

Use el método [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) para habilitar o deshabilitar esta propiedad.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

La autenticación de usuario en la conexión está deshabilitada.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

La autenticación de usuario en la conexión está habilitada.

</dd> </dl>

</dd> <dt>

**WindowsAuthentication**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si la conexión tiene como valor predeterminado el proceso de autenticación de Windows estándar o un paquete de autenticación que se ha instalado en el sistema.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

No tiene como valor predeterminado el proceso de autenticación de Windows estándar.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Tiene como valor predeterminado el proceso de autenticación de Windows estándar.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta que las estaciones de ventana no asociadas a la sesión de consola no pueden tener acceso a los métodos y las propiedades de esta clase. Si se realiza un intento de hacerlo especificando "Console" como el valor de la propiedad TerminalName, los métodos de este objeto devolverán **WBEM \_ E \_ no \_ compatible**. También se devolverá este código de error si una estación de ventana intenta llamar a métodos de este objeto con el fin de agregar o modificar las propiedades de seguridad de las cuentas LocalSystem, LocalService o NetworkService.

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
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> </dl>

 

