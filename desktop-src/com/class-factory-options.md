---
title: Opciones del generador de clases
description: Opciones del generador de clases
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793972"
---
# <a name="class-factory-options"></a><span data-ttu-id="66927-103">Opciones del generador de clases</span><span class="sxs-lookup"><span data-stu-id="66927-103">Class Factory Options</span></span>

<span data-ttu-id="66927-104">Un control ActiveX, en virtud de ser un objeto COM, debe tener un código de servidor asociado que admita la creación de controles mediante [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) como mínimo.</span><span class="sxs-lookup"><span data-stu-id="66927-104">An ActiveX Control, by virtue of being a COM object, must have associated server code that supports control creation through [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) as a minimum.</span></span>

<span data-ttu-id="66927-105">Es opcional, no es necesario, que este objeto de clase también admite [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) para la administración de licencias.</span><span class="sxs-lookup"><span data-stu-id="66927-105">It is optional, not required, that this class object also support [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) for licensing management.</span></span> <span data-ttu-id="66927-106">Solo los proveedores que preocupan sobre las licencias deben ser compatibles con el mecanismo de concesión de licencias de COM.</span><span class="sxs-lookup"><span data-stu-id="66927-106">Only those vendors that are concerned about licensing need to support COM's licensing mechanism.</span></span> <span data-ttu-id="66927-107">En otras palabras, dado que **IClassFactory2** es la única manera de lograr licencias de nivel com, esta interfaz es necesaria en el objeto de clase para los controles que desean tener licencia.</span><span class="sxs-lookup"><span data-stu-id="66927-107">In other words, because **IClassFactory2** is the only way to achieve COM-level licensing, this interface is required on the class object for those controls that want to be licensed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66927-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66927-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66927-109">Controles</span><span class="sxs-lookup"><span data-stu-id="66927-109">Controls</span></span>](controls.md)
</dt> </dl>

 

 