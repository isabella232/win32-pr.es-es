---
title: Error de tabIndex del contenedor de ARIA
description: Error de tabIndex del contenedor de ARIA
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- AriaContainerTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419067"
---
# <a name="aria-container-tabindex-error"></a><span data-ttu-id="6ab1e-104">Error de tabIndex del contenedor de ARIA</span><span class="sxs-lookup"><span data-stu-id="6ab1e-104">ARIA Container Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="6ab1e-105">Texto</span><span class="sxs-lookup"><span data-stu-id="6ab1e-105">Text</span></span>

<span data-ttu-id="6ab1e-106">El elemento es un contenedor enfocable con descendientes activos definidos pero sin el valor de **TabIndex** mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="6ab1e-106">Element is a focusable container with active descendants defined but without **tabindex** value greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="6ab1e-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ab1e-107">Type</span></span>

<span data-ttu-id="6ab1e-108">Error</span><span class="sxs-lookup"><span data-stu-id="6ab1e-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="6ab1e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ab1e-109">Description</span></span>

<span data-ttu-id="6ab1e-110">Este error se aplica a los elementos que tienen el atributo **Aria-activedescendant** , no se deshabilitan y no tienen el atributo **TabIndex** establecido en un valor mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="6ab1e-110">This error applies to elements that have the **aria-activedescendant** attribute, are not disabled, and do not have the **tabindex** attribute set to a value that is greater than or equal to 0.</span></span> <span data-ttu-id="6ab1e-111">Estos elementos deben estar en el orden de tabulación porque son responsables de controlar los eventos de teclado de sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="6ab1e-111">These elements must be in tab order because they are responsible for handling keyboard events for their child elements.</span></span>

<span data-ttu-id="6ab1e-112">Para corregir este error, establezca el atributo **TabIndex** en un valor que sea mayor o igual que 0.</span><span class="sxs-lookup"><span data-stu-id="6ab1e-112">To fix this error, set the **tabindex** attribute to a value that is greater than or equal to 0.</span></span>

## <a name="example"></a><span data-ttu-id="6ab1e-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ab1e-113">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
       <div role="option" id="listbox1-1" class="selected">Item 1</div> 
       <div role="option" id="listbox1-2">Item 2</div> 

       <div role="option" id="listbox1-3">Item 3</div>
      ... 
<div>
```



## <a name="related-topics"></a><span data-ttu-id="6ab1e-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ab1e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab1e-115">Error de tabIndex del rol de contenedor de ARIA (sin activos descendientes)</span><span class="sxs-lookup"><span data-stu-id="6ab1e-115">ARIA Container Role (without active descendant) Tabindex Error</span></span>](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




