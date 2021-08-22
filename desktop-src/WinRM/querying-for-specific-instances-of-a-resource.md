---
title: Consulta de instancias específicas de un recurso
description: La llamada a Session.Enumerate tiene parámetros opcionales que reducen la enumeración en una consulta.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f757b6392ec26f809004d599f6c5603629d23e8eb7a7f4b08a4f3a4ef18791a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642855"
---
# <a name="querying-for-specific-instances-of-a-resource"></a>Consulta de instancias específicas de un recurso

La llamada a [**Session.Enumerate tiene**](session-enumerate.md) parámetros opcionales que reducen la enumeración en una consulta. Dado que la API de scripting de [WinRM](winrm-scripting-api.md) y la API de C++ de [WinRM](winrm-c---api.md) están estrechamente modeladas en el protocolo WS-Management subyacente, los parámetros usan la misma terminología para realizar consultas como el protocolo: filtrar y filtrar *dialecto*.

Puede usar los parámetros de filtro y dialecto [**de Session.Enumerate**](session-enumerate.md) o puede construir y proporcionar un objeto [**ResourceLocator**](resourcelocator.md) y el [**método AddSelector,**](resourcelocator-addselector.md) pero no puede hacer ambos.

Este procedimiento ejecuta una consulta para los adaptadores de red que tienen TCP/IP enlazado y habilitado. La consulta solicita todas las instancias de [**\_ NetworkAdapterConfiguration de Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) que tienen la **propiedad IpEnabled** establecida en **True.** A excepción de la adición del *filtro y* *el dialecto*, la consulta se controla como una enumeración simple.

En este ejemplo, el nombre del recurso de la constante Resource se representa mediante un asterisco " " porque el nombre de \* clase, [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), ya se menciona en la *cadena strFilter.*

**Para consultar instancias específicas de un recurso**

1.  Para facilitar la lectura, defina los URI como constantes.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  Crear una sesión.

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  Construya la cadena de filtro. Windows Administración remota admite [WQL como](/windows/desktop/WmiSdk/wql-sql-for-wmi) dialecto de filtro.

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  Establezca las constantes [**de enumeración necesarias en**](enumeration-constants.md) el parámetro *flags.*

    Tenga en cuenta que si [](enumeration-constants.md) las marcas incluyen las constantes de enumeración **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow,** el servicio WinRM devuelve el código de **error ERROR \_ WSMAN \_ POLYMORPHISM \_ MODE \_ UNSUPPORTED**.

5.  Llame al [**método Session.Enumerate.**](session-enumerate.md) Esta llamada inicia una enumeración. El **método Session.Enumerate** establece un WS-Management de enumeración de protocolos, que se mantiene en el [**objeto Enumerador.**](enumerator.md)

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  Llame al [**método Enumerator.ReadItem**](enumerator-readitem.md) para obtener el siguiente elemento de los resultados. En WS-Management protocolo, corresponde a la operación de extracción. Use el [**método Enumerator.AtEndOfStream**](enumerator-atendofstream.md) como control para saber cuándo se debe detener la lectura.

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

En el siguiente ejemplo de código de VBScript se muestra el script completo.


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> <dt>

[Enumerar o enumerar todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 