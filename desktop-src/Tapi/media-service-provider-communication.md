---
description: A partir de Windows 2000, los proveedores de servicios de telefonía que negocian una versión de 3,0 o posterior deben tener un proveedor de servicios multimedia correspondiente.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Comunicación del proveedor de servicios multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a50ec6a4fb96a86ceab3a302b138ee72d6c61b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361894"
---
# <a name="media-service-provider-communication"></a><span data-ttu-id="909af-103">Comunicación del proveedor de servicios multimedia</span><span class="sxs-lookup"><span data-stu-id="909af-103">Media Service Provider Communication</span></span>

<span data-ttu-id="909af-104">A partir de Windows 2000, los proveedores de servicios de telefonía que negocian una versión de 3,0 o posterior deben tener un proveedor de servicios multimedia correspondiente.</span><span class="sxs-lookup"><span data-stu-id="909af-104">Starting with Windows 2000 telephony service providers that negotiate a version of 3.0 or later must have a matching media service provider.</span></span> <span data-ttu-id="909af-105">La división precisa de Responsabilidades operativas depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="909af-105">The precise division of operational responsibilities is implementation dependent.</span></span> <span data-ttu-id="909af-106">Por ejemplo, un TSP podría usar el MSP coincidente para realizar la determinación del tipo de medio en una sesión entrante.</span><span class="sxs-lookup"><span data-stu-id="909af-106">For example, a TSP might use the matching MSP to perform media type determination on an incoming session.</span></span> <span data-ttu-id="909af-107">Sin embargo, el TSP debe cumplir el TSPI, lo que significa obtener esa determinación del MSP e informar a TAPI.</span><span class="sxs-lookup"><span data-stu-id="909af-107">However, the TSP must conform to the TSPI, which means getting that determination from the MSP and reporting it to TAPI.</span></span>

<span data-ttu-id="909af-108">TSPI proporciona las siguientes funciones y mensajes para permitir una conexión virtual entre un TSP y un MSP:</span><span class="sxs-lookup"><span data-stu-id="909af-108">TSPI provides the following functions and messages to allow a virtual connection between a TSP and an MSP:</span></span>

-   [<span data-ttu-id="909af-109">**TSPI \_ lineCloseMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="909af-109">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [<span data-ttu-id="909af-110">**TSPI \_ lineCreateMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="909af-110">**TSPI\_lineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [<span data-ttu-id="909af-111">**TSPI \_ lineMSPIdentify**</span><span class="sxs-lookup"><span data-stu-id="909af-111">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [<span data-ttu-id="909af-112">**TSPI \_ lineReceiveMSPData**</span><span class="sxs-lookup"><span data-stu-id="909af-112">**TSPI\_lineReceiveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [<span data-ttu-id="909af-113">**LÍNEA \_ QOSINFO**</span><span class="sxs-lookup"><span data-stu-id="909af-113">**LINE\_QOSINFO**</span></span>](line-qosinfo.md)
-   [<span data-ttu-id="909af-114">**LÍNEA \_ SENDMSPDATA**</span><span class="sxs-lookup"><span data-stu-id="909af-114">**LINE\_SENDMSPDATA**</span></span>](line-sendmspdata.md)

 

 
