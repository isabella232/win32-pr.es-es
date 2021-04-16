---
description: Un proveedor de servicios multimedia (MSP) permite que una aplicación controle los medios de un mecanismo de transporte determinado.
ms.assetid: f886380f-d970-4511-bf71-fb1eb767e4f4
title: Proveedores de servicios multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd78f5ff4a13da4365f99bd2cb539738b6f3fd6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689640"
---
# <a name="media-service-providers"></a><span data-ttu-id="b587c-103">Proveedores de servicios multimedia</span><span class="sxs-lookup"><span data-stu-id="b587c-103">Media Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="b587c-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="b587c-104">Purpose</span></span>

<span data-ttu-id="b587c-105">Un proveedor de servicios multimedia (MSP) permite que una aplicación controle los medios de un mecanismo de transporte determinado.</span><span class="sxs-lookup"><span data-stu-id="b587c-105">A media service provider (MSP) enables an application to control media for a particular transport mechanism.</span></span> <span data-ttu-id="b587c-106">Un MSP siempre se empareja con un proveedor de servicios de telefonía (TSP).</span><span class="sxs-lookup"><span data-stu-id="b587c-106">An MSP is always paired with a Telephony Service Provider (TSP).</span></span>

<span data-ttu-id="b587c-107">La interfaz del proveedor de servicios multimedia (MSPI) es un conjunto de interfaces y métodos implementados por un MSP para permitir un control de la aplicación sobre el transporte multimedia durante una sesión de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="b587c-107">The Media Service Provider Interface (MSPI) is a set of interfaces and methods implemented by an MSP to allow an application control over media transport during a communications session.</span></span> <span data-ttu-id="b587c-108">Un MSP controla los mecanismos específicos del dispositivo y específicos del protocolo necesarios para activar estos controles y se comunica con su TSP emparejado o con una aplicación mediante el uso de los métodos proporcionados en MSPI.</span><span class="sxs-lookup"><span data-stu-id="b587c-108">An MSP handles the device-specific and protocol-specific mechanisms required to enact these controls, and communicates with its paired TSP or an application through use of the methods provided in the MSPI.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b587c-109">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="b587c-109">Developer audience</span></span>

<span data-ttu-id="b587c-110">Es necesario estar familiarizado con COM.</span><span class="sxs-lookup"><span data-stu-id="b587c-110">Familiarity with COM is required.</span></span> <span data-ttu-id="b587c-111">La experiencia de desarrollo con las telecomunicaciones y otras aplicaciones de telefonía es útil, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="b587c-111">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b587c-112">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="b587c-112">Run-time requirements</span></span>

<span data-ttu-id="b587c-113">MSPI permite el desarrollo de proveedores de servicios multimedia para determinados protocolos o dispositivos que se ejecutan en sistemas operativos Windows Server 2003, Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b587c-113">MSPI enables development of media service providers for particular protocols or devices running on Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b587c-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b587c-114">In this section</span></span>



| <span data-ttu-id="b587c-115">Tema</span><span class="sxs-lookup"><span data-stu-id="b587c-115">Topic</span></span>                                                                       | <span data-ttu-id="b587c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b587c-116">Description</span></span>                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b587c-117">Información general</span><span class="sxs-lookup"><span data-stu-id="b587c-117">Overview</span></span>](about-the-media-service-provider-msp-.md)<br/>            | <span data-ttu-id="b587c-118">Información general sobre la arquitectura y los componentes de MSP.</span><span class="sxs-lookup"><span data-stu-id="b587c-118">General information about MSP architecture and components.</span></span><br/> |
| [<span data-ttu-id="b587c-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="b587c-119">Reference</span></span>](media-service-provider-interface-mspi-reference.md)<br/> | <span data-ttu-id="b587c-120">Documentación de las interfaces MSPI.</span><span class="sxs-lookup"><span data-stu-id="b587c-120">Documentation for the MSPI interfaces.</span></span><br/>                     |



 

## <a name="related-topics"></a><span data-ttu-id="b587c-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b587c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b587c-122">Introducción a la telefonía de Microsoft</span><span class="sxs-lookup"><span data-stu-id="b587c-122">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="b587c-123">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="b587c-123">TAPI 3.1</span></span>](tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="b587c-124">Proveedores de servicios de telefonía</span><span class="sxs-lookup"><span data-stu-id="b587c-124">Telephony Service Providers</span></span>](./telephony-service-providers-start-page.md)
</dt> </dl>

 

