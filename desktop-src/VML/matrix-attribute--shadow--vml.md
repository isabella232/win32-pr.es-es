---
title: Atributo de matriz (sombra) (VML)
description: Atributo de matriz (sombra) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421320"
---
# <a name="matrix-attribute-shadowvml"></a><span data-ttu-id="fbcec-103">Atributo de matriz (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="fbcec-103">Matrix Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="fbcec-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fbcec-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fbcec-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="fbcec-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fbcec-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="fbcec-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fbcec-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="fbcec-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fbcec-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fbcec-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fbcec-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fbcec-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fbcec-110">Define una transformación de perspectiva para una sombra.</span><span class="sxs-lookup"><span data-stu-id="fbcec-110">Defines a perspective transform for a shadow.</span></span> <span data-ttu-id="fbcec-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fbcec-111">Read/write.</span></span> <span data-ttu-id="fbcec-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="fbcec-112">**String**.</span></span>

<span data-ttu-id="fbcec-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="fbcec-113">**Applies To**</span></span>

[<span data-ttu-id="fbcec-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="fbcec-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="fbcec-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="fbcec-115">**Tag Syntax**</span></span>

<span data-ttu-id="fbcec-116"><v: *Element* Matrix = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="fbcec-116"><v: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="fbcec-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="fbcec-117">**Script Syntax**</span></span>

<span data-ttu-id="fbcec-118">*Element* . Matrix = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="fbcec-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="fbcec-119">*expresión* = de *elemento*. Matrix</span><span class="sxs-lookup"><span data-stu-id="fbcec-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="fbcec-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="fbcec-120">**Remarks**</span></span>

<span data-ttu-id="fbcec-121">Una matriz de transformación de perspectiva con el formato "SXX, SXY, SYX, SYY, PX, py" donde s = scale y p = perspectiva.</span><span class="sxs-lookup"><span data-stu-id="fbcec-121">A perspective transform matrix in the form "sxx,sxy,syx,syy,px,py" where s= scale and p = perspective.</span></span> <span data-ttu-id="fbcec-122">Si el desplazamiento está en unidades absolutas, PX, py están en unidades de 1/UME; de lo contrario, se trata de una fracción inversa del tamaño de la forma.</span><span class="sxs-lookup"><span data-stu-id="fbcec-122">If offset is in absolute units then px, py are in 1/emu units; otherwise they are an inverse fraction of the shape size.</span></span>

<span data-ttu-id="fbcec-123">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="fbcec-123">*VML Standard Attribute*</span></span>

 

 