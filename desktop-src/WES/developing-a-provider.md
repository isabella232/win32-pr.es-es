---
title: Desarrollo de un proveedor
description: Para escribir los eventos que defina en el manifiesto, use las funciones incluidas en la API de seguimiento de eventos (ETW). Para obtener más información sobre cómo escribir un proveedor, consulte proporcionar eventos.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149556"
---
# <a name="developing-a-provider"></a><span data-ttu-id="4caa9-104">Desarrollo de un proveedor</span><span class="sxs-lookup"><span data-stu-id="4caa9-104">Developing a Provider</span></span>

<span data-ttu-id="4caa9-105">Para escribir los eventos que defina en el manifiesto, use las funciones incluidas en la API de [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="4caa9-105">To write the events that you define in your manifest, you use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span> <span data-ttu-id="4caa9-106">Para obtener más información sobre cómo escribir un proveedor, consulte [proporcionar eventos](/windows/desktop/ETW/providing-events).</span><span class="sxs-lookup"><span data-stu-id="4caa9-106">For details on writing a provider, see [Providing Events](/windows/desktop/ETW/providing-events).</span></span>

<span data-ttu-id="4caa9-107">Después de escribir el proveedor, utilice la herramienta WevtUtil.exe para registrar el proveedor y el esquema.</span><span class="sxs-lookup"><span data-stu-id="4caa9-107">After writing the provider, use the WevtUtil.exe tool to register the provider and schema.</span></span> <span data-ttu-id="4caa9-108">Para más información sobre el uso de WevtUtil, consulte [herramientas de registro de eventos de Windows](windows-event-log-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4caa9-108">For details on using WevtUtil, see [Windows Event Log Tools](windows-event-log-tools.md).</span></span> <span data-ttu-id="4caa9-109">A continuación se muestra cómo usar WevtUtil para registrar un proveedor y para quitar el registro.</span><span class="sxs-lookup"><span data-stu-id="4caa9-109">The following shows how to use WevtUtil to register a provider and to remove the registration.</span></span>


```cmd
wevtutil im provider.man

wevtutil um provider.man
```