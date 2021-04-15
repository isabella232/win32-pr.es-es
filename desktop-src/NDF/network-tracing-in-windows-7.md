---
title: Seguimiento de red en Windows 7
description: Windows 7 se expande en el marco de diagnóstico de redes (NDF) para proporcionar un método rápido para solucionar problemas de conectividad de red habilitando la recopilación de toda la información necesaria en un solo paso y aprovechando el seguimiento de eventos para Windows (ETW) para registrar los paquetes de eventos de red en un único archivo.
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421382"
---
# <a name="network-tracing-in-windows-7"></a><span data-ttu-id="cd422-103">Seguimiento de red en Windows 7</span><span class="sxs-lookup"><span data-stu-id="cd422-103">Network Tracing in Windows 7</span></span>

<span data-ttu-id="cd422-104">A medida que aumenta la complejidad de la pila de red, a menudo resulta difícil realizar un seguimiento de los problemas y diagnosticarlos rápidamente en la pila.</span><span class="sxs-lookup"><span data-stu-id="cd422-104">As the complexity of the networking stack increases, it is often difficult to quickly trace and diagnose issues within the stack.</span></span> <span data-ttu-id="cd422-105">Windows 7 se expande en el marco de diagnóstico de redes (NDF) para proporcionar un método rápido para solucionar problemas de conectividad de red habilitando la recopilación de toda la información necesaria en un solo paso y aprovechando el [seguimiento de eventos para Windows (ETW)](../etw/event-tracing-portal.md) para registrar eventos de red & paquetes en un único archivo.</span><span class="sxs-lookup"><span data-stu-id="cd422-105">Windows 7 expands on the Network Diagnostic Framework (NDF) to provide a quick method for troubleshooting network connectivity issues by enabling collection of all the needed information in one step, and by leveraging [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) to log network events & packets in a single file.</span></span>

<span data-ttu-id="cd422-106">Los eventos y paquetes relacionados se agrupan para una actividad determinada, como explorar un sitio web, entre los distintos componentes de la pila de red.</span><span class="sxs-lookup"><span data-stu-id="cd422-106">Related events and packets are grouped together for a given activity, such as browsing a website, across the various components in the networking stack.</span></span> <span data-ttu-id="cd422-107">El resultado de este proceso es un archivo de registro de seguimiento de eventos (ETL).</span><span class="sxs-lookup"><span data-stu-id="cd422-107">The output of this process is an Event Trace Log (ETL) file.</span></span> <span data-ttu-id="cd422-108">Al permitir que todos los eventos relacionados con una actividad específica se vean a la vez en este archivo, se puede reducir considerablemente el tiempo necesario para aislar y diagnosticar problemas de red.</span><span class="sxs-lookup"><span data-stu-id="cd422-108">By allowing all of the events related to a specific activity to be viewed at once in this file, the time required to isolate and diagnose network issues can be greatly reduced.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cd422-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="cd422-109">In This Section</span></span>



| <span data-ttu-id="cd422-110">Tema</span><span class="sxs-lookup"><span data-stu-id="cd422-110">Topic</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd422-111">Seguimiento de red en Windows 7: arquitectura</span><span class="sxs-lookup"><span data-stu-id="cd422-111">Network Tracing in Windows 7: Architecture</span></span>](network-tracing-in-windows-7-architecture.md)                                |
| [<span data-ttu-id="cd422-112">Herramientas para solucionar problemas con el seguimiento de red en Windows 7</span><span class="sxs-lookup"><span data-stu-id="cd422-112">Tools for Troubleshooting using Network Tracing in Windows 7</span></span>](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [<span data-ttu-id="cd422-113">Seguimiento de red en Windows 7: escenarios</span><span class="sxs-lookup"><span data-stu-id="cd422-113">Network Tracing in Windows 7: Scenarios</span></span>](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 