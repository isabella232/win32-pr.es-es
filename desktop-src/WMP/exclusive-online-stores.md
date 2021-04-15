---
title: Tiendas en línea exclusivas
description: Tiendas en línea exclusivas
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player tiendas en línea, exclusivas
- tiendas en línea, exclusivas
- tipo 1 tiendas en línea, exclusivas
- tipo 2 tiendas en línea, exclusivas
- tiendas en línea exclusivas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695532"
---
# <a name="exclusive-online-stores"></a><span data-ttu-id="7ea02-108">Tiendas en línea exclusivas</span><span class="sxs-lookup"><span data-stu-id="7ea02-108">Exclusive Online Stores</span></span>

<span data-ttu-id="7ea02-109">Con Windows Media Player 11, una aplicación que incrusta el control del reproductor de forma remota puede especificar una tienda en línea exclusiva.</span><span class="sxs-lookup"><span data-stu-id="7ea02-109">With Windows Media Player 11, an application that embeds the Player control remotely can specify an exclusive online store.</span></span> <span data-ttu-id="7ea02-110">En ese caso, el selector de servicio de Windows Media Player está deshabilitado y solo la tienda en línea especificada está disponible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="7ea02-110">In that case, the service selector in Windows Media Player is disabled, and only the specified online store is available to the user.</span></span> <span data-ttu-id="7ea02-111">Además, Windows Media Player adopta el color especificado por el elemento **color** del documento ServiceInfo de la tienda en línea exclusiva.</span><span class="sxs-lookup"><span data-stu-id="7ea02-111">Also, Windows Media Player adopts the color specified by the **Color** element of the exclusive online store's ServiceInfo document.</span></span>

<span data-ttu-id="7ea02-112">Para especificar una tienda en línea exclusiva, una aplicación debe anexar ExclusiveService:*keyName* al final de la cadena que devuelve de [IWMPRemoteMediaServices:: GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span><span class="sxs-lookup"><span data-stu-id="7ea02-112">To specify an exclusive online store, an application must append ExclusiveService:*keyname* to the end of the string that it returns from [IWMPRemoteMediaServices::GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span></span> <span data-ttu-id="7ea02-113">Por ejemplo, supongamos que Proseware es el nombre de clave que se asigna a una tienda en línea determinada.</span><span class="sxs-lookup"><span data-stu-id="7ea02-113">For example, suppose Proseware is the key name given to a particular online store.</span></span> <span data-ttu-id="7ea02-114">Si **GetServiceType** devuelve la cadena "Remote ExclusiveService: Proseware", Proseware será la única tienda en línea disponible en el control Player Embedded de forma remota.</span><span class="sxs-lookup"><span data-stu-id="7ea02-114">If **GetServiceType** returns the string "Remote ExclusiveService:Proseware", then Proseware will be the only online store available in the remotely embedded Player control.</span></span>

<span data-ttu-id="7ea02-115">Una aplicación puede limitar el Media Player de Windows a una tienda en línea exclusiva solo si Windows Media Player no se está ejecutando cuando se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7ea02-115">An application can limit Windows Media Player to an exclusive online store only if Windows Media Player is not already running when the application is launched.</span></span> <span data-ttu-id="7ea02-116">Es responsabilidad de la aplicación informar al usuario de que debe cerrar Windows Media Player antes de ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7ea02-116">It is the application's responsibility to inform the user that he or she must close Windows Media Player before running the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ea02-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7ea02-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ea02-118">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="7ea02-118">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="7ea02-119">**Control remoto del Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7ea02-119">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




