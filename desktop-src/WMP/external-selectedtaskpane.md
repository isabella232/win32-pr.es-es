---
title: External. SelectedTaskPane
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad SelectedTaskPane especifica o recupera el panel de tareas seleccionado actualmente.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- Media Player de Windows externa. SelectedTaskPane
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698576"
---
# <a name="externalselectedtaskpane"></a><span data-ttu-id="3e538-106">External. SelectedTaskPane</span><span class="sxs-lookup"><span data-stu-id="3e538-106">External.SelectedTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="3e538-107">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="3e538-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="3e538-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="3e538-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="3e538-109">La propiedad **SelectedTaskPane** especifica o recupera el panel de tareas seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="3e538-109">The **SelectedTaskPane** property specifies or retrieves the currently selected task pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e538-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e538-110">Syntax</span></span>

<span data-ttu-id="3e538-111">Window. external. SelectedTaskPane = *servicetask*</span><span class="sxs-lookup"><span data-stu-id="3e538-111">window.external.SelectedTaskPane = *servicetask*</span></span>

## <a name="possible-values"></a><span data-ttu-id="3e538-112">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="3e538-112">Possible Values</span></span>

<span data-ttu-id="3e538-113">Esta propiedad es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="3e538-113">This property is a read/write **String**.</span></span> <span data-ttu-id="3e538-114">Los valores posibles son "ServiceTask1", "ServiceTask2" y "ServiceTask3".</span><span class="sxs-lookup"><span data-stu-id="3e538-114">Possible values are "ServiceTask1", "ServiceTask2", and "ServiceTask3".</span></span>

## <a name="remarks"></a><span data-ttu-id="3e538-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e538-115">Remarks</span></span>

<span data-ttu-id="3e538-116">Al especificar un valor para esta propiedad, se resalta el botón de ese panel.</span><span class="sxs-lookup"><span data-stu-id="3e538-116">Specifying a value for this property highlights the button for that pane.</span></span> <span data-ttu-id="3e538-117">No hace que el panel de tareas especificado esté activo.</span><span class="sxs-lookup"><span data-stu-id="3e538-117">It does not make the specified task pane active.</span></span> <span data-ttu-id="3e538-118">Debe especificar un valor para esta propiedad para establecer el botón actual del panel de tareas de la página web cuando la página se carga para asegurarse de que el botón del panel de tareas correcto está activo.</span><span class="sxs-lookup"><span data-stu-id="3e538-118">You should specify a value for this property to set the current task pane button for your webpage when the page loads to ensure that the correct task pane button is active.</span></span>

<span data-ttu-id="3e538-119">Para hacer que un panel de tareas determinado sea el activo, use el método **NavigateTaskPaneURL** .</span><span class="sxs-lookup"><span data-stu-id="3e538-119">To make a particular task pane the active one, use the **NavigateTaskPaneURL** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e538-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e538-120">Requirements</span></span>



| <span data-ttu-id="3e538-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e538-121">Requirement</span></span> | <span data-ttu-id="3e538-122">Value</span><span class="sxs-lookup"><span data-stu-id="3e538-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3e538-123">Versión</span><span class="sxs-lookup"><span data-stu-id="3e538-123">Version</span></span><br/> | <span data-ttu-id="3e538-124">Windows Media Player 10 o posterior</span><span class="sxs-lookup"><span data-stu-id="3e538-124">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="3e538-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e538-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3e538-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e538-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e538-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e538-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e538-128">**Objeto externo para las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="3e538-128">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="3e538-129">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="3e538-129">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





