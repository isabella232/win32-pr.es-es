---
title: Propiedad Session.Timeout (WSManDisp.h)
description: Establece y obtiene la cantidad máxima de tiempo, en milisegundos, que la aplicación cliente espera a que Windows administración remota complete sus operaciones.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Propiedad Timeout Windows Administración remota
- Propiedad Timeout Windows remote management , objeto Session
- Objeto de sesión Windows administración remota, propiedad Timeout
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4731e4f76ee890bc925a14b69c8ffb3d50e47406939b76183359021242a5fadc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743246"
---
# <a name="sessiontimeout-property"></a>Propiedad Session.Timeout

Establece y obtiene la cantidad máxima de tiempo, en milisegundos, que la aplicación cliente espera a que Windows administración remota complete sus operaciones.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
Session.Timeout As long
```



## <a name="property-value"></a>Valor de propiedad

Valor de tiempo de espera, en milisegundos. Cuando se supera el valor de tiempo de espera, se produce un error en tiempo de ejecución.

## <a name="remarks"></a>Comentarios

El valor de tiempo de espera se puede establecer antes de cada operación realizada por el agente. Si no se especifica un valor de tiempo de espera, el agente establece el valor de tiempo de espera.

Durante una operación de enumeración, no se puede restablecer el valor de tiempo de espera mientras se enumera el recurso.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se inicia Calc.exe proceso mediante el [**método Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la clase [**Process win32 \_ de**](/windows/desktop/CIMWin32Prov/win32-process) WMI. El *parámetro strInputParameters* contiene los parámetros de entrada en formato XML. El script especifica un tiempo de espera para la sesión.


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
    "wmi/root/cimv2/Win32_Process"

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

strInputParameters = "<p:Create_INPUT " & _
    "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Process"">" & _
    "<p:CommandLine>" & "calc.exe" & _
    "</p:CommandLine>" & _
    "</p:Create_INPUT>"

strOutputParameters = objSession.Invoke( "Create", _
    strResource, strInputParameters )

DisplayOutput( strOutputParameters )

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

