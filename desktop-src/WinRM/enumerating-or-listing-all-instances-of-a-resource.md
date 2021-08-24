---
title: Enumerar o enumerar todas las instancias de un recurso
description: El método Session.Enumerate es el Windows de administración remota para obtener todas las instancias de un recurso especificado.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f510d0e0cc8115ca4dca7c7e46dd5e987ef0dd15dd4fa7d92e47d737e467d8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679995"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a>Enumerar o enumerar todas las instancias de un recurso

El [**método Session.Enumerate**](session-enumerate.md) es el Windows de administración remota para obtener todas las instancias de un recurso especificado.

El [**método Session.Enumerate**](session-enumerate.md) no obtiene una colección en un objeto [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) como una llamada [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) con una consulta [WMI](/windows/desktop/WmiSdk/querying-wmi) como parámetro (por ejemplo, ) ni una llamada a un método como `ExecQuery("SELECT * from Win32_LogicalDisk")` [**SWbemObject.Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-). **Los métodos de objeto Session.Enumerate** y [**Enumerator**](enumerator.md) son mucho más similares al funcionamiento del objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de scripting que se usa para leer archivos como una secuencia.

Para leer archivos como una secuencia de texto, debe crear el objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de scripting y llamar al [método TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) para leer cada línea del archivo. De forma similar, puede llamar al método [**Session.Enumerate**](session-enumerate.md) para obtener un objeto [**Enumerator**](enumerator.md) y llamar al método [**Enumerator.ReadItem**](enumerator-readitem.md) para obtener el siguiente elemento. Como ocurre al leer desde el archivo de texto, puede llamar a la propiedad [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) para comprobar si ha llegado al final de los elementos de datos.

**Para enumerar un recurso**

1.  Crear una sesión.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  Construya el URI para identificar el recurso.

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  Llame al [**método Session.Enumerate.**](session-enumerate.md) Esta llamada inicia una enumeración . En WinRM, una operación de enumeración no obtiene una colección de la misma manera que WMI. En su lugar, **el método Session.Enumerate** establece un WS-Management de enumeración de protocolo que se mantiene en el [**objeto Enumerator.**](enumerator.md)

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  Llame al [**método Enumerator.ReadItem**](enumerator-readitem.md) para obtener el siguiente elemento de los resultados. En WS-Management protocolo, corresponde a la operación de extracción. Use el [**método Enumerator.AtEndOfStream**](enumerator-atendofstream.md) como control para saber cuándo se debe detener la lectura.

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

En el siguiente ejemplo de código de VBScript se muestra el script completo.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set EnumJobs = objSession.Enumerate( strResource )
NumOfJobs = 0
While Not EnumJobs.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( EnumJobs.ReadItem ) 
Wend
Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> <dt>

[Windows Referencia de administración remota](windows-remote-management-reference.md)
</dt> </dl>

 

 