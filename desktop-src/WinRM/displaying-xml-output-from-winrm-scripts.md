---
title: Mostrar la salida XML de los scripts de WinRM
description: Administración remota de Windows scripts devuelven XML en lugar de objetos. El XML no tiene un formato legible. Puede usar los métodos de la API de MSXML y el archivo XSL preinstalado para transformar los datos en un formato legible.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c70dd0a61181f6fc61e685641ff0ed5e3d43ffe8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078145"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>Mostrar la salida XML de los scripts de WinRM

Administración remota de Windows scripts devuelven XML en lugar de objetos. El XML no tiene un formato legible. Puede usar los métodos de la API de [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) y el archivo XSL preinstalado para transformar los datos en un formato legible.

Para obtener más información acerca de la salida XML de WinRM y ejemplos de XML y sin formato, vea [Scripting in administración remota de Windows](scripting-in-windows-remote-management.md).

La herramienta de línea de comandos de **WinRM** incluye un archivo de transformación denominado WsmTxt. XSL que muestra la salida en un formato tabular. Si el script suministra este archivo a los métodos MSXML que realizan transforma, la salida aparece igual que la salida de la herramienta **WinRM** .

**Para dar formato a la salida XML sin formato**

1.  Cree el objeto [**WSMan**](wsman.md) y cree una sesión.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  Cree objetos MSXML que representen la salida de respuesta XML y la transformación XSL.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Obtener datos a través de métodos de objeto de [**sesión**](session.md) .

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  Proporcione la respuesta al método [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) de MSXML y el método [Load](/previous-versions/windows/desktop/ms762722(v=vs.85)) para almacenar el archivo de transformación.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  Usar el método [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) de MSXML y mostrar o guardar la salida.

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

En el siguiente ejemplo de código VBScript se muestra el script completo.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set Session = Wsman.CreateSession
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(xmlResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)
```



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a>Agregar una subrutina portable para transformar XML en los scripts

Puede Agregar una subrutina a los scripts que utiliza el archivo XSL preinstalado para convertir la salida XML sin formato de un script WinRM a un formato tabular.

La subrutina siguiente usa llamadas a los métodos de scripting de MSXML para proporcionar la salida a WsmTxt. Xsl.


```VB
'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile)
End Sub
```



La subrutina siguiente transforma cada línea de los datos tal y como se muestra en el ejemplo siguiente.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_LogicalDisk"
Set objResultSet = objSession.Enumerate(strResource)
While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dt>

[Referencia de Administración remota de Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 