---
description: En esta sección se muestra un problema que puede encontrarse al trabajar con ventanas de dispositivos en aplicaciones Direct3D.
ms.assetid: 7cfd2ad6-fb85-4303-9fa4-6fe7d16d9951
title: Trabajar con ventanas de dispositivos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56352ef0ec66def620a0ae0995d92d8b421722e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714671"
---
# <a name="working-with-device-windows-direct3d-9"></a><span data-ttu-id="8b02f-103">Trabajar con ventanas de dispositivos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8b02f-103">Working with Device Windows (Direct3D 9)</span></span>

<span data-ttu-id="8b02f-104">En esta sección se muestra un problema que puede encontrarse al trabajar con ventanas de dispositivos en aplicaciones Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8b02f-104">This section lists an issue that you might encounter when working with device windows in Direct3D applications.</span></span>

-   <span data-ttu-id="8b02f-105">Direct3D solo enlaza las ventanas de foco en lugar de la ventana de dispositivo con la función de procesamiento de mensajes de Direct3D y solo procesa los mensajes de la ventana de foco.</span><span class="sxs-lookup"><span data-stu-id="8b02f-105">Direct3D only hooks up the focus windows instead of the device window with the Direct3D message processing function, and only processes the focus window messages.</span></span> <span data-ttu-id="8b02f-106">Por lo tanto, la ventana de enfoque debe ser el elemento primario de cualquier ventana de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b02f-106">So, the focus window should be the parent of any device window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b02f-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b02f-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b02f-108">Sugerencias de programación</span><span class="sxs-lookup"><span data-stu-id="8b02f-108">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



