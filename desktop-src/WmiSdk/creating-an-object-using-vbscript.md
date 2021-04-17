---
description: Puede crear un objeto para WMI en Visual Basic Scripting Edition (VBScript) si se conecta a WMI y, a continuación, llama a CreateObject. En la tabla siguiente se enumeran los métodos de la API de scripting para WMI que admiten la creación de objetos.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Crear un objeto mediante VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497770"
---
# <a name="creating-an-object-using-vbscript"></a><span data-ttu-id="ae27e-104">Crear un objeto mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="ae27e-104">Creating an Object Using VBScript</span></span>

<span data-ttu-id="ae27e-105">Puede crear un objeto para WMI en Visual Basic Scripting Edition (VBScript) si se conecta a WMI y, a continuación, llama a [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae27e-105">You can create an object for WMI in Visual Basic Scripting Edition (VBScript) by connecting to WMI and then calling [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span> <span data-ttu-id="ae27e-106">En la tabla siguiente se enumeran los métodos de la API de scripting para WMI que admiten la creación de objetos.</span><span class="sxs-lookup"><span data-stu-id="ae27e-106">The following table lists the methods in the Scripting API for WMI that support object creation.</span></span>



| <span data-ttu-id="ae27e-107">Interfaz</span><span class="sxs-lookup"><span data-stu-id="ae27e-107">Interface</span></span>                                        | <span data-ttu-id="ae27e-108">ProgID</span><span class="sxs-lookup"><span data-stu-id="ae27e-108">ProgID</span></span>                             |
|--------------------------------------------------|------------------------------------|
| [<span data-ttu-id="ae27e-109">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="ae27e-109">**SWbemDateTime**</span></span>](swbemdatetime.md)           | <span data-ttu-id="ae27e-110">"WbemScripting.SwbemDateTime"</span><span class="sxs-lookup"><span data-stu-id="ae27e-110">"WbemScripting.SwbemDateTime"</span></span>      |
| [<span data-ttu-id="ae27e-111">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="ae27e-111">**SWbemLocator**</span></span>](swbemlocator.md)             | <span data-ttu-id="ae27e-112">"WbemScripting.SWbemLocator"</span><span class="sxs-lookup"><span data-stu-id="ae27e-112">"WbemScripting.SWbemLocator"</span></span>       |
| [<span data-ttu-id="ae27e-113">**SWbemLastError**</span><span class="sxs-lookup"><span data-stu-id="ae27e-113">**SWbemLastError**</span></span>](swbemlasterror.md)         | <span data-ttu-id="ae27e-114">"WbemScripting. SWbem. LastError"</span><span class="sxs-lookup"><span data-stu-id="ae27e-114">"WbemScripting.SWbem.LastError"</span></span>    |
| [<span data-ttu-id="ae27e-115">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="ae27e-115">**SWbemObjectPath**</span></span>](swbemobjectpath.md)       | <span data-ttu-id="ae27e-116">"WbemScripting.SWbemObjectPath"</span><span class="sxs-lookup"><span data-stu-id="ae27e-116">"WbemScripting.SWbemObjectPath"</span></span>    |
| [<span data-ttu-id="ae27e-117">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="ae27e-117">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md) | <span data-ttu-id="ae27e-118">"WbemScripting.SWbemNamedValueSet"</span><span class="sxs-lookup"><span data-stu-id="ae27e-118">"WbemScripting.SWbemNamedValueSet"</span></span> |
| [<span data-ttu-id="ae27e-119">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="ae27e-119">**SWbemRefresher**</span></span>](swbemrefresher.md)         | <span data-ttu-id="ae27e-120">"WbemScripting.SWbemRefresher"</span><span class="sxs-lookup"><span data-stu-id="ae27e-120">"WbemScripting.SWbemRefresher"</span></span>     |
| [<span data-ttu-id="ae27e-121">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="ae27e-121">**SWbemSink**</span></span>](swbemsink.md)                   | <span data-ttu-id="ae27e-122">"WbemScripting.SWbemSink"</span><span class="sxs-lookup"><span data-stu-id="ae27e-122">"WbemScripting.SWbemSink"</span></span>          |



 

<span data-ttu-id="ae27e-123">En el procedimiento siguiente se describe cómo crear un objeto WMI con VBScript.</span><span class="sxs-lookup"><span data-stu-id="ae27e-123">The following procedure describes how to create a WMI object using VBScript.</span></span>

<span data-ttu-id="ae27e-124">**Para crear un objeto WMI mediante VBScript**</span><span class="sxs-lookup"><span data-stu-id="ae27e-124">**To create a WMI object using VBScript**</span></span>

1.  <span data-ttu-id="ae27e-125">Conéctese a WMI con un moniker o un objeto [**SWbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="ae27e-125">Connect to WMI using either a moniker or an [**SWbemLocator**](swbemlocator.md) object.</span></span>

    <span data-ttu-id="ae27e-126">Para obtener más información, vea [crear un script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ae27e-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

2.  <span data-ttu-id="ae27e-127">Realice una llamada al método [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="ae27e-127">Make a call to the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method.</span></span>

    <span data-ttu-id="ae27e-128">En el ejemplo de código siguiente se muestra cómo crear un objeto.</span><span class="sxs-lookup"><span data-stu-id="ae27e-128">The following code example shows how to create an object.</span></span>

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    <span data-ttu-id="ae27e-129">Si utiliza un moniker en el paso 1, no es necesario volver a llamar a [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ae27e-129">If you use a moniker in Step 1, you do not need to call [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) again.</span></span>

 

 
