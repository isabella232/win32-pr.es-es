---
title: Propiedad Session. error (WSManDisp. h)
description: Obtiene información de error adicional en una secuencia XML.
ms.assetid: f291c11c-012f-45eb-b851-5661d881ee79
ms.tgt_platform: multiple
keywords:
- Error de la propiedad Administración remota de Windows
- Propiedad error Administración remota de Windows, objeto Session
- Administración remota de Windows de objeto de sesión, propiedad error
topic_type:
- apiref
api_name:
- Session.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2568fb7f51d6970d3d98f8434357b22efb7793d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714653"
---
# <a name="sessionerror-property"></a>Session. error (propiedad)

Obtiene información de error adicional en una secuencia XML. La información de error también se puede obtener del objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) de VBScript.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Session.Error As BSTR
```



## <a name="property-value"></a>Valor de propiedad

Representación XML de la información de error.

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se muestra un script que contiene un error en el [*URI del recurso*](windows-remote-management-glossary.md). El URI de recurso correcto es `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_QuotaSetting?VolumePath=c:\\` .


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

strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_QuotaSetting"

On Error Resume Next
strResponse = objSession.Get( strResourceUri )
If Err.number <> 0 Then
    DisplayErrorInfo()
    strErrorXML = objSession.Error
    WScript.Echo strErrorXML
Else
    Call DisplayOutput(strResponse)
End If
On Error Goto 0

'*************************************************************
' Displays Error information from Err object and Session.Error
'*************************************************************
Sub DisplayErrorInfo()

    WScript.Echo "An error has occurred."     
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    Err.Clear
End Sub
```



El siguiente texto es la salida de error del script.

``` syntax
Number      : 0x803380FA
Description : The WinRM client cannot process the request. 
The resource URI is not valid: it does not contain keys, but
the class selected is not a singleton. To access an instance which 
is not a singleton, keys must be provided. Use the following 
command to get more information about how to construct a 
resource URI: "winrm help uris".
Source      : Session
HelpFile    :
HelpContext : 0
<f:WSManFault 
xmlns:f="http://schemas.microsoft.com/wbem/wsman/1/wsmanfault" 
Code="2150859002" Machine="Server1" xml:lang="en-US">
<f:Message>
<f:ProviderFault provider="WMIv1 plugin for Windows Remote Management " 
path="%systemroot%\system32\WsmWmiPl.dll">
<f:WSManFault 
xmlns:f="http://schemas.microsoft.com/wbem/wsman/1/wsmanfault" 
Code="2150859002" Machine="" xml:lang="en-US">
<f:Message>The WinRM client cannot process the request. 
The resource URI is not valid: it does not contain keys, but the 
class selected is not a singleton. To access an instance which is 
not a singleton, keys must be provided. Use the following command 
to get more information in how to construct a resource URI: 
&quot;winrm help uris&quot;. 
</f:Message></f:WSManFault>
</f:ProviderFault>
</f:Message
></f:WSManFault>
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

 

