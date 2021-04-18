---
title: Consultar instancias específicas de un recurso
description: La llamada a Session. Enumerate tiene parámetros opcionales que restringen la enumeración a una consulta.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704963"
---
# <a name="querying-for-specific-instances-of-a-resource"></a>Consultar instancias específicas de un recurso

La llamada a [**Session. Enumerate**](session-enumerate.md) tiene parámetros opcionales que restringen la enumeración a una consulta. Dado que la [API de scripting de WinRM](winrm-scripting-api.md) y la API de C++ de [WinRM](winrm-c---api.md) se modelan estrechamente en el protocolo de WS-Management subyacente, los parámetros usan la misma terminología para realizar consultas como el protocolo:*filtrar* y *filtrar el dialecto*.

Puede usar los parámetros Filter y Dialect de [**Session. Enumerate**](session-enumerate.md) o puede construir y proporcionar un objeto [**ResourceLocator**](resourcelocator.md) y el método [**AddSelector**](resourcelocator-addselector.md) , pero no puede hacer ambas cosas.

Este procedimiento ejecuta una consulta para los adaptadores de red que tienen TCP/IP enlazado y habilitado. La consulta solicita todas las instancias de [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) que tienen la propiedad **IpEnabled** establecida en **true**. A excepción de la adición del *filtro* y del *dialecto*, la consulta se trata como una enumeración simple.

En este ejemplo, el nombre de recurso para la constante de recurso se representa con un asterisco " \* " porque el nombre de clase, [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), ya se menciona en la cadena *strFilter* .

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

    

3.  Construya la cadena de filtro. Administración remota de Windows admite [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) como dialecto de filtro.

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  Establezca las [**constantes de enumeración**](enumeration-constants.md) necesarias en el parámetro *Flags* .

    Tenga en cuenta que si las marcas incluyen las [**constantes de enumeración**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow** , el servicio WinRM devuelve el error del código de error del **modo de \_ \_ polimorfismo WSMAN \_ \_ no compatible**.

5.  Llame al método [**Session. Enumerate**](session-enumerate.md) . Esta llamada inicia una enumeración. El método **Session. Enumerate** establece un contexto de enumeración de protocolo WS-Management, mantenido en el objeto de [**enumerador**](enumerator.md) .

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  Llame al método [**enumerador. ReadItem**](enumerator-readitem.md) para obtener el siguiente elemento de los resultados. En WS-Management protocolo, esto corresponde a la operación de extracción. Use el método [**enumerador. AtEndOfStream**](enumerator-atendofstream.md) como control para saber cuándo detener la lectura.

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

En el siguiente ejemplo de código VBScript se muestra el script completo.


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

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dt>

[Enumerar o enumerar todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 