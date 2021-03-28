---
description: La región de actualización identifica la parte de una ventana que no está actualizada o no es válida y en la que es necesario volver a dibujar.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: La región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e670bac065782a1e09c4d142f964aaea97d4b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997913"
---
# <a name="the-update-region"></a><span data-ttu-id="f0046-103">La región de actualización</span><span class="sxs-lookup"><span data-stu-id="f0046-103">The Update Region</span></span>

<span data-ttu-id="f0046-104">La *región de actualización* identifica la parte de una ventana que no está actualizada o no es válida y en la que es necesario volver a dibujar.</span><span class="sxs-lookup"><span data-stu-id="f0046-104">The *update region* identifies the portion of a window that is out-of-date or invalid and in need of redrawing.</span></span> <span data-ttu-id="f0046-105">El sistema utiliza la región de actualización para generar mensajes de [**WM \_ Paint**](wm-paint.md) para las aplicaciones y para minimizar el tiempo que las aplicaciones dedican a poner el contenido de sus ventanas al día.</span><span class="sxs-lookup"><span data-stu-id="f0046-105">The system uses the update region to generate [**WM\_PAINT**](wm-paint.md) messages for applications and to minimize the time applications spend bringing the contents of their windows up to date.</span></span> <span data-ttu-id="f0046-106">El sistema solo agrega la parte no válida de la ventana a la región de actualización, por lo que solo se debe dibujar esa parte.</span><span class="sxs-lookup"><span data-stu-id="f0046-106">The system adds only the invalid portion of the window to the update region, requiring only that portion to be drawn.</span></span>

<span data-ttu-id="f0046-107">Cuando el sistema determina que es necesario actualizar una ventana, establece las dimensiones de la región de actualización en la parte no válida de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f0046-107">When the system determines that a window needs updating, it sets the dimensions of the update region to the invalid portion of the window.</span></span> <span data-ttu-id="f0046-108">La configuración de la región de actualización no hace que la aplicación se dibuje inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f0046-108">Setting the update region does not immediately cause the application to draw.</span></span> <span data-ttu-id="f0046-109">En su lugar, la aplicación continúa recuperando mensajes de la cola de mensajes de la aplicación hasta que no quedan mensajes.</span><span class="sxs-lookup"><span data-stu-id="f0046-109">Instead, the application continues retrieving messages from the application message queue until no messages remain.</span></span> <span data-ttu-id="f0046-110">Después, el sistema comprueba la región de actualización y, si la región no está vacía (no NULL), envía un mensaje de [**\_ dibujo de WM**](wm-paint.md) al procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="f0046-110">The system then checks the update region, and if the region is not empty (non-NULL), it sends a [**WM\_PAINT**](wm-paint.md) message to the window procedure.</span></span>

<span data-ttu-id="f0046-111">Una aplicación puede usar la región de actualización para generar sus mensajes de [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="f0046-111">An application can use the update region to generate its [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="f0046-112">Por ejemplo, una aplicación que carga datos de archivos abiertos normalmente establece la región de actualización durante la carga, de modo que los nuevos datos se dibujen durante el procesamiento del siguiente mensaje de **\_ dibujo de WM** .</span><span class="sxs-lookup"><span data-stu-id="f0046-112">For example, an application that loads data from open files typically sets the update region while loading so that new data is drawn during processing of the next **WM\_PAINT** message.</span></span> <span data-ttu-id="f0046-113">En general, una aplicación no debe dibujar en el momento en que los datos cambian, pero enrutar todas las operaciones de dibujo a través del mensaje de **\_ Paint de WM** .</span><span class="sxs-lookup"><span data-stu-id="f0046-113">In general, an application should not draw at the time its data changes, but route all drawing operations through the **WM\_PAINT** message.</span></span>

 

 



