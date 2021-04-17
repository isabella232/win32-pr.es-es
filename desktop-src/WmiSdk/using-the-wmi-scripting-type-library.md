---
description: Puede usar la biblioteca de tipos de scripts de WMI para llamar a métodos de API de scripting de WMI desde Microsoft Visual Studio y en archivos WSF de Windows Script Host.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Usar la biblioteca de tipos de scripts WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8ba419d9a9b676d798b97e3b1a57f4e038d97814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706746"
---
# <a name="using-the-wmi-scripting-type-library"></a>Usar la biblioteca de tipos de scripts WMI

Puede usar la biblioteca de tipos de scripts de WMI para llamar a métodos de API de scripting de WMI desde Microsoft Visual Studio y en archivos WSF de Windows Script Host.

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a>Usar la biblioteca de tipos de scripts WMI con Microsoft Visual Studio

> [!Note]  
> Las características de Visual InterDev 6,0 se han integrado en [Microsoft Visual Studio .net](https://msdn.microsoft.com/vstudio/default.aspx).

 

En el procedimiento siguiente se describe cómo habilitar el entorno de desarrollo integrado (IDE) para que tenga en cuenta la biblioteca de tipos WbemScripting.

**Para agregar la biblioteca de tipos de scripts WMI a las referencias del proyecto**

1.  Seleccione **Agregar referencias** en el menú **proyecto** .
2.  En la pestaña COM del cuadro **Agregar referencia** , seleccione biblioteca de scripting de Microsoft WMI v 1.2.
3.  Si no aparece ninguna opción adecuada en la lista de referencias, agréguela mediante **examinar** en el cuadro **referencias** . El botón **examinar** abre un cuadro **Agregar referencia** que le permite buscar la biblioteca de tipos WbemScripting.

    La biblioteca de tipos WbemScripting reside en el archivo Wbemdisp. tlb en el directorio% WINDIR% \\ system32 \\ WBEM.

4.  Seleccione el archivo y haga clic en **Abrir**. La biblioteca Microsoft WMI scripting V 1.2 aparece en la lista de referencias. Asegúrese de activar la casilla situada junto a este elemento en la lista.

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a>Usar la biblioteca de tipos de scripts WMI con Windows Script Host 2,0

Puede incluir la referencia a **WbemScripting. SWbemLocator** en un archivo wsf de Windows Script Host, a diferencia de un script escrito en Visual Basic, Scripting Edition u otros lenguajes de scripting. Esto le permite usar nombres constantes en lugar de valores. Por ejemplo, use **WbemAuthenticationLevelPktPrivacy** en lugar del valor 6 al establecer la autenticación.

Los scripts pueden conectarse con la API de scripting para la biblioteca de tipos WMI mediante los métodos siguientes:

-   Especificar el GUID de WbemScripting en los métodos de VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) y [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).

    Esto alerta a Windows Script Host para conectarse al conjunto de objetos WMI.

    En el siguiente ejemplo de código de VBScript se crea un nuevo objeto [**SWbemDateTime**](swbemdatetime.md) .

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   Usar la [cadena de moniker](constructing-a-moniker-string.md) "winmgmts:" al obtener un objeto nuevo o existente.

    En el siguiente ejemplo de código de VBScript se usa el moniker "winmgmts:" para obtener la instancia del [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) con una propiedad de **identificador** de 0 (cero). **Handle** es la propiedad de clave de esta clase.

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   Hacer referencia a la biblioteca de tipos WMI mediante la <reference> etiqueta del formato de archivo XML de WSH 2,0. Si usa la <reference> etiqueta, la etiqueta debe tener un atributo **UUID** cuyo valor sea el **GUID** de la biblioteca de tipos WMI, o (recomendado) un atributo de objeto cuyo valor es el **ProgID** de cualquiera de los objetos de scripting de WMI que puede crear.

    En el siguiente ejemplo de código de VBScript se usa el PROGID de "WbemScripting". Para ejecutar el script, guarde el texto en un archivo con la extensión. wsf.

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   Usar un **objeto** de <> etiqueta para crear un objeto de scripting de WMI. Puede especificar el atributo **ID** con el valor de un nombre que haga referencia al objeto de scripting de WMI que desea crear, y el atributo **ProgID** igual a PROID del objeto de scripting de WMI.

    El siguiente script de WSH muestra el nombre de host y el número de procesadores en el equipo local. Para ejecutar el script, guarde el texto en un archivo con la extensión. wsf.

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[API de scripting para WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
