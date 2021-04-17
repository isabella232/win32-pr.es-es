---
description: Cualquier lenguaje de scripting, como VBScript, que funcione con objetos ActiveX podrá tener acceso a los datos de WMI. Las aplicaciones pueden tener acceso a WMI en C++, mediante la API COM para WMI o en Visual Basic, mediante la biblioteca de tipos Wbemdisp. tlb y la API de scripting para WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Crear una aplicación o un script WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707097"
---
# <a name="creating-a-wmi-application-or-script"></a><span data-ttu-id="ec305-105">Crear una aplicación o un script WMI</span><span class="sxs-lookup"><span data-stu-id="ec305-105">Creating a WMI Application or Script</span></span>

<span data-ttu-id="ec305-106">Cualquier lenguaje de scripting, como VBScript, que funcione con objetos ActiveX podrá tener acceso a los datos de WMI.</span><span class="sxs-lookup"><span data-stu-id="ec305-106">Any scripting language, such as VBScript, that works with ActiveX objects can access WMI data.</span></span> <span data-ttu-id="ec305-107">Las aplicaciones pueden tener acceso a WMI en C++, mediante la [API com para WMI](com-api-for-wmi.md) o en Visual Basic, mediante la [biblioteca de tipos](using-the-wmi-scripting-type-library.md) Wbemdisp. tlb y la [API de scripting para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ec305-107">Applications can access WMI in C++, using the [COM API for WMI](com-api-for-wmi.md) or in Visual Basic, using the Wbemdisp.tlb [type library](using-the-wmi-scripting-type-library.md) and the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="ec305-108">.</span><span class="sxs-lookup"><span data-stu-id="ec305-108">.</span></span> <span data-ttu-id="ec305-109">Puede obtener datos a través de WMI escribiendo un script, una Active Server página (ASP) o una aplicación HTML (HTA).</span><span class="sxs-lookup"><span data-stu-id="ec305-109">You can obtain data through WMI by writing a script, an Active Server Page (ASP), or an HTML application (HTA).</span></span> <span data-ttu-id="ec305-110">También puede usar Windows PowerShell para obtener datos o escribir scripts.</span><span class="sxs-lookup"><span data-stu-id="ec305-110">You can also use Windows PowerShell to obtain data or write scripts.</span></span> <span data-ttu-id="ec305-111">Para obtener más información, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) y [Introducción con Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="ec305-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) and [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span> <span data-ttu-id="ec305-112">TechNet ScriptCenter en [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contiene cientos de ejemplos de scripting.</span><span class="sxs-lookup"><span data-stu-id="ec305-112">The TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contains hundreds of scripting examples.</span></span> <span data-ttu-id="ec305-113">Para obtener más información sobre los recursos de impresión y en línea, vea [más información](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="ec305-113">For more information about print and online resources, see [Further Information](further-information.md).</span></span>

<span data-ttu-id="ec305-114">En el procedimiento siguiente se describe cómo conectarse al servicio WMI y al almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="ec305-114">The following procedure describes how to connect to the WMI service and data store.</span></span>

<span data-ttu-id="ec305-115">**Para conectarse al servicio WMI y al almacén de datos**</span><span class="sxs-lookup"><span data-stu-id="ec305-115">**To connect to the WMI service and data store**</span></span>

1.  <span data-ttu-id="ec305-116">Busque el servicio WMI en un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="ec305-116">Locate the WMI service on a specific machine.</span></span>
2.  <span data-ttu-id="ec305-117">Conéctese a uno o varios espacios de nombres de WMI.</span><span class="sxs-lookup"><span data-stu-id="ec305-117">Connect to one or more WMI namespaces.</span></span>

<span data-ttu-id="ec305-118">Estas operaciones son diferentes en C++, Visual Basic, .NET Framework lenguajes o cuando se usa un script.</span><span class="sxs-lookup"><span data-stu-id="ec305-118">These operations are different in C++, Visual Basic, .NET Framework languages, or when using a script.</span></span> <span data-ttu-id="ec305-119">Los scripts y las aplicaciones Visual Basic deben tener acceso a las clases cuyas instancias se proporcionan con los datos de los proveedores existentes.</span><span class="sxs-lookup"><span data-stu-id="ec305-119">Scripts and Visual Basic applications must access classes whose instances are supplied with data by existing providers.</span></span> <span data-ttu-id="ec305-120">Sin embargo, las aplicaciones escritas en C++ pueden hacer más.</span><span class="sxs-lookup"><span data-stu-id="ec305-120">But applications written in C++ can do more.</span></span> <span data-ttu-id="ec305-121">Por ejemplo, una aplicación escrita en C++ puede enviar eventos, pero un script de WMI solo puede suscribirse para recibir eventos.</span><span class="sxs-lookup"><span data-stu-id="ec305-121">For example, an application written in C++ can send events, but a WMI script can only subscribe to receive events.</span></span>

<span data-ttu-id="ec305-122">Un proveedor WMI solo se puede escribir en C++ o mediante el .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ec305-122">A WMI provider can be written only in C++ or using the .NET Framework.</span></span> <span data-ttu-id="ec305-123">Para obtener más información sobre cómo escribir aplicaciones en C# o Visual Basic .NET, consulte [información general sobre WMI .net](/previous-versions/bb404655(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="ec305-123">For more information about writing applications in C# or Visual Basic .NET, see [WMI .NET Overview](/previous-versions/bb404655(v=vs.90)).</span></span>

<span data-ttu-id="ec305-124">Para obtener más información acerca de la creación de aplicaciones y scripts para WMI, vea:</span><span class="sxs-lookup"><span data-stu-id="ec305-124">For more information about creating applications and scripts for WMI, see:</span></span>

-   [<span data-ttu-id="ec305-125">Crear una aplicación WMI con C++</span><span class="sxs-lookup"><span data-stu-id="ec305-125">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
-   [<span data-ttu-id="ec305-126">Creación de un script de WMI</span><span class="sxs-lookup"><span data-stu-id="ec305-126">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
-   [<span data-ttu-id="ec305-127">Crear un cliente WMI administrado</span><span class="sxs-lookup"><span data-stu-id="ec305-127">Creating a Managed WMI Client</span></span>](creating-a-managed-wmi-client.md)

<span data-ttu-id="ec305-128">Para realizar la mayoría de las tareas, utilice las [clases WMI](wmi-classes.md)preinstaladas.</span><span class="sxs-lookup"><span data-stu-id="ec305-128">To perform most tasks, use the preinstalled [WMI classes](wmi-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec305-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec305-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec305-130">Usar WMI</span><span class="sxs-lookup"><span data-stu-id="ec305-130">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
