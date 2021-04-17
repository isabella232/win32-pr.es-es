---
description: La tabla ComPlus contiene información necesaria para instalar aplicaciones COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Tabla de ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653025"
---
# <a name="complus-table"></a><span data-ttu-id="0c243-103">Tabla de ComPlus</span><span class="sxs-lookup"><span data-stu-id="0c243-103">Complus Table</span></span>

<span data-ttu-id="0c243-104">La tabla ComPlus contiene información necesaria para instalar aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="0c243-104">The Complus table contains information needed to install COM+ applications.</span></span>

<span data-ttu-id="0c243-105">La tabla ComPlus tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="0c243-105">The Complus table has the following columns.</span></span>



| <span data-ttu-id="0c243-106">Columna</span><span class="sxs-lookup"><span data-stu-id="0c243-106">Column</span></span>      | <span data-ttu-id="0c243-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c243-107">Type</span></span>                         | <span data-ttu-id="0c243-108">Clave</span><span class="sxs-lookup"><span data-stu-id="0c243-108">Key</span></span> | <span data-ttu-id="0c243-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="0c243-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="0c243-110">Componente\_</span><span class="sxs-lookup"><span data-stu-id="0c243-110">Component\_</span></span> | [<span data-ttu-id="0c243-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="0c243-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="0c243-112">Y</span><span class="sxs-lookup"><span data-stu-id="0c243-112">Y</span></span>   | <span data-ttu-id="0c243-113">N</span><span class="sxs-lookup"><span data-stu-id="0c243-113">N</span></span>        |
| <span data-ttu-id="0c243-114">ExpType</span><span class="sxs-lookup"><span data-stu-id="0c243-114">ExpType</span></span>     | [<span data-ttu-id="0c243-115">Entero</span><span class="sxs-lookup"><span data-stu-id="0c243-115">Integer</span></span>](integer.md)       | <span data-ttu-id="0c243-116">N</span><span class="sxs-lookup"><span data-stu-id="0c243-116">N</span></span>   | <span data-ttu-id="0c243-117">Y</span><span class="sxs-lookup"><span data-stu-id="0c243-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0c243-118">Columnas</span><span class="sxs-lookup"><span data-stu-id="0c243-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0c243-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="0c243-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="0c243-120">Una clave externa en la primera columna de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="0c243-120">An external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="0c243-121">Este es el componente que contiene la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="0c243-121">This is the component that contains the COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="0c243-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span><span class="sxs-lookup"><span data-stu-id="0c243-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span></span>
</dt> <dd>

<span data-ttu-id="0c243-123">Exporte las marcas usadas durante la generación del archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="0c243-123">Export flags used during the generation of the .msi file.</span></span> <span data-ttu-id="0c243-124">Para obtener más información, vea la documentación de COM+ en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0c243-124">For more information see the COM+ documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c243-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c243-125">Remarks</span></span>

<span data-ttu-id="0c243-126">Vea la [acción RegisterComPlus](registercomplus-action.md) y la [acción UnregisterComPlus](unregistercomplus-action.md).</span><span class="sxs-lookup"><span data-stu-id="0c243-126">See the [RegisterComPlus action](registercomplus-action.md) and [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

<span data-ttu-id="0c243-127">Vea [instalar una aplicación com+ con el Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="0c243-127">See [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span></span>

## <a name="validation"></a><span data-ttu-id="0c243-128">Validación</span><span class="sxs-lookup"><span data-stu-id="0c243-128">Validation</span></span>

<dl>

[<span data-ttu-id="0c243-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="0c243-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="0c243-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="0c243-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="0c243-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="0c243-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="0c243-132">ICE66</span><span class="sxs-lookup"><span data-stu-id="0c243-132">ICE66</span></span>](ice66.md)  
</dl>

 

 



