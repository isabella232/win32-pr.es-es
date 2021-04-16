---
title: Seguimiento de referencias
description: Seguimiento de referencias
ms.assetid: 1e2cf555-3b96-42d5-a0bb-abb720c93520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45607a495e973ec33acde6d97cb1f83259a27c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488318"
---
# <a name="reference-tracking"></a><span data-ttu-id="1ad78-103">Seguimiento de referencias</span><span class="sxs-lookup"><span data-stu-id="1ad78-103">Reference Tracking</span></span>

<span data-ttu-id="1ad78-104">El seguimiento de referencias puede evitar la versión temprana accidental o malintencionada de los objetos.</span><span class="sxs-lookup"><span data-stu-id="1ad78-104">Reference tracking can prevent the unintentional or malicious early release of objects.</span></span>

<span data-ttu-id="1ad78-105">Al habilitar el seguimiento de referencias, se solicita que COM autentique las llamadas [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) distribuidas.</span><span class="sxs-lookup"><span data-stu-id="1ad78-105">When you enable reference tracking, you are requesting that distributed [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls be authenticated by COM.</span></span> <span data-ttu-id="1ad78-106">Cuando el seguimiento de referencias está habilitado, COM realiza un seguimiento de los recuentos de referencias por usuario para que un usuario pueda llamar a **Release** solo en los objetos en los que el usuario llamó a **AddRef** previamente.</span><span class="sxs-lookup"><span data-stu-id="1ad78-106">When reference tracking is enabled, COM keeps track of per-user reference counts so that a user can call **Release** only on objects that the user previously called **AddRef** on.</span></span> <span data-ttu-id="1ad78-107">Aunque el seguimiento de referencia puede reducir el rendimiento, garantiza que, independientemente del número de veces que un usuario determinado llame a **Release**, los objetos y códigos auxiliares seguirán existiendo si otra persona tiene una referencia a ellos.</span><span class="sxs-lookup"><span data-stu-id="1ad78-107">Although reference tracking can decrease performance, it ensures that no matter how many times a given user calls **Release**, the objects and stubs will still exist if someone else has a reference to them.</span></span>

<span data-ttu-id="1ad78-108">El cliente puede establecer el seguimiento de referencia para un proceso pasando la marca de la capacidad de EOAC \_ Secure \_ Refs en una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="1ad78-108">The client can set reference tracking for a process by passing the EOAC\_SECURE\_REFS capability flag in a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="1ad78-109">También puede habilitar o deshabilitar el seguimiento de referencias para todas las aplicaciones de un equipo mediante Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="1ad78-109">You can also enable or disable reference tracking for all applications on a computer by using Dcomcnfg.exe.</span></span>

<span data-ttu-id="1ad78-110">Si está habilitado el seguimiento de referencias, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) siempre usa la configuración de seguridad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1ad78-110">If reference tracking is enabled, [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) always uses default security settings.</span></span> <span data-ttu-id="1ad78-111">En este caso, se producirá un error en las llamadas a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) en **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="1ad78-111">In this case, calls to [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) on **IUnknown** will fail.</span></span>

 

 