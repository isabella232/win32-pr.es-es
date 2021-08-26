---
title: Método Session.Put (WSManDisp.h)
description: Actualiza un recurso.
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Put method Windows Remote Management
- Put method Windows Remote Management , Session object
- Objeto de sesión Windows administración remota , Método Put
topic_type:
- apiref
api_name:
- Session.Put
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c6fc6123470f6633b77a1c51234e751f3be04044c0ad100f0017849cb1ac42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898695"
---
# <a name="sessionput-method"></a>Método Session.Put

Actualiza un recurso.

## <a name="syntax"></a>Sintaxis


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*resourceUri* \[ En\]
</dt> <dd>

Identificador del recurso que se va a actualizar.

Este parámetro puede contener uno de los elementos incluidos en la lista siguiente:

-   URI con o sin [*selectores*](windows-remote-management-glossary.md). Al llamar al **método Put** para obtener un recurso WMI, use la propiedad o las propiedades de clave del objeto . Por ejemplo, en el siguiente Visual Basic de código de Scripting Edition (VBScript), la clave se especifica mediante `Win32_Service?Name=winmgmt` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   [**Objeto ResourceLocator**](resourcelocator.md) que puede contener selectores, [*fragmentos*](windows-remote-management-glossary.md)u [*opciones*](windows-remote-management-glossary.md).
-   [*Referencia del punto de conexión WS-Addressing,*](windows-remote-management-glossary.md) tal como se describe en [el protocolo WS-Management](ws-management-protocol.md) estándar. Para obtener más información sobre la especificación pública para el protocolo WS-Management, vea Página de índice de [especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*recurso* \[ En\]
</dt> <dd>

Contenido del recurso actualizado.

</dd> <dt>

*flags* \[ en, opcional\]
</dt> <dd>

Reservado. Se debe establecer en 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

XML que contiene el contenido del recurso actualizado.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se escriben datos en el [**objeto \_ WMISetting de Win32.**](/windows/desktop/CIMWin32Prov/win32-wmisetting) Debe incluir todas las propiedades que no son de matriz del objeto en el XML del *parámetro Resource.* El orden de las propiedades no es significativo.


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

'Change the property value by putting
'the new XML content into the resource.
Dim strResourceUri, strReturnedResourceUri, newXmlContent
strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
  & "wmi/root/cimv2/Win32_WMISetting"
newXmlContent = _
  "<p:Win32_WMISetting xmlns:p=""http://schemas.microsoft.com/" & _
  "wbem/wsman/1/wmi/root/cimv2/Win32_WMISetting"">" & _
  "<p:LoggingLevel>2</p:LoggingLevel></p:Win32_WMISetting>" 

On Error Resume Next
strReturnedResourceUri = objSession.Put(reourceUri, newXmlContent)
WScript.Echo "Returned resource Uri:" & Chr(10) & _
  strReturnedResourceUri
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
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sesión**](session.md)
</dt> </dl>

 

