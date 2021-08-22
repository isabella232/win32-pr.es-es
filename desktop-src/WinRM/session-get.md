---
title: Método Session.Get (WSManDisp.h)
description: Recupera el recurso especificado por el URI y devuelve una representación XML de la instancia actual del recurso.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Obtener método Windows administración remota
- Get method Windows Remote Management , Session object
- Objeto de sesión Windows administración remota, método Get
topic_type:
- apiref
api_name:
- Session.Get
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c983c5f95ddfa3acc88b85b383ec85ddf85f885293031fe9bc4e4e07c90850a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642565"
---
# <a name="sessionget-method"></a>Método Session.Get

Recupera el recurso especificado por el [*URI*](windows-remote-management-glossary.md) y devuelve una representación XML de la instancia actual del recurso.

## <a name="syntax"></a>Sintaxis


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*resourceUri* \[ En\]
</dt> <dd>

Identificador del recurso que se va a recuperar.

Este parámetro puede contener uno de los siguientes elementos:

-   URI con o sin [*selectores*](windows-remote-management-glossary.md). Al llamar al **método Get** con un selector para obtener un recurso WMI, use la propiedad de clave o las propiedades del objeto . Por ejemplo, en el siguiente ejemplo Visual Basic código de Scripting Edition (VBScript), la clave se especifica mediante `Win32_Service?Name=winmgmt` . Para las clases singleton, como [**Win32 \_ LocalTime,**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)no se puede usar un selector.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   Objeto [**ResourceLocator**](resourcelocator.md) que puede contener selectores, [*fragmentos*](windows-remote-management-glossary.md)u [*opciones*](windows-remote-management-glossary.md).
-   Una [*referencia de punto de conexión WS-Addressing*](windows-remote-management-glossary.md) como se describe en el estándar WS-Management protocolo. Para obtener más información sobre la especificación pública [para protocolo WS-Management](ws-management-protocol.md), vea Página de índice [de especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*flags* \[ in, opcional\]
</dt> <dd>

Reservado. Se debe establecer en 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Representación XML del recurso.

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se recupera la representación XML de la instancia del servicio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) que representa el servicio Winmgmt de WMI en el equipo local.


```VB

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/" _ 
    & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub

```



En el ejemplo de código de VBScript siguiente se recupera la instancia del servicio Winmgmt de WMI de un equipo remoto. El equipo remoto se identifica mediante el nombre de dominio completo (servername.domain.com). La única diferencia entre la versión local y la remota es la especificación del equipo remoto en la llamada a [**WSMan.CreateSession**](wsman-createsession.md).


```VB
Const RemoteComputer = "servername.domain.com"

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Dim objSession
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/" _ 
    & "Win32_Service?Name=winmgmt"


On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sesión**](session.md)
</dt> </dl>

 

