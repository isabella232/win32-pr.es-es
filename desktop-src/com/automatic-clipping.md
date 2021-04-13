---
title: Recorte automático
description: Recorte automático
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357421"
---
# <a name="automatic-clipping"></a><span data-ttu-id="d3a38-103">Recorte automático</span><span class="sxs-lookup"><span data-stu-id="d3a38-103">Automatic Clipping</span></span>

<span data-ttu-id="d3a38-104">Se recomienda encarecidamente que un contenedor de controles ActiveX admita el recorte automático de sus controles.</span><span class="sxs-lookup"><span data-stu-id="d3a38-104">It is strongly recommended that an ActiveX control container supports automatic clipping of its controls.</span></span> <span data-ttu-id="d3a38-105">Esto dará lugar a una operación más eficaz para la mayoría de los controles.</span><span class="sxs-lookup"><span data-stu-id="d3a38-105">This will result in more efficient operation for most controls.</span></span> <span data-ttu-id="d3a38-106">Si se admite el recorte automático, se debe admitir la propiedad de ambiente AutoClip y tener un valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="d3a38-106">If automatic clipping is supported, the AutoClip ambient property must be supported and have a value of **TRUE**.</span></span>

<span data-ttu-id="d3a38-107">El recorte automático es la capacidad de un contenedor para asegurarse de que la salida dibujada de un control solo se dirige a la región de recorte actual del contenedor.</span><span class="sxs-lookup"><span data-stu-id="d3a38-107">Automatic clipping is the ability of a container to ensure that a control's drawn output goes only to the container's current clipping region.</span></span> <span data-ttu-id="d3a38-108">En un contenedor que admite el recorte automático, un control puede pintar sin tener en cuenta su región de recorte, ya que el contenedor recortará automáticamente cualquier dibujo que se produzca fuera del área del control.</span><span class="sxs-lookup"><span data-stu-id="d3a38-108">In a container that supports automatic clipping, a control can paint without regard to its clipping region, because the container will automatically clip any painting that occurs outside the control's area.</span></span> <span data-ttu-id="d3a38-109">Si un contenedor no admite el recorte automático, los controles generados por el CDK crearán una ventana primaria adicional si se pasa una región de recorte que no sea NULL.</span><span class="sxs-lookup"><span data-stu-id="d3a38-109">If a container does not support automatic clipping, then CDK-generated controls will create an extra parent window if a non-null clipping region is passed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3a38-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3a38-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3a38-111">Contenedores</span><span class="sxs-lookup"><span data-stu-id="d3a38-111">Containers</span></span>](containers.md)
</dt> </dl>

 

 




