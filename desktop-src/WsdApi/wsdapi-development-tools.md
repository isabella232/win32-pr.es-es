---
description: Las herramientas de desarrollo de WSDAPI incluidas en el Windows SDK (la CodeGen de WSD, el host de depuración WSD y el cliente de depuración WSD) permiten a los desarrolladores crear y depurar clientes y dispositivos basados en WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Herramientas de desarrollo de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706025"
---
# <a name="wsdapi-development-tools"></a><span data-ttu-id="8a725-103">Herramientas de desarrollo de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="8a725-103">WSDAPI Development Tools</span></span>

<span data-ttu-id="8a725-104">Las herramientas de desarrollo de WSDAPI incluidas en el Windows SDK (la CodeGen de WSD, el host de depuración WSD y el cliente de depuración WSD) permiten a los desarrolladores crear y depurar clientes y dispositivos basados en WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="8a725-104">The WSDAPI development tools included in the Windows SDK (WSD CodeGen, WSD Debug Host, and WSD Debug Client) enable developers to create and debug WSDAPI-based clients and devices.</span></span> <span data-ttu-id="8a725-105">El código fuente de estas herramientas no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8a725-105">The source code for these tools is not available.</span></span> <span data-ttu-id="8a725-106">Las herramientas del SDK se encuentran en el siguiente directorio: <Windows SDK Install Folder> \\ bin.</span><span class="sxs-lookup"><span data-stu-id="8a725-106">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="8a725-107">WSD CodeGen (wsdcodegen.exe) convierte un contrato WSDL en código C++ generado, al que los desarrolladores pueden llamar directamente.</span><span class="sxs-lookup"><span data-stu-id="8a725-107">WSD CodeGen (wsdcodegen.exe) converts a WSDL contract into generated C++ code, which developers can call directly into.</span></span> <span data-ttu-id="8a725-108">Controla la serialización de datos y la representación de conexión para que los desarrolladores puedan centrarse en el diseño de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8a725-108">It handles the data serialization and wire representation so developers can focus on designing applications.</span></span> <span data-ttu-id="8a725-109">Para obtener más información sobre WSD CodeGen, consulte [servicios web en el generador de código de dispositivos](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="8a725-109">For more information about WSD CodeGen, see [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="8a725-110">Esta herramienta está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows y en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="8a725-110">This tool is available in the Microsoft Windows Software Development Kit (SDK) and in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="8a725-111">Las herramientas host de depuración WSD (wsddebug \_host.exe) y cliente de depuración WSD (wsddebug \_client.exe) ayudan a los desarrolladores a depurar sus clientes y hosts.</span><span class="sxs-lookup"><span data-stu-id="8a725-111">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools help developers debug their clients and hosts.</span></span> <span data-ttu-id="8a725-112">Estas herramientas se pueden usar para comprobar e inspeccionar el tráfico de intercambio de metadatos y WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="8a725-112">These tools can be used to verify and inspect WS-Discovery and metadata exchange traffic.</span></span> <span data-ttu-id="8a725-113">Para obtener más información sobre el host de depuración WSD y el cliente de depuración WSD, vea [herramientas de depuración](debugging-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8a725-113">For more information about WSD Debug Host and WSD Debug Client, see [Debugging Tools](debugging-tools.md).</span></span> <span data-ttu-id="8a725-114">Estas herramientas solo están disponibles en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8a725-114">These tools are available only in the Windows SDK.</span></span>

<span data-ttu-id="8a725-115">Hay una herramienta de desarrollo adicional, denominada [herramienta de interoperabilidad básica de WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), que solo está disponible en el WDK.</span><span class="sxs-lookup"><span data-stu-id="8a725-115">There is an additional development tool, named [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), that is available only in the WDK.</span></span> <span data-ttu-id="8a725-116">Esta herramienta se utiliza para probar los métodos de servicio, el mecanismo de optimización de transmisión de mensajes (MTOM), los datos adjuntos o WS-Eventing.</span><span class="sxs-lookup"><span data-stu-id="8a725-116">This tool is used for testing service methods, Message Transmission Optimization Mechanism (MTOM), attachments or WS-Eventing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a725-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a725-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a725-118">Desarrollo de aplicaciones WSD en Windows</span><span class="sxs-lookup"><span data-stu-id="8a725-118">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="8a725-119">Generador de código de servicios web en dispositivos</span><span class="sxs-lookup"><span data-stu-id="8a725-119">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="8a725-120">Herramienta de interoperabilidad básica de WSDAPI (WSDBIT)</span><span class="sxs-lookup"><span data-stu-id="8a725-120">WSDAPI Basic Interoperability Tool (WSDBIT)</span></span>](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[<span data-ttu-id="8a725-121">Herramientas de depuración</span><span class="sxs-lookup"><span data-stu-id="8a725-121">Debugging Tools</span></span>](debugging-tools.md)
</dt> </dl>

 

 



