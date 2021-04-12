---
title: El método IOleContainer EnumObjects
description: El método IOleContainer EnumObjects
ms.assetid: 29562d0e-dc8b-49cd-a58f-1f3125a438ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a2dff2331374299abbc13cdd595aa709ec1aa74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268361"
---
# <a name="the-iolecontainerenumobjects-method"></a><span data-ttu-id="cf82d-103">El método IOleContainer:: EnumObjects</span><span class="sxs-lookup"><span data-stu-id="cf82d-103">The IOleContainer::EnumObjects Method</span></span>

<span data-ttu-id="cf82d-104">Este método se utiliza para enumerar todos los objetos OLE contenidos en un documento o formulario, devolviendo un puntero de interfaz para cada objeto OLE.</span><span class="sxs-lookup"><span data-stu-id="cf82d-104">This method is used to enumerate over all the OLE objects contained in a document or form, returning an interface pointer for each OLE object.</span></span> <span data-ttu-id="cf82d-105">El contenedor debe devolver punteros a cada objeto OLE que comparta el mismo contenedor.</span><span class="sxs-lookup"><span data-stu-id="cf82d-105">The container must return pointers to each OLE object that shares the same container.</span></span> <span data-ttu-id="cf82d-106">También se deben enumerar los formularios anidados o los controles anidados.</span><span class="sxs-lookup"><span data-stu-id="cf82d-106">Nested forms or nested controls must also be enumerated.</span></span>

<span data-ttu-id="cf82d-107">Algunos contenedores implementan controles extensores, que encapsulan controles que no son de ActiveX y, a continuación, devuelven punteros a estos controles extensores a medida que se enumera un formulario.</span><span class="sxs-lookup"><span data-stu-id="cf82d-107">Some containers implement extender controls, which wrap non-ActiveX controls, and then return pointers to these extender controls as a form is enumerated.</span></span> <span data-ttu-id="cf82d-108">Este comportamiento permite que los controles ActiveX y los contenedores de controles ActiveX se integren bien con controles no ActiveX y, por tanto, se recomienda, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="cf82d-108">This behavior enables ActiveX controls and ActiveX control containers to integrate well with non-ActiveX controls, and is thus recommended, but not required.</span></span>

 

 




