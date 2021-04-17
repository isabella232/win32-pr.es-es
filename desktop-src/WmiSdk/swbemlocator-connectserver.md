---
description: Se conecta al espacio de nombres en el equipo especificado en el parámetro strServer.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: Método SWbemLocator. ConnectServer (Wbemdisp. h)
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
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697684"
---
# <a name="swbemlocatorconnectserver-method"></a>SWbemLocator. ConnectServer, método

El método **ConnectServer** del objeto [**SWbemLocator**](swbemlocator.md) se conecta al espacio de nombres en el equipo especificado en el parámetro *strServer* . El equipo de destino puede ser local o remoto, pero debe tener WMI instalado. Para obtener ejemplos y una comparación con el tipo de moniker de conexión, vea [crear un script WMI](creating-a-wmi-script.md).

A partir de Windows Vista, **SWbemLocator. ConnectServer** puede conectarse con equipos que ejecutan IPv6 mediante una dirección IPv6 en el parámetro *strServer* . Para obtener más información, consulte [compatibilidad con IPv6 e IPv4 en WMI](ipv6-and-ipv4-support-in-wmi.md).

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

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

Nombre del equipo al que se está conectando. Si el equipo remoto está en un dominio diferente al de la cuenta de usuario en la que inicia sesión, use el nombre de equipo completo. Si no proporciona este parámetro, la llamada tiene como valor predeterminado el equipo local.

Ejemplo: `server1.network.fabrikam`

También puede usar una dirección IP en este parámetro. Si la dirección IP está en formato IPv6, el equipo de destino debe ejecutar IPv6. Una dirección en IPv4 tiene el siguiente aspecto `123.123.123.123`

Una dirección IP en formato IPv6 tiene el siguiente aspecto `2010:836B:4179::836B:4179`

Para obtener más información sobre DNS e IPv4, consulte la sección Comentarios.

</dd> <dt>

*strNamespace* \[ en, opcional\]
</dt> <dd>

Cadena que especifica el espacio de nombres en el que se inicia la sesión. Por ejemplo, para iniciar sesión en el \\ espacio de nombres predeterminado raíz, use la raíz \\ predeterminada. Si no se especifica este parámetro, el valor predeterminado es el espacio de nombres configurado como espacio de nombres predeterminado para el scripting. Para obtener más información, vea [crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md).

Ejemplo: "root \\ cimv2"

</dd> <dt>

*strUser* \[ en, opcional\]
</dt> <dd>

Nombre de usuario que se va a usar para conectarse. La cadena puede tener la forma de un nombre de usuario o un nombre de usuario de dominio \\ . Deje este parámetro en blanco para utilizar el contexto de seguridad actual. El parámetro *strUser* solo debe usarse con conexiones a servidores WMI remotos. Si intenta especificar *strUser* para una conexión WMI local, se producirá un error en el intento de conexión. Si la autenticación Kerberos está en uso, el nombre de usuario y la contraseña que se especifican en *strUser* y *strPassword* no se pueden interceptar en una red. Puede usar el formato UPN para especificar *strUser*.

Ejemplo: "nombreDeDominio \\ nombreDeUsuario"

> [!Note]  
> Si se especifica un dominio en *strAuthority*, el dominio no debe especificarse aquí. Si se especifica el dominio en ambos parámetros, se producirá un error de parámetro no válido.

 

</dd> <dt>

*strPassword* \[ en, opcional\]
</dt> <dd>

Cadena que especifica la contraseña que se va a usar al intentar conectarse. Deje el parámetro en blanco para utilizar el contexto de seguridad actual. El parámetro *strPassword* solo debe usarse con conexiones a servidores WMI remotos. Si intenta especificar *strPassword* para una conexión WMI local, se producirá un error en el intento de conexión. Si se usa la autenticación Kerberos, el nombre de usuario y la contraseña que se especifican en *strUser* y *strPassword* no se pueden interceptar en la red.

</dd> <dt>

*strLocale* \[ en, opcional\]
</dt> <dd>

Cadena que especifica el código de localización. Si desea usar la configuración regional actual, déjela en blanco. Si no está en blanco, este parámetro debe ser una cadena que indica la configuración regional deseada en la que se debe recuperar la información. En el caso de los identificadores de configuración regional de Microsoft, el formato de la cadena es "MS \_ xxxx", donde XXXX es una cadena en formato hexadecimal que indica el LCID. Por ejemplo, el inglés americano aparecería como "MS \_ 409".

</dd> <dt>

*strAuthority* \[ en, opcional\]
</dt> <dd>

<dt>

""
</dt> <dd>

Este parámetro es opcional. Sin embargo, si se especifica, solo se puede usar Kerberos o NTLMDomain.

</dd> <dt>

V5
</dt> <dd>

Si el parámetro *strAuthority* comienza con la cadena "Kerberos:", se usa la autenticación Kerberos y este parámetro debe contener un nombre de entidad de seguridad Kerberos. El nombre de la entidad de seguridad de Kerberos se especifica como Kerberos:*dominio*, por ejemplo, `Kerberos:fabrikam` donde `fabrikam` es el servidor al que está intentando conectarse.

Ejemplo: "Kerberos: dominio"

</dd> <dt>

NTLMDomain
</dt> <dd>

Para usar la autenticación de NT LAN Manager (NTLM), debe especificarla como NTLMDomain:*Domain*, como, por ejemplo, `NTLMDomain:fabrikam` donde `fabrikam` es el nombre del dominio.

Ejemplo: "NTLMDomain: dominio"

</dd> </dl>

Si deja este parámetro en blanco, el sistema operativo negocia con COM para determinar si se utiliza la autenticación NTLM o Kerberos. Este parámetro solo debe usarse con conexiones a servidores WMI remotos. Si intenta establecer la autoridad para una conexión WMI local, se producirá un error en el intento de conexión.

> [!Note]  
> Si el dominio se especifica en *strUser*, que es la ubicación preferida, no debe especificarse aquí. Si se especifica el dominio en ambos parámetros, se producirá un error de parámetro no válido.

 

</dd> <dt>

*iSecurityFlags* \[ en, opcional\]
</dt> <dd>

Se usa para pasar valores de marca a **ConnectServer**.

<dt>

0 (0X0)
</dt> <dd>

Un valor de 0 para este parámetro hace que la llamada a **ConnectServer** se devuelva solo después de que se establezca la conexión al servidor. Esto podría hacer que el programa dejara de responder indefinidamente si no se puede establecer la conexión.

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait * * * * (128 (0x80))


</dt> <dd>

Se garantiza que la llamada a **ConnectServer** se devuelve en 2 minutos o menos. Utilice esta marca para evitar que el programa deje de responder indefinidamente si no se puede establecer la conexión.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ en, opcional\]
</dt> <dd>

Normalmente, esto no está definido. De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que atiende la solicitud. Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si es correcto, WMI devuelve un objeto [**SWbemServices**](swbemservices.md) que está enlazado al espacio de nombres especificado en *strNamespace* en el equipo que se especifica en *strServer*.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **ConnectServer** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

El nombre de usuario y la contraseña actuales o especificados no son válidos o están autorizados para realizar la conexión.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrInvalidNamespace** -2147749902 (0x8004100E)
</dt> <dd>

El espacio de nombres especificado no existía en el servidor.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Se especificó un parámetro no válido o no se pudo analizar el espacio de nombres.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insuficiente para completar la operación.

</dd> <dt>

**wbemErrTransportFailure** -2147749909
</dt> <dd>

Se produjo un error de red que impide el funcionamiento normal.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método **ConnectServer** se usa a menudo al conectarse a una cuenta con un nombre de usuario y unas credenciales de contraseña diferentes en un equipo remoto, ya que no se puede especificar una contraseña diferente en una cadena de [moniker](constructing-a-moniker-string.md) . Para obtener más información, consulte [Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md) (puede estar en inglés).

El uso de una dirección IPv4 para conectarse a un servidor remoto puede producir un comportamiento inesperado. La causa probable es que las entradas DNS estén obsoletas en su entorno. En estas circunstancias, se usará la entrada PTR obsoleta para el equipo, con resultados imprevisibles. Para evitar este comportamiento, puede anexar un punto (".") a la dirección IP antes de llamar a ConnectServer. Esto hace que se produzca un error en la búsqueda inversa de DNS, pero puede permitir que la llamada **ConnectServer** se realice correctamente en el equipo correcto.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se describe cómo conectarse a un equipo remoto para obtener datos de [**\_ IP4RouteTable de Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) . El nombre de dominio que se especifica en *strDomain* se usa en *strAuthority*.


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
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | \_ISWBEMLOCATOR IID<br/>                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[Conexión a WMI en un equipo remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Creación de un script de WMI](creating-a-wmi-script.md)
</dt> </dl>

 

