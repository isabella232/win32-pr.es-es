---
title: Enumerar o enumerar todas las instancias de un recurso
description: El método Session. Enumerate es el Administración remota de Windows enfoque para obtener todas las instancias de un recurso especificado.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54587ce97ec6ed5e87af8b0424a6a18d684f7698
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271322"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a>Enumerar o enumerar todas las instancias de un recurso

El método [**Session. Enumerate**](session-enumerate.md) es el administración remota de Windows enfoque para obtener todas las instancias de un recurso especificado.

El método [**Session. Enumerate**](session-enumerate.md) no obtiene una colección en un objeto [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) como una llamada a [**SWbemService.ExecQuery**](/windows/desktop/WmiSdk/swbemservices-execquery) con una [consulta WMI](/windows/desktop/WmiSdk/querying-wmi) como parámetro (por ejemplo, `ExecQuery("SELECT * from Win32_LogicalDisk")` ) o una llamada a un método como [**SWbemObject. instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-). **Session. Enumerate** y los métodos del objeto de [**enumerador**](enumerator.md) son mucho más similares a la operación del objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) de scripting que se usa para leer archivos como una secuencia.

Para leer archivos como una secuencia de texto, debe crear el objeto [TextStream](/previous-versions//312a5kbt(v=vs.85)) scripting y llamar al método [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) para leer cada línea del archivo. De forma similar, puede llamar al método [**Session. Enumerate**](session-enumerate.md) para obtener un objeto de [**enumerador**](enumerator.md) y llamar al método [**enumerador. ReadItem**](enumerator-readitem.md) para obtener el elemento siguiente. Como ocurre cuando se lee desde el archivo de texto, se puede llamar a la propiedad [**enumerador. AtEndOfStream**](enumerator-atendofstream.md) para comprobar si se ha alcanzado el final de los elementos de datos.

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

    

3.  Llame al método [**Session. Enumerate**](session-enumerate.md) . Esta llamada inicia una enumeración. En WinRM, una operación de enumeración no obtiene una colección del mismo modo que lo hace WMI. En su lugar, el método **Session. Enumerate** establece un contexto de enumeración de protocolo WS-Management que se mantiene en el objeto de [**enumerador**](enumerator.md) .

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  Llame al método [**enumerador. ReadItem**](enumerator-readitem.md) para obtener el siguiente elemento de los resultados. En WS-Management protocolo, esto corresponde a la operación de extracción. Use el método [**enumerador. AtEndOfStream**](enumerator-atendofstream.md) como control para saber cuándo detener la lectura.

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

En el siguiente ejemplo de código VBScript se muestra el script completo.


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

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dt>

[Referencia de Administración remota de Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 