---
description: Guardar y restaurar objetos DvdState
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Guardar y restaurar objetos DvdState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677097"
---
# <a name="saving-and-restoring-dvdstate-objects"></a><span data-ttu-id="d86b9-103">Guardar y restaurar objetos DvdState</span><span class="sxs-lookup"><span data-stu-id="d86b9-103">Saving and Restoring DvdState Objects</span></span>

<span data-ttu-id="d86b9-104">Los objetos [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) permiten a las aplicaciones guardar una instantánea de la sesión de usuario, incluida información como la ubicación actual en el disco, el nivel parental de la persona que está viendo, los flujos de audio y subimágenes seleccionados, etc.</span><span class="sxs-lookup"><span data-stu-id="d86b9-104">[**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) objects enable applications to save a snapshot of the user session, including information such as the current location on the disc, the parental level of the person who is viewing, the selected audio and subpicture streams, and so on.</span></span> <span data-ttu-id="d86b9-105">Esto significa que los usuarios pueden guardar su lugar en un disco DVD-Video y verlo en otro momento.</span><span class="sxs-lookup"><span data-stu-id="d86b9-105">This means that users can save their place on a DVD-Video disc and watch it at a later time.</span></span>

<span data-ttu-id="d86b9-106">Las aplicaciones no pueden crear objetos DvdState.</span><span class="sxs-lookup"><span data-stu-id="d86b9-106">Applications cannot create DvdState objects.</span></span> <span data-ttu-id="d86b9-107">El navegador de DVD crea estos objetos internamente cuando una aplicación llama a [**IDvdInfo2:: GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span><span class="sxs-lookup"><span data-stu-id="d86b9-107">These objects are created internally by the DVD Navigator when an application calls [**IDvdInfo2::GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span></span> <span data-ttu-id="d86b9-108">Los objetos DvdState exponen la interfaz [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) para permitir que las aplicaciones consulten cierta información.</span><span class="sxs-lookup"><span data-stu-id="d86b9-108">DvdState objects expose the [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) interface to allow applications to query for certain information.</span></span>

<span data-ttu-id="d86b9-109">En la aplicación de ejemplo de DVD, las funciones **CDvdCore:: RestoreBookmark** y **CDvdCore:: SaveBookmark** muestran cómo guardar y recuperar objetos DvdState.</span><span class="sxs-lookup"><span data-stu-id="d86b9-109">In the DVD sample application, the **CDvdCore::RestoreBookmark** and **CDvdCore::SaveBookmark** functions show how to save and retrieve DvdState objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d86b9-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d86b9-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d86b9-111">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="d86b9-111">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



