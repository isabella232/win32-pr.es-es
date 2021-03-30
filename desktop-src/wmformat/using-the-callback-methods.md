---
title: Usar los métodos de devolución de llamada
description: Usar los métodos de devolución de llamada
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- SDK de Windows Media Format, métodos de devolución de llamada
- SDK de Windows Media Format, métodos denominados de forma asincrónica
- métodos de devolución de llamada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788703"
---
# <a name="using-the-callback-methods"></a><span data-ttu-id="27363-106">Usar los métodos de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="27363-106">Using the Callback Methods</span></span>

<span data-ttu-id="27363-107">Varias interfaces del SDK de Windows Media Format contienen métodos a los que se llama de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="27363-107">Several interfaces in the Windows Media Format SDK contain methods that are called asynchronously.</span></span> <span data-ttu-id="27363-108">La mayoría de estos métodos usan funciones de devolución de llamada para pasar información a la aplicación de control.</span><span class="sxs-lookup"><span data-stu-id="27363-108">Most of these methods use callback functions to pass information to the controlling application.</span></span>

<span data-ttu-id="27363-109">En las secciones siguientes se describen algunos de los problemas generales relacionados con el uso de métodos de devolución de llamada con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="27363-109">The following sections describe some of the general issues regarding the use of callback methods with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="27363-110">Sección</span><span class="sxs-lookup"><span data-stu-id="27363-110">Section</span></span>                                                                          | <span data-ttu-id="27363-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="27363-111">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27363-112">Usar la devolución de llamada en estado</span><span class="sxs-lookup"><span data-stu-id="27363-112">Using the OnStatus Callback</span></span>](using-the-onstatus-callback.md)                   | <span data-ttu-id="27363-113">Describe cómo implementar el método de devolución de llamada [**IWMStatusCallback:: Alstatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , que utilizan varios objetos para notificar a las aplicaciones el progreso de la operación del SDK.</span><span class="sxs-lookup"><span data-stu-id="27363-113">Describes how to implement the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, which is used by several objects to advise applications of SDK operation progress.</span></span> |
| [<span data-ttu-id="27363-114">Usar eventos con llamadas asincrónicas</span><span class="sxs-lookup"><span data-stu-id="27363-114">Using Events with Asynchronous Calls</span></span>](using-events-with-asynchronous-calls.md) | <span data-ttu-id="27363-115">Describe una técnica común para controlar las llamadas a métodos asincrónicos en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="27363-115">Describes a common technique to handle asynchronous method calls in an application.</span></span>                                                                                                                  |
| [<span data-ttu-id="27363-116">Usar el parámetro de contexto</span><span class="sxs-lookup"><span data-stu-id="27363-116">Using the Context Parameter</span></span>](using-the-context-parameter.md)                   | <span data-ttu-id="27363-117">Presenta el parámetro *pvContext* , compartido por varias devoluciones de llamada y sus métodos de llamada, y explica cómo utilizarla.</span><span class="sxs-lookup"><span data-stu-id="27363-117">Introduces the *pvContext* parameter, shared by several callbacks and their calling methods, and explains how to use it.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="27363-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27363-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27363-119">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="27363-119">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




