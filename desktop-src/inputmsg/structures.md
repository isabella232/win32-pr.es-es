---
title: Estructuras (mensajes de entrada de puntero y notificaciones)
description: En los temas de esta sección se proporcionan las especificaciones de referencia para los mensajes de entrada de puntero y las estructuras de notificaciones.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105721635"
---
# <a name="pointer-input-messages-and-notifications-structures"></a><span data-ttu-id="c44cb-103">Mensajes de entrada de puntero y estructuras de notificaciones</span><span class="sxs-lookup"><span data-stu-id="c44cb-103">Pointer Input Messages and Notifications structures</span></span>

<span data-ttu-id="c44cb-104">En los temas de esta sección se proporcionan las especificaciones de referencia para [los mensajes de entrada de puntero y](messages-and-notifications-portal.md) las estructuras de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="c44cb-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c44cb-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c44cb-105">In this section</span></span>



| <span data-ttu-id="c44cb-106">Tema</span><span class="sxs-lookup"><span data-stu-id="c44cb-106">Topic</span></span>                                                                            | <span data-ttu-id="c44cb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c44cb-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c44cb-108">**INPUT_TRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="c44cb-108">**INPUT_TRANSFORM**</span></span>](/previous-versions/windows/desktop/api)<br/>                           | <span data-ttu-id="c44cb-109">Define la matriz que representa una transformación en un consumidor de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c44cb-109">Defines the matrix that represents a transform on a message consumer.</span></span> <span data-ttu-id="c44cb-110">Esta matriz se puede usar para transformar datos de entrada de puntero de coordenadas de cliente a coordenadas de pantalla, mientras que el inverso se puede usar para transformar datos de entrada de puntero de coordenadas de pantalla a coordenadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="c44cb-110">This matrix can be used to transform pointer input data from client coordinates to screen coordinates, while the inverse can be used to transform pointer input data from screen coordinates to client coordinates.</span></span> <br/>                                                                 |
| [<span data-ttu-id="c44cb-111">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="c44cb-111">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                          | <span data-ttu-id="c44cb-112">Contiene información de puntero básica común a todos los tipos de puntero.</span><span class="sxs-lookup"><span data-stu-id="c44cb-112">Contains basic pointer information common to all pointer types.</span></span> <span data-ttu-id="c44cb-113">Las aplicaciones pueden recuperar esta información mediante las funciones [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) y [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="c44cb-113">Applications can retrieve this information using the [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) and [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) functions.</span></span> <br/> |
| [<span data-ttu-id="c44cb-114">**POINTER_PEN_INFO**</span><span class="sxs-lookup"><span data-stu-id="c44cb-114">**POINTER_PEN_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                 | <span data-ttu-id="c44cb-115">Define la información de lápiz básica común a todos los tipos de puntero.</span><span class="sxs-lookup"><span data-stu-id="c44cb-115">Defines basic pen information common to all pointer types.</span></span> <br/>                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="c44cb-116">**POINTER_TOUCH_INFO**</span><span class="sxs-lookup"><span data-stu-id="c44cb-116">**POINTER_TOUCH_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>             | <span data-ttu-id="c44cb-117">Define la información básica táctil común a todos los tipos de puntero.</span><span class="sxs-lookup"><span data-stu-id="c44cb-117">Defines basic touch information common to all pointer types.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="c44cb-118">**TOUCHPREDICTIONPARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="c44cb-118">**TOUCHPREDICTIONPARAMETERS**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="c44cb-119">Contiene los detalles de entrada de hardware que se pueden usar para predecir los destinos táctiles y ayudar a compensar la latencia de hardware al procesar la entrada táctil y de gestos que contiene datos de distancia y velocidad.</span><span class="sxs-lookup"><span data-stu-id="c44cb-119">Contains hardware input details that can be used to predict touch targets and help compensate for hardware latency when processing touch and gesture input that contains distance and velocity data.</span></span><br/>                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="c44cb-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c44cb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c44cb-121">Referencia de mensajes de entrada de puntero</span><span class="sxs-lookup"><span data-stu-id="c44cb-121">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





