---
title: Propiedad Ribbon. QuickAccessToolbar
description: Representa un contenedor para la barra de herramientas de acceso rápido (QAT).
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- Ribbon. QuickAccessToolbar (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0e09b220bd60b60ccbb8ee05c2da9c4317ba78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421953"
---
# <a name="ribbonquickaccesstoolbar-property"></a><span data-ttu-id="25944-104">Propiedad Ribbon. QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="25944-104">Ribbon.QuickAccessToolbar property</span></span>

<span data-ttu-id="25944-105">Representa un contenedor para la barra de herramientas de acceso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="25944-105">Represents a container for the Quick Access Toolbar (QAT).</span></span>

## <a name="usage"></a><span data-ttu-id="25944-106">Uso</span><span class="sxs-lookup"><span data-stu-id="25944-106">Usage</span></span>

``` syntax
<Ribbon.QuickAccessToolbar>
  child elements
</Ribbon.QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="25944-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="25944-107">Attributes</span></span>

<span data-ttu-id="25944-108">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="25944-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="25944-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25944-109">Child elements</span></span>



| <span data-ttu-id="25944-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="25944-110">Element</span></span>                                                                           | <span data-ttu-id="25944-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="25944-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="25944-112">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="25944-112">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md)<br/> | <span data-ttu-id="25944-113">Debe aparecer exactamente una vez</span><span class="sxs-lookup"><span data-stu-id="25944-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="25944-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="25944-114">Parent elements</span></span>



| <span data-ttu-id="25944-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="25944-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="25944-116">**Cinta de opciones**</span><span class="sxs-lookup"><span data-stu-id="25944-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="25944-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25944-117">Remarks</span></span>

<span data-ttu-id="25944-118">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="25944-118">Required.</span></span>

<span data-ttu-id="25944-119">Puede producirse una o varias veces para cada [**cinta**](windowsribbon-element-ribbon.md)de opciones.</span><span class="sxs-lookup"><span data-stu-id="25944-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="25944-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="25944-120">Examples</span></span>

<span data-ttu-id="25944-121">En el ejemplo siguiente se muestra el marcado básico para el elemento **Ribbon. QuickAccessToolbar** .</span><span class="sxs-lookup"><span data-stu-id="25944-121">The following example demonstrates the basic markup for the **Ribbon.QuickAccessToolbar** element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a><span data-ttu-id="25944-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25944-122">Requirements</span></span>



| <span data-ttu-id="25944-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="25944-123">Requirement</span></span> | <span data-ttu-id="25944-124">Value</span><span class="sxs-lookup"><span data-stu-id="25944-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="25944-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25944-125">Minimum supported client</span></span><br/> | <span data-ttu-id="25944-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="25944-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="25944-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25944-127">Minimum supported server</span></span><br/> | <span data-ttu-id="25944-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="25944-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





