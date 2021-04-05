---
title: Método Session. get (WSManDisp. h)
description: Recupera el recurso especificado por el URI y devuelve una representación XML de la instancia actual del recurso.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Método get Administración remota de Windows
- Método get Administración remota de Windows, objeto Session
- Administración remota de Windows de objeto de sesión, get (método)
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
ms.openlocfilehash: 7e4ee84cc711db312389151d1dd95fb890474dcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359802"
---
# <a name="sessionget-method"></a>Session. get (método)

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

*resourceUri* \[ de\]
</dt> <dd>

Identificador del recurso que se va a recuperar.

Este parámetro puede contener uno de los siguientes elementos:

-   Un URI con o sin [*selectores*](windows-remote-management-glossary.md). Al llamar al método **Get** con un selector para obtener un recurso WMI, utilice la propiedad o propiedades de clave del objeto. Por ejemplo, en el siguiente ejemplo de código de Visual Basic Scripting Edition (VBScript), la clave se especifica mediante `Win32_Service?Name=winmgmt` . En el caso de las clases singleton, como [**\_ localtime de Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), no se puede utilizar un selector.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   Un objeto [**ResourceLocator**](resourcelocator.md) que puede contener selectores, [*fragmentos*](windows-remote-management-glossary.md)u [*Opciones*](windows-remote-management-glossary.md).
-   Una referencia de extremo de [*WS-Addressing*](windows-remote-management-glossary.md) como se describe en el estándar del protocolo WS-Management. Para obtener más información sobre la especificación pública de [protocolo WS-Management](ws-management-protocol.md), consulte la [Página de índice de especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*marcas* \[ de en, opcional\]
</dt> <dd>

Reservado. Se debe establecer en 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Representación XML del recurso.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se recupera la representación XML de la instancia de [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service) que representa el servicio WMI WinMgmt en el equipo local.


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



El siguiente ejemplo de código de VBScript recupera la instancia de servicio de WMI WinMgmt de un equipo remoto. El equipo remoto se identifica mediante el nombre de dominio completo (servername.domain.com). La única diferencia entre la versión local y la remota es la especificación del equipo remoto en la llamada a [**WSMan. createSession**](wsman-createsession.md).


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



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**De sesión**](session.md)
</dt> </dl>

 

