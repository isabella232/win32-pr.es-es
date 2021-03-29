---
title: Matrix (atributo) (sesgo) (VML)
description: Matrix (atributo) (sesgo) (VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078276"
---
# <a name="matrix-attribute-skewvml"></a><span data-ttu-id="4d348-103">Matrix (atributo) (sesgo) (VML)</span><span class="sxs-lookup"><span data-stu-id="4d348-103">Matrix Attribute (Skew)(VML)</span></span>

<span data-ttu-id="4d348-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4d348-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4d348-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="4d348-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4d348-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="4d348-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4d348-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="4d348-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4d348-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4d348-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4d348-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4d348-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4d348-110">Define una transformación de perspectiva de un sesgo.</span><span class="sxs-lookup"><span data-stu-id="4d348-110">Defines a perspective transform of a skew.</span></span> <span data-ttu-id="4d348-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d348-111">Read/write.</span></span> <span data-ttu-id="4d348-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="4d348-112">**String**.</span></span>

<span data-ttu-id="4d348-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="4d348-113">**Applies To**</span></span>

[<span data-ttu-id="4d348-114">Sesgar</span><span class="sxs-lookup"><span data-stu-id="4d348-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="4d348-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="4d348-115">**Tag Syntax**</span></span>

<span data-ttu-id="4d348-116"><o: *elemento* Matrix = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="4d348-116"><o: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="4d348-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="4d348-117">**Script Syntax**</span></span>

<span data-ttu-id="4d348-118">*Element* . Matrix = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="4d348-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="4d348-119">*expresión* = de *elemento*. Matrix</span><span class="sxs-lookup"><span data-stu-id="4d348-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="4d348-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="4d348-120">**Remarks**</span></span>

<span data-ttu-id="4d348-121">La matriz es una cadena con el formato "SXX, SXY, SYX, SYY, PX, py", donde s es Scale, p es Perspective y x e y son valores x e y.</span><span class="sxs-lookup"><span data-stu-id="4d348-121">The matrix is a string in the form "sxx, sxy, syx, syy, px, py" where s is scale, p is perspective, and x and y are x and y values.</span></span> <span data-ttu-id="4d348-122">Si el [desplazamiento](offset-attribute--skew--vml.md) está en unidades absolutas, PX y py están en [unidades](msdn-online-vml-units.md) de la UME ^-1 (de lo contrario, son una fracción inversa del tamaño de la forma).</span><span class="sxs-lookup"><span data-stu-id="4d348-122">If [Offset](offset-attribute--skew--vml.md) is in absolute units, then px and py are in emu^-1 [units](msdn-online-vml-units.md) (otherwise they are an inverse fraction of the shape size).</span></span> <span data-ttu-id="4d348-123">El valor predeterminado es "1, 0, 0, 1, 0".</span><span class="sxs-lookup"><span data-stu-id="4d348-123">The default value is "1,0,0,1,0,0".</span></span>

<span data-ttu-id="4d348-124">*Microsoft Office atributo Extensions*</span><span class="sxs-lookup"><span data-stu-id="4d348-124">*Microsoft Office Extensions Attribute*</span></span>

 

 