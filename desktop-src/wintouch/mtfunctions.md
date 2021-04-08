---
title: Funciones (entrada táctil de Windows)
description: Esta sección contiene funciones para la entrada táctil de Windows.
ms.assetid: 6c64ed75-37ac-47ae-b39e-bdf10d2b5211
keywords:
- Windows Touch, funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a18ba246ab8b1d228d257d32982e9afc2c418eb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078782"
---
# <a name="functions-windows-touch-input"></a><span data-ttu-id="42f27-104">Funciones (entrada táctil de Windows)</span><span class="sxs-lookup"><span data-stu-id="42f27-104">Functions (Windows Touch Input)</span></span>

<span data-ttu-id="42f27-105">Esta sección contiene funciones para la entrada táctil de Windows.</span><span class="sxs-lookup"><span data-stu-id="42f27-105">This section contains functions for Windows Touch input.</span></span>

<span data-ttu-id="42f27-106">Las siguientes funciones se usan para la entrada táctil de Windows.</span><span class="sxs-lookup"><span data-stu-id="42f27-106">The following functions are used for Windows Touch input.</span></span>



| <span data-ttu-id="42f27-107">Función</span><span class="sxs-lookup"><span data-stu-id="42f27-107">Function</span></span>                                                                                               | <span data-ttu-id="42f27-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="42f27-108">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42f27-109">**CloseTouchInputHandle**</span><span class="sxs-lookup"><span data-stu-id="42f27-109">**CloseTouchInputHandle**</span></span>](/windows/desktop/api/winuser/nf-winuser-closetouchinputhandle)                                                 | <span data-ttu-id="42f27-110">Cierra un identificador de entrada táctil, libera la memoria de proceso asociada a él e invalida el identificador.</span><span class="sxs-lookup"><span data-stu-id="42f27-110">Closes a touch input handle, frees process memory associated with it, and invalidates the handle.</span></span>                                       |
| [<span data-ttu-id="42f27-111">**GetTouchInputInfo**</span><span class="sxs-lookup"><span data-stu-id="42f27-111">**GetTouchInputInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo)                                                         | <span data-ttu-id="42f27-112">Recupera información detallada sobre las entradas táctiles asociadas a un controlador de entrada táctil específico.</span><span class="sxs-lookup"><span data-stu-id="42f27-112">Retrieves detailed information about touch inputs associated with a specific touch input handle.</span></span>                                        |
| [<span data-ttu-id="42f27-113">**IsTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="42f27-113">**IsTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-istouchwindow)                                                                 | <span data-ttu-id="42f27-114">Comprueba si una ventana especificada es compatible con funciones táctiles y, opcionalmente, recupera el conjunto de marcadores modificadores para la funcionalidad táctil de la ventana.</span><span class="sxs-lookup"><span data-stu-id="42f27-114">Checks whether a specified window is touch-capable and, optionally, retrieves the modifier flags set for the window's touch capability.</span></span> |
| [<span data-ttu-id="42f27-115">**RegisterTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="42f27-115">**RegisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)                                                     | <span data-ttu-id="42f27-116">Registra una ventana como compatible con la funcionalidad táctil.</span><span class="sxs-lookup"><span data-stu-id="42f27-116">Registers a window as being touch-capable.</span></span>                                                                                              |
| [<span data-ttu-id="42f27-117">**UnregisterTouchWindow**</span><span class="sxs-lookup"><span data-stu-id="42f27-117">**UnregisterTouchWindow**</span></span>](/windows/desktop/api/winuser/nf-winuser-unregistertouchwindow)                                                 | <span data-ttu-id="42f27-118">Registra una ventana como que ya no es compatible con Touch.</span><span class="sxs-lookup"><span data-stu-id="42f27-118">Registers a window as no longer being touch-capable.</span></span>                                                                                    |
| [<span data-ttu-id="42f27-119">SendMessage, PostMessage y funciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="42f27-119">SendMessage, PostMessage, and Related Functions</span></span>](sendmessage--postmessage--and-related-functions.md) | <span data-ttu-id="42f27-120">Contiene consideraciones sobre el reenvío de mensajes.</span><span class="sxs-lookup"><span data-stu-id="42f27-120">Contains considerations about forwarding messages.</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="42f27-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42f27-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42f27-122">Entrada táctil de Windows</span><span class="sxs-lookup"><span data-stu-id="42f27-122">Windows Touch Input</span></span>](multi-touch-input.md)
</dt> <dt>

[<span data-ttu-id="42f27-123">Guía de programación de entrada táctil de Windows</span><span class="sxs-lookup"><span data-stu-id="42f27-123">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 




