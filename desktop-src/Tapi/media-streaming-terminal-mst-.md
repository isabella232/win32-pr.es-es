---
description: El terminal de transmisión por secuencias multimedia (MST) es un terminal dinámico basado en el uso de filtros de DirectShow. Un MSP escrito mediante las clases base de TAPI 3 MSP incorporará un MST, pero los autores de MSP pueden optar por implementarlo sin usar las clases base.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Terminal de streaming multimedia (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb9bb4b97d0e741aec96454b187beefe2d21eb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003370"
---
# <a name="media-streaming-terminal-mst"></a><span data-ttu-id="8e45a-104">Terminal de streaming multimedia (MST)</span><span class="sxs-lookup"><span data-stu-id="8e45a-104">Media Streaming Terminal (MST)</span></span>

<span data-ttu-id="8e45a-105">El terminal de transmisión por secuencias multimedia (MST) es un terminal dinámico basado en el uso de filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8e45a-105">The Media Streaming Terminal (MST) is a dynamic terminal based on use of DirectShow filters.</span></span> <span data-ttu-id="8e45a-106">Un MSP escrito mediante las [clases base de TAPI 3 MSP](tapi-3-msp-base-classes.md) incorporará un MST, pero los autores de MSP pueden optar por implementarlo sin usar las clases base.</span><span class="sxs-lookup"><span data-stu-id="8e45a-106">An MSP written using the [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md) will incorporate an MST, but MSP authors may choose to implement it without using the base classes.</span></span>

<span data-ttu-id="8e45a-107">Para invocar la creación de MST, una aplicación realiza una llamada a [**ITTerminalSupport:: CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) con *PTERMINALCLASS* establecido en CLSID \_ MediaStreamTerminal.</span><span class="sxs-lookup"><span data-stu-id="8e45a-107">To invoke MST creation, an application makes a call to [**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) using *pTerminalClass* set to CLSID\_MediaStreamTerminal.</span></span>

<span data-ttu-id="8e45a-108">A continuación, se exponen las interfaces [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) y [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) en el terminal, lo que permite a una aplicación optimizar el rendimiento de streaming.</span><span class="sxs-lookup"><span data-stu-id="8e45a-108">The [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) and [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) interfaces are then exposed on the terminal, allowing an application to tune streaming performance.</span></span> <span data-ttu-id="8e45a-109">Estas interfaces se declaran en Tapi3. h.</span><span class="sxs-lookup"><span data-stu-id="8e45a-109">These interfaces are declared in Tapi3.h.</span></span>

<span data-ttu-id="8e45a-110">La implementación y el uso de un MST requiere estar familiarizado con los filtros de DirectShow y la administración de gráficos de filtros.</span><span class="sxs-lookup"><span data-stu-id="8e45a-110">Implementation and use of an MST requires familiarity with DirectShow filters and filter graph management.</span></span> <span data-ttu-id="8e45a-111">Consulte el material de DirectShow en el nodo gráficos y servicios multimedia del kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="8e45a-111">Please refer to the DirectShow material under the Graphic and Multimedia Services node of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="8e45a-112">La referencia de streaming multimedia será especialmente útil para los autores de MSP.</span><span class="sxs-lookup"><span data-stu-id="8e45a-112">The Multimedia Streaming Reference will be particularly useful to MSP authors.</span></span>

 

 
