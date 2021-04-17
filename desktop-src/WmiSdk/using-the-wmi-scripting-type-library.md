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
# <a name="using-the-wmi-scripting-type-library"></a><span data-ttu-id="e9a4f-103">Usar la biblioteca de tipos de scripts WMI</span><span class="sxs-lookup"><span data-stu-id="e9a4f-103">Using the WMI Scripting Type Library</span></span>

<span data-ttu-id="e9a4f-104">Puede usar la biblioteca de tipos de scripts de WMI para llamar a métodos de API de scripting de WMI desde Microsoft Visual Studio y en archivos WSF de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-104">You can use the WMI scripting type library to call WMI Scripting API methods from Microsoft Visual Studio and in Windows Script Host WSF files.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a><span data-ttu-id="e9a4f-105">Usar la biblioteca de tipos de scripts WMI con Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e9a4f-105">Using the WMI Scripting Type Library with Microsoft Visual Studio</span></span>

> [!Note]  
> <span data-ttu-id="e9a4f-106">Las características de Visual InterDev 6,0 se han integrado en [Microsoft Visual Studio .net](https://msdn.microsoft.com/vstudio/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="e9a4f-106">Visual InterDev 6.0 features have been integrated into [Microsoft Visual Studio .NET](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

 

<span data-ttu-id="e9a4f-107">En el procedimiento siguiente se describe cómo habilitar el entorno de desarrollo integrado (IDE) para que tenga en cuenta la biblioteca de tipos WbemScripting.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-107">The following procedure describes how to enable the integrated development environment (IDE) to be aware of the WbemScripting type library.</span></span>

<span data-ttu-id="e9a4f-108">**Para agregar la biblioteca de tipos de scripts WMI a las referencias del proyecto**</span><span class="sxs-lookup"><span data-stu-id="e9a4f-108">**To add the WMI Scripting type library to the project references**</span></span>

1.  <span data-ttu-id="e9a4f-109">Seleccione **Agregar referencias** en el menú **proyecto** .</span><span class="sxs-lookup"><span data-stu-id="e9a4f-109">Select **Add References** from the **Project** menu.</span></span>
2.  <span data-ttu-id="e9a4f-110">En la pestaña COM del cuadro **Agregar referencia** , seleccione biblioteca de scripting de Microsoft WMI v 1.2.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-110">In the COM tab of the **Add Reference** box, select Microsoft WMI Scripting V1.2 Library.</span></span>
3.  <span data-ttu-id="e9a4f-111">Si no aparece ninguna opción adecuada en la lista de referencias, agréguela mediante **examinar** en el cuadro **referencias** .</span><span class="sxs-lookup"><span data-stu-id="e9a4f-111">If no suitable option appears in the References list, add it by using **Browse** in the **References** box.</span></span> <span data-ttu-id="e9a4f-112">El botón **examinar** abre un cuadro **Agregar referencia** que le permite buscar la biblioteca de tipos WbemScripting.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-112">The **Browse** opens an **Add Reference** box that enables you to locate the WbemScripting type library.</span></span>

    <span data-ttu-id="e9a4f-113">La biblioteca de tipos WbemScripting reside en el archivo Wbemdisp. tlb en el directorio% WINDIR% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-113">The WbemScripting type library resides in the file Wbemdisp.tlb in the %windir%\\System32\\Wbem directory.</span></span>

4.  <span data-ttu-id="e9a4f-114">Seleccione el archivo y haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-114">Select the file and click **Open**.</span></span> <span data-ttu-id="e9a4f-115">La biblioteca Microsoft WMI scripting V 1.2 aparece en la lista de referencias.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-115">Microsoft WMI Scripting V1.2 Library appears on the references list.</span></span> <span data-ttu-id="e9a4f-116">Asegúrese de activar la casilla situada junto a este elemento en la lista.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-116">Ensure that you select the box next to this item in the list.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a><span data-ttu-id="e9a4f-117">Usar la biblioteca de tipos de scripts WMI con Windows Script Host 2,0</span><span class="sxs-lookup"><span data-stu-id="e9a4f-117">Using the WMI Scripting Type Library with Windows Script Host 2.0</span></span>

<span data-ttu-id="e9a4f-118">Puede incluir la referencia a **WbemScripting. SWbemLocator** en un archivo wsf de Windows Script Host, a diferencia de un script escrito en Visual Basic, Scripting Edition u otros lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-118">You can include the reference to the **WbemScripting.SWbemLocator** in a Windows Script Host WSF file, unlike a script written in Visual Basic, Scripting Edition or other scripting languages.</span></span> <span data-ttu-id="e9a4f-119">Esto le permite usar nombres constantes en lugar de valores.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-119">This enables you to use constant names instead of values.</span></span> <span data-ttu-id="e9a4f-120">Por ejemplo, use **WbemAuthenticationLevelPktPrivacy** en lugar del valor 6 al establecer la autenticación.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-120">For example, use **WbemAuthenticationLevelPktPrivacy** rather than the value 6 when setting authentication.</span></span>

<span data-ttu-id="e9a4f-121">Los scripts pueden conectarse con la API de scripting para la biblioteca de tipos WMI mediante los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e9a4f-121">Scripts can connect with the Scripting API for WMI type library using the following methods:</span></span>

-   <span data-ttu-id="e9a4f-122">Especificar el GUID de WbemScripting en los métodos de VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) y [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="e9a4f-122">Specifying the WbemScripting GUID in the VBScript methods [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span></span>

    <span data-ttu-id="e9a4f-123">Esto alerta a Windows Script Host para conectarse al conjunto de objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-123">This alerts Windows Script Host to connect to the WMI object set.</span></span>

    <span data-ttu-id="e9a4f-124">En el siguiente ejemplo de código de VBScript se crea un nuevo objeto [**SWbemDateTime**](swbemdatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="e9a4f-124">The following VBScript code example creates a new [**SWbemDateTime**](swbemdatetime.md) object.</span></span>

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   <span data-ttu-id="e9a4f-125">Usar la [cadena de moniker](constructing-a-moniker-string.md) "winmgmts:" al obtener un objeto nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-125">Using the [Moniker string](constructing-a-moniker-string.md) "winmgmts:" when obtaining a new or existing object.</span></span>

    <span data-ttu-id="e9a4f-126">En el siguiente ejemplo de código de VBScript se usa el moniker "winmgmts:" para obtener la instancia del [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) con una propiedad de **identificador** de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="e9a4f-126">The following VBScript code example uses the "winmgmts:" moniker to get the instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) with a **Handle** property of 0 (zero).</span></span> <span data-ttu-id="e9a4f-127">**Handle** es la propiedad de clave de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-127">**Handle** is the key property for this class.</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   <span data-ttu-id="e9a4f-128">Hacer referencia a la biblioteca de tipos WMI mediante la <reference> etiqueta del formato de archivo XML de WSH 2,0.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-128">Referencing the WMI type library using the <reference> tag of the WSH 2.0 XML file format.</span></span> <span data-ttu-id="e9a4f-129">Si usa la <reference> etiqueta, la etiqueta debe tener un atributo **UUID** cuyo valor sea el **GUID** de la biblioteca de tipos WMI, o (recomendado) un atributo de objeto cuyo valor es el **ProgID** de cualquiera de los objetos de scripting de WMI que puede crear.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-129">If you use the <reference> tag, the tag must have either a **uuid** attribute whose value is the **GUID** of the WMI type library, or (recommended) an object attribute whose value is the **PROGID** of any of the WMI scripting objects you can create.</span></span>

    <span data-ttu-id="e9a4f-130">En el siguiente ejemplo de código de VBScript se usa el PROGID de "WbemScripting".</span><span class="sxs-lookup"><span data-stu-id="e9a4f-130">The following VBScript code example uses the PROGID of "WbemScripting" .</span></span> <span data-ttu-id="e9a4f-131">Para ejecutar el script, guarde el texto en un archivo con la extensión. wsf.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-131">To run the script, save the text in a file with a .wsf extension.</span></span>

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

    

-   <span data-ttu-id="e9a4f-132">Usar un **objeto** de <> etiqueta para crear un objeto de scripting de WMI.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-132">Using an <**object**> tag to create a WMI scripting object.</span></span> <span data-ttu-id="e9a4f-133">Puede especificar el atributo **ID** con el valor de un nombre que haga referencia al objeto de scripting de WMI que desea crear, y el atributo **ProgID** igual a PROID del objeto de scripting de WMI.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-133">You can specify the **id** attribute with the value of a name that references the WMI scripting object you want to create, and the **progid** attribute equal to the PROID of the WMI scripting object.</span></span>

    <span data-ttu-id="e9a4f-134">El siguiente script de WSH muestra el nombre de host y el número de procesadores en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-134">The following WSH script displays the hostname and the number of processors on the local computer.</span></span> <span data-ttu-id="e9a4f-135">Para ejecutar el script, guarde el texto en un archivo con la extensión. wsf.</span><span class="sxs-lookup"><span data-stu-id="e9a4f-135">To run the script, save the text in a file with a .wsf extension.</span></span>

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

    

## <a name="related-topics"></a><span data-ttu-id="e9a4f-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9a4f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9a4f-137">Scripting en WMI</span><span class="sxs-lookup"><span data-stu-id="e9a4f-137">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[<span data-ttu-id="e9a4f-138">API de scripting para WMI</span><span class="sxs-lookup"><span data-stu-id="e9a4f-138">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
