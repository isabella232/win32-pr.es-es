---
title: Objeto ResourceLocator (WSManDisp. h)
description: Proporciona la ruta de acceso a un recurso. Puede usar un objeto ResourceLocator en lugar de un URI de recurso en operaciones de objetos de sesión como Session. get, Session. put o Session. Enumerate.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- Objeto ResourceLocator Administración remota de Windows
- Administración remota de Windows de objeto ResourceLocator, descrito
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149992"
---
# <a name="resourcelocator-object"></a>Objeto ResourceLocator

Objeto que proporciona la ruta de acceso a un recurso. Puede usar un objeto **ResourceLocator** en lugar de un [*URI de recurso*](windows-remote-management-glossary.md) en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).

Este objeto le permite:

-   Agregue uno o más [*selectores*](windows-remote-management-glossary.md) que identifiquen una instancia concreta de un recurso. Esto es lo mismo que proporcionar un valor de clave en el URI de recurso para un recurso que utiliza claves. Para obtener más información, vea [**ResourceLocator. AddSelector**](resourcelocator-addselector.md). Puede realizar una operación similar mediante el parámetro de *filtro* en una llamada a [**Session. Enumerate**](session-enumerate.md).
-   Especifique una ruta de acceso de [*fragmento*](windows-remote-management-glossary.md) y un dialecto para obtener solo una propiedad de un recurso. También puede especificar uno o todos los elementos de una propiedad de matriz proporcionando el índice de la matriz. Para obtener más información, vea [**ResourceLocator. FragmentPath**](resourcelocator-fragmentpath.md).
-   Agregue una o varias [*Opciones*](windows-remote-management-glossary.md) que un origen de datos pueda necesitar para procesar una solicitud. Para obtener más información, consulte [**ResourceLocator. AddOption**](resourcelocator-addoption.md).

Para obtener más información, consulte [consultas para instancias específicas de un recurso](querying-for-specific-instances-of-a-resource.md).

## <a name="members"></a>Miembros

El objeto **ResourceLocator** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **ResourceLocator** tiene estos métodos.



| Método                                                   | Descripción                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddOption**](resourcelocator-addoption.md)           | Agrega datos adicionales necesarios para procesar la solicitud.<br/>                                                                   |
| [**AddSelector**](resourcelocator-addselector.md)       | Agrega un [*selector*](windows-remote-management-glossary.md) al objeto **ResourceLocator** .<br/>     |
| [**ClearOptions**](resourcelocator-clearoptions.md)     | Quita todas [*las opciones*](windows-remote-management-glossary.md) del objeto **ResourceLocator** .<br/> |
| [**ClearSelectors**](resourcelocator-clearselectors.md) | Quita todos los selectores de un objeto **ResourceLocator** .<br/>                                                            |



 

### <a name="properties"></a>Propiedades

El objeto **ResourceLocator** tiene estas propiedades.



| Propiedad                                                                          | Tipo de acceso           | Descripción                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FragmentDialect**](resourcelocator-fragmentdialect.md)<br/>             | Lectura/escritura<br/> | Obtiene o establece el dialecto del lenguaje para un [*fragmento*](windows-remote-management-glossary.md)de [*recursos*](windows-remote-management-glossary.md) .<br/> |
| [**FragmentPath**](resourcelocator-fragmentpath.md)<br/>                   | Lectura/escritura<br/> | Obtiene o establece la ruta de acceso de un [*fragmento*](windows-remote-management-glossary.md) de [*recurso*](windows-remote-management-glossary.md) o propiedad.<br/> |
| [**MustUnderstandOptions**](resourcelocator-mustunderstandoptions.md)<br/> | Lectura/escritura<br/> | Obtiene o establece el valor de **MustUnderstandOptions** para el objeto **ResourceLocator** .<br/>                                                                                                         |
| [**ResourceURI**](resourcelocator-resourceuri.md)<br/>                     | Lectura/escritura<br/> | Obtiene o establece el [*URI de recurso*](windows-remote-management-glossary.md) en un objeto **ResourceLocator** .<br/>                                                          |



 

## <a name="remarks"></a>Observaciones

El objeto **ResourceLocator** corresponde a la interfaz **IWSManResourceLocator** .

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se obtienen las propiedades **NumberOfLogicalProcessors** y **NumberOfCores** de una instancia específica del [**\_ procesador Win32**](/windows/desktop/CIMWin32Prov/win32-processor).


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

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
</dt> </dl>

 

