---
title: Mostrar la salida XML de scripts winRM
description: Windows Los scripts de administración remota devuelven XML en lugar de objetos . El XML no está en un formato legible para el ser humano. Puede usar los métodos de la API MSXML API y el archivo XSL preinstalado para transformar los datos en formato legible para el usuario.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df5c27c1fe22ae87395357aeefe681af7c041420d32b7bccbf595fab38bb060b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680025"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>Mostrar la salida XML de scripts winRM

Windows Los scripts de administración remota devuelven XML en lugar de objetos . El XML no está en un formato legible para el ser humano. Puede usar los métodos de la API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) API y el archivo XSL preinstalado para transformar los datos en un formato legible para el usuario.

Para obtener más información sobre la salida XML de WinRM y ejemplos de XML sin formato y con formato, vea [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).

La herramienta de línea de comandos **Winrm** incluye un archivo de transformación denominado WsmTxt.xsl que muestra la salida en un formato tabular. Si el script proporciona este archivo a los métodos MSXML que realizan tranformes, la salida aparece igual que la salida de la **herramienta Winrm.**

**Para dar formato a la salida XML sin formato**

1.  Cree el [**objeto WSMan**](wsman.md) y cree una sesión.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  Cree MSXML objetos que representen la salida de respuesta XML y la transformación XSL.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Obtener datos a través [**de métodos de**](session.md) objeto Session.

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  Proporcione la respuesta al método MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) y al método [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) para almacenar el archivo de transformación.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  Use el MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) y muestre o guarde la salida.

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

En el siguiente ejemplo de código de VBScript se muestra el script completo.


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



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a>Agregar una subrutina portable para transformar XML a los scripts

Puede agregar una subrutina a los scripts que usan el archivo XSL preinstalado para convertir la salida XML sin formato de un script WinRM en un formulario tabular.

La siguiente subrutina usa llamadas a MSXML métodos de scripting para proporcionar la salida a WsmTxt.xsl.


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



La siguiente subrutina transforma cada línea de los datos como se muestra en el ejemplo siguiente.


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

[Acerca Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> <dt>

[Windows Referencia de administración remota](windows-remote-management-reference.md)
</dt> </dl>

 

 