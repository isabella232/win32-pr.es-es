---
title: Objeto Enumerator (WSManDisp. h)
description: Representa una secuencia de resultados devuelta de operaciones, como una operación de extracción.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- Objeto enumerador Administración remota de Windows
- Objeto de enumerador Administración remota de Windows, descrito
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
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079690"
---
# <a name="enumerator-object"></a>Enumerator (objeto)

Representa una secuencia de resultados devuelta de operaciones, como una operación de extracción. Por ejemplo, el método [**Session. Enumerate**](session-enumerate.md) devuelve varios resultados.

## <a name="members"></a>Miembros

El objeto de **enumerador** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **enumerador** tiene estos métodos.



| Método                                  | Descripción                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ReadItem**](enumerator-readitem.md) | Recupera un elemento del recurso y devuelve una representación XML del elemento.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto de **enumerador** tiene estas propiedades.



| Propiedad                                                     | Descripción                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AtEndOfStream**](enumerator-atendofstream.md)<br/> | Obtiene un valor booleano que indica si hay más elementos en la colección.<br/> |
| [**Error**](enumerator-error.md)<br/>                 | Obtiene una representación XML de información de error adicional.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Para iniciar una enumeración, use [**Session. Enumerate**](session-enumerate.md). Para realizar una operación [*WS-Enumeration:*](windows-remote-management-glossary.md)[*pull*](windows-remote-management-glossary.md) que continúe leyendo los elementos de la enumeración, use [**Enumerator. ReadItem**](enumerator-readitem.md).

El objeto de **enumerador** corresponde a la interfaz [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) .

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se enumeran todos los discos de un equipo remoto especificado por el nombre de dominio completo (servername.domain.com). La subrutina DisplayOutput da formato a la salida de datos de la misma manera que la herramienta WinRM. cmd.


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

[API de scripting de WinRM](winrm-scripting-api.md)
</dt> <dt>

[Enumerar o enumerar todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Scripting en Administración remota de Windows](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





