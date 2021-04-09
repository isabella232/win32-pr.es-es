---
title: Atributo de bajorrelieve (VML)
description: Atributo de bajorrelieve (VML)
ms.assetid: b50f900a-b0dc-4042-af9e-050011307765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83f2ea38ef4ca90f6687196335d2edd2d39c09c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149351"
---
# <a name="vml-inset-attribute"></a><span data-ttu-id="8bdbc-103">Atributo de bajorrelieve (VML)</span><span class="sxs-lookup"><span data-stu-id="8bdbc-103">VML Inset Attribute</span></span>

<span data-ttu-id="8bdbc-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8bdbc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8bdbc-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="8bdbc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8bdbc-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="8bdbc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8bdbc-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="8bdbc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8bdbc-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8bdbc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8bdbc-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8bdbc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8bdbc-110">Especifica los valores de margen interno del texto del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="8bdbc-110">Specifies inner margin values for textbox text.</span></span> <span data-ttu-id="8bdbc-111">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8bdbc-111">Read/write.</span></span> <span data-ttu-id="8bdbc-112">**Cadena**.</span><span class="sxs-lookup"><span data-stu-id="8bdbc-112">**String**.</span></span>

<span data-ttu-id="8bdbc-113">**Se aplica a**</span><span class="sxs-lookup"><span data-stu-id="8bdbc-113">**Applies To**</span></span>

[<span data-ttu-id="8bdbc-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="8bdbc-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="8bdbc-115">**Sintaxis de etiquetas**</span><span class="sxs-lookup"><span data-stu-id="8bdbc-115">**Tag Syntax**</span></span>

<span data-ttu-id="8bdbc-116"><v: *elemento* bajorrelieve = " *expresión* " ></span><span class="sxs-lookup"><span data-stu-id="8bdbc-116"><v: *element* inset=" *expression* "></span></span>

<span data-ttu-id="8bdbc-117">**Sintaxis de script**</span><span class="sxs-lookup"><span data-stu-id="8bdbc-117">**Script Syntax**</span></span>

<span data-ttu-id="8bdbc-118">*Element* . bajorrelieve = "*expresión*"</span><span class="sxs-lookup"><span data-stu-id="8bdbc-118">*element* .inset="*expression*"</span></span>

<span data-ttu-id="8bdbc-119">*expresión* = de *elemento*. bajorrelieve</span><span class="sxs-lookup"><span data-stu-id="8bdbc-119">*expression*=*element*.inset</span></span>

<span data-ttu-id="8bdbc-120">**Comentarios:**</span><span class="sxs-lookup"><span data-stu-id="8bdbc-120">**Remarks**</span></span>

<span data-ttu-id="8bdbc-121">El valor del margen de texto interno se especifica como una cadena que contiene cuatro valores, separados por comas o espacios.</span><span class="sxs-lookup"><span data-stu-id="8bdbc-121">The internal text margin value is specified as a string containing four values, each separated by commas or spaces.</span></span> <span data-ttu-id="8bdbc-122">Los valores se miden desde los bordes izquierdo, superior, derecho e inferior del cuadro especificado por el atributo [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) de **path**.</span><span class="sxs-lookup"><span data-stu-id="8bdbc-122">The values measure inset from the left, top, right, and bottom edges of the box specified by the [TextBoxRect](msdn-online-vml-textboxrect-attribute.md) attribute of **Path**.</span></span> <span data-ttu-id="8bdbc-123">Los valores que faltan se establecen en el valor predeterminado, que es "0.1 en, 0,05 en, 0.1 en, 0,05 en".</span><span class="sxs-lookup"><span data-stu-id="8bdbc-123">Missing values are set to the default, which is "0.1in, 0.05in, 0.1in, 0.05in".</span></span>

<span data-ttu-id="8bdbc-124">En el caso de las formas giradas en los exploradores que no admiten la rotación, el cuadro de límite se ajustará al múltiplo más cercano de 90 grados.</span><span class="sxs-lookup"><span data-stu-id="8bdbc-124">For rotated shapes in browsers that do not support rotation, the bounding box will snap to the closest multiple of 90 degrees.</span></span>

<span data-ttu-id="8bdbc-125">*Atributo estándar de VML*</span><span class="sxs-lookup"><span data-stu-id="8bdbc-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="8bdbc-126">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="8bdbc-126">**Example**</span></span>

<span data-ttu-id="8bdbc-127">El cuadro de texto tendrá un margen de bajorrelieve de 10 píxeles.</span><span class="sxs-lookup"><span data-stu-id="8bdbc-127">The textbox will have an inset margin of 10 pixels.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox" inset="10px, 10px, 10px, 10px">
   VML
   </v:textbox/>
   </v:shape>
```



 

 