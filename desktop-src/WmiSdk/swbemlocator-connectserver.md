---
description: Se conecta al espacio de nombres en el equipo especificado en el parámetro strServer.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: Método SWbemLocator.ConnectServer (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4153a5761d59c54cf8635202adcca0ddf72603022ebf8dbb5b160231c90e49e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955215"
---
# <a name="swbemlocatorconnectserver-method"></a>Método SWbemLocator.ConnectServer

El **método ConnectServer** del objeto [**SWbemLocator**](swbemlocator.md) se conecta al espacio de nombres del equipo especificado en el *parámetro strServer.* El equipo de destino puede ser local o remoto, pero debe tener INSTALADO WMI. Para obtener ejemplos y una comparación con el tipo de moniker de conexión, vea [Crear un script WMI.](creating-a-wmi-script.md)

A partir Windows Vista, **SWbemLocator.ConnectServer** puede conectarse con equipos que ejecutan IPv6 mediante una dirección IPv6 en el *parámetro strServer.* Para obtener más información, vea [Compatibilidad con IPv6 e IPv4 en WMI.](ipv6-and-ipv4-support-in-wmi.md)

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strServer* \[ en, opcional\]
</dt> <dd>

Nombre de equipo al que se va a conectar. Si el equipo remoto está en un dominio diferente al de la cuenta de usuario con la que inicia sesión, use el nombre completo del equipo. Si no proporciona este parámetro, la llamada se establece de forma predeterminada en el equipo local.

Ejemplo: `server1.network.fabrikam`

También puede usar una dirección IP en este parámetro. Si la dirección IP está en formato IPv6, el equipo de destino debe ejecutar IPv6. Una dirección en IPv4 es similar a `123.123.123.123`

Una dirección IP en formato IPv6 es similar a `2010:836B:4179::836B:4179`

Para obtener más información sobre DNS e IPv4, consulte la sección Comentarios.

</dd> <dt>

*strNamespace* \[ en, opcional\]
</dt> <dd>

Cadena que especifica el espacio de nombres en el que se inicia sesión. Por ejemplo, para iniciar sesión en el espacio de \\ nombres predeterminado raíz, use root \\ default. Si no especifica este parámetro, el valor predeterminado es el espacio de nombres configurado como espacio de nombres predeterminado para el scripting. Para obtener más información, vea [Crear una aplicación WMI o script](creating-a-wmi-application-or-script.md).

Ejemplo: \\ "root CIMV2"

</dd> <dt>

*strUser* \[ en, opcional\]
</dt> <dd>

Nombre de usuario que se usará para conectarse. La cadena puede tener el formato de nombre de usuario o nombre de usuario \\ de dominio. Deje este parámetro en blanco para usar el contexto de seguridad actual. El *parámetro strUser* solo debe usarse con conexiones a servidores WMI remotos. Si intenta especificar *strUser para una* conexión WMI local, se produce un error en el intento de conexión. Si la autenticación Kerberos está en uso, el nombre de usuario y la contraseña especificados en *strUser* y *strPassword* no se pueden interceptar en una red. Puede usar el formato UPN para especificar *strUser*.

Ejemplo: "DomainName \\ UserName"

> [!Note]  
> Si se especifica un dominio en *strAuthority*, el dominio no se debe especificar aquí. Si se especifica el dominio en ambos parámetros, se produce un error de parámetro no válido.

 

</dd> <dt>

*strPassword* \[ en, opcional\]
</dt> <dd>

Cadena que especifica la contraseña que se usará al intentar conectarse. Deje el parámetro en blanco para usar el contexto de seguridad actual. El *parámetro strPassword* solo debe usarse con conexiones a servidores WMI remotos. Si intenta especificar *strPassword* para una conexión WMI local, se produce un error en el intento de conexión. Si la autenticación Kerberos está en uso, el nombre de usuario y la contraseña especificados en *strUser* y *strPassword* no se pueden interceptar en la red.

</dd> <dt>

*strLocale* \[ en, opcional\]
</dt> <dd>

Cadena que especifica el código de localización. Si desea usar la configuración regional actual, déjela en blanco. Si no está en blanco, este parámetro debe ser una cadena que indique la configuración regional deseada donde se debe recuperar la información. Para los identificadores de configuración regional de Microsoft, el formato de la cadena es "MS xxxx", donde xxxx es una cadena en formato hexadecimal que \_ indica el LCID. Por ejemplo, el inglés estadounidense aparecería como "MS \_ 409".

</dd> <dt>

*strAuthority* \[ en, opcional\]
</dt> <dd>

<dt>

""
</dt> <dd>

Este parámetro es opcional. Sin embargo, si se especifica, solo se puede usar Kerberos o NTLMDomain.

</dd> <dt>

Kerberos:
</dt> <dd>

Si el *parámetro strAuthority* comienza con la cadena "Kerberos:", se usa la autenticación Kerberos y este parámetro debe contener un nombre principal de Kerberos. El nombre principal de Kerberos se especifica como Kerberos:*dominio*, por ejemplo, donde es el servidor al `Kerberos:fabrikam` que está `fabrikam` intentando conectarse.

Ejemplo: "Kerberos:DOMAIN"

</dd> <dt>

NTLMDomain:
</dt> <dd>

Para usar la autenticación NT Lan Manager (NTLM), debe especificarla como NTLMDomain:*dominio*, por ejemplo, donde es el `NTLMDomain:fabrikam` nombre del `fabrikam` dominio.

Ejemplo: "NTLMDomain:DOMAIN"

</dd> </dl>

Si deja este parámetro en blanco, el sistema operativo negocia con COM para determinar si se usa la autenticación NTLM o Kerberos. Este parámetro solo debe usarse con conexiones a servidores WMI remotos. Si intenta establecer la autoridad para una conexión WMI local, se produce un error en el intento de conexión.

> [!Note]  
> Si el dominio se especifica en *strUser*, que es la ubicación preferida, no se debe especificar aquí. Si se especifica el dominio en ambos parámetros, se produce un error de parámetro no válido.

 

</dd> <dt>

*iSecurityFlags* \[ en, opcional\]
</dt> <dd>

Se usa para pasar valores de marca **a ConnectServer.**

<dt>

0 (0x0)
</dt> <dd>

Un valor de 0 para este parámetro hace que la llamada a **ConnectServer** devuelva solo una vez establecida la conexión al servidor. Esto podría hacer que el programa dejara de responder indefinidamente si no se puede establecer la conexión.

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait** (128 (0x80))


</dt> <dd>

Se garantiza que la llamada a **ConnectServer** volverá en 2 minutos o menos. Use esta marca para evitar que el programa ceja para responder indefinidamente si no se puede establecer la conexión.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ en, opcional\]
</dt> <dd>

Normalmente, esto es indefinido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que está atendiendo la solicitud. Un proveedor que admita o requiera dicha información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, WMI devuelve un objeto [**SWbemServices**](swbemservices.md) enlazado al espacio de nombres especificado en *strNamespace* en el equipo especificado en *strServer*.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **ConnectServer,** el [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied:** 2147749891 (0x80041003)
</dt> <dd>

El nombre de usuario y la contraseña actuales o especificados no eran válidos ni estaban autorizados para realizar la conexión.

</dd> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidNamespace:** 2147749902 (0x8004100E)
</dt> <dd>

El espacio de nombres especificado no existía en el servidor.

</dd> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido o no se pudo analizar el espacio de nombres.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para completar la operación.

</dd> <dt>

**wbemErrTransportFailure:** 2147749909
</dt> <dd>

Se ha producido un error de red que impide el funcionamiento normal.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **método ConnectServer** se usa a menudo al conectarse a una cuenta con un nombre de usuario y una contraseña diferentes en un equipo remoto porque no se puede especificar una contraseña diferente en una cadena [de moniker.](constructing-a-moniker-string.md) Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

El uso de una dirección IPv4 para conectarse a un servidor remoto puede provocar un comportamiento inesperado. La causa probable es que haya entradas DNS obsoletas en su entorno. En estas circunstancias, se usará la entrada PTR obsoleta de la máquina, con resultados impredecibles. Para evitar este comportamiento, puede anexar un punto (".") a la dirección IP antes de llamar a ConnectServer. Esto hace que se produce un error en la búsqueda inversa de DNS, pero puede permitir que la llamada **a ConnectServer** se haga correctamente en el equipo correcto.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se describe cómo conectarse a un equipo remoto para obtener datos [**\_ de Win32 IP4RouteTable.**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) El nombre de dominio especificado en *strDomain* se usa en *strAuthority*.


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



El siguiente fragmento de código de PowerShell accede a un servidor remoto y enumera las clases WMI disponibles.


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Crear un script WMI](creating-a-wmi-script.md)
</dt> </dl>

 

