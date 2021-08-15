---
title: Objeto Enumerador (WSManDisp.h)
description: Representa un flujo de resultados devueltos por operaciones, como una operación de extracción.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- Objeto enumerador Windows administración remota
- Objeto enumerador Windows administración remota , descrito
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83799c4c67ad0b0f7c1ad89c77c3abab5989f1231508757c47dfe4c1705d7e20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051833"
---
# <a name="enumerator-object"></a>Enumerator (objeto)

Representa un flujo de resultados devueltos por operaciones, como una operación de extracción. Por ejemplo, el [**método Session.Enumerate**](session-enumerate.md) devuelve varios resultados.

## <a name="members"></a>Miembros

El **objeto Enumerator** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Enumerator** tiene estos métodos.



| Método                                  | Descripción                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ReadItem**](enumerator-readitem.md) | Recupera un elemento del recurso y devuelve una representación XML del elemento.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto Enumerador** tiene estas propiedades.



| Propiedad                                                     | Descripción                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AtEndOfStream**](enumerator-atendofstream.md)<br/> | Obtiene un valor booleano que indica si hay más elementos en la colección.<br/> |
| [**Error**](enumerator-error.md)<br/>                 | Obtiene una representación XML de información de error adicional.<br/>                         |



 

## <a name="remarks"></a>Comentarios

Para iniciar una enumeración, use [**Session.Enumerate**](session-enumerate.md). Para realizar una operación [*WS-Enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) que continúa leyendo elementos de la enumeración, use [**Enumerator.ReadItem**](enumerator-readitem.md).

El **objeto Enumerator** corresponde a la [**interfaz IWSManEnumerator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código VBScript se enumeran todos los discos de un equipo remoto especificado por el nombre de dominio completo (servername.domain.com). La subrutina DisplayOutput da formato a la salida de datos de la misma manera que la herramienta WinRM.cmd.


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[WinRM Scripting API](winrm-scripting-api.md)
</dt> <dt>

[Enumerar o enumerar todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Scripting en Windows administración remota](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





