---
title: Propiedad Ribbon. HelpButton
description: Representa un contenedor para el botón ayuda.
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Ribbon. HelpButton (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802870"
---
# <a name="ribbonhelpbutton-property"></a><span data-ttu-id="10b14-104">Propiedad Ribbon. HelpButton</span><span class="sxs-lookup"><span data-stu-id="10b14-104">Ribbon.HelpButton property</span></span>

<span data-ttu-id="10b14-105">Representa un contenedor para el [botón ayuda](windowsribbon-controls-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="10b14-105">Represents a container for the [Help Button](windowsribbon-controls-helpbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="10b14-106">Uso</span><span class="sxs-lookup"><span data-stu-id="10b14-106">Usage</span></span>

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a><span data-ttu-id="10b14-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="10b14-107">Attributes</span></span>

<span data-ttu-id="10b14-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="10b14-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="10b14-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="10b14-109">Child elements</span></span>



| <span data-ttu-id="10b14-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="10b14-110">Element</span></span>                                                           | <span data-ttu-id="10b14-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="10b14-111">Description</span></span>                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="10b14-112">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="10b14-112">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)<br/> | <span data-ttu-id="10b14-113">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="10b14-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="10b14-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="10b14-114">Parent elements</span></span>



| <span data-ttu-id="10b14-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="10b14-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="10b14-116">**Cinta de opciones**</span><span class="sxs-lookup"><span data-stu-id="10b14-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="10b14-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10b14-117">Remarks</span></span>

<span data-ttu-id="10b14-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="10b14-118">Optional.</span></span>

<span data-ttu-id="10b14-119">Puede producirse al menos una vez para cada [**cinta**](windowsribbon-element-ribbon.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="10b14-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="10b14-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="10b14-120">Examples</span></span>

<span data-ttu-id="10b14-121">En el ejemplo siguiente se muestra el marcado básico necesario para implementar un botón de ayuda de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="10b14-121">The following example demonstrates the basic markup that is required to implement a Ribbon Help button.</span></span>

<span data-ttu-id="10b14-122">En esta sección de código se muestra la declaración de comando **Ribbon. HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="10b14-122">This section of code shows the **Ribbon.HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="10b14-123">En esta sección de código se muestra la declaración de control **Ribbon. HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="10b14-123">This section of code shows the **Ribbon.HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a><span data-ttu-id="10b14-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10b14-124">Requirements</span></span>



| <span data-ttu-id="10b14-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="10b14-125">Requirement</span></span> | <span data-ttu-id="10b14-126">Value</span><span class="sxs-lookup"><span data-stu-id="10b14-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="10b14-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10b14-127">Minimum supported client</span></span><br/> | <span data-ttu-id="10b14-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="10b14-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="10b14-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10b14-129">Minimum supported server</span></span><br/> | <span data-ttu-id="10b14-130">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="10b14-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





