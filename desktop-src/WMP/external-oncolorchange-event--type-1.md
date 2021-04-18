---
title: Evento external. OnColorChange (tipo 1)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | Evento external. OnColorChange (tipo 1)
ms.assetid: 45e6ec4a-e680-4d50-8fb7-410f12383eef
keywords:
- Evento external. OnColorChange (tipo 1) Windows Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event (Type 1)
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11805cc154c60b8a765f46041f74d40929df418d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700021"
---
# <a name="externaloncolorchange-event-type-1"></a><span data-ttu-id="e1f62-105">Evento external. OnColorChange (tipo 1)</span><span class="sxs-lookup"><span data-stu-id="e1f62-105">External.OnColorChange Event (Type 1)</span></span>

> [!Note]  
> <span data-ttu-id="e1f62-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="e1f62-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="e1f62-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="e1f62-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="e1f62-108">El evento **OnColorChange** se produce cuando cambia el color de la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e1f62-108">The **OnColorChange** event occurs when the color of the Windows Media Player user interface changes.</span></span>

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="e1f62-109">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="e1f62-109">Possible Values</span></span>

<span data-ttu-id="e1f62-110">Esta es una propiedad de solo escritura que especifica el nombre de la función en el script que Windows Media Player llama cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="e1f62-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1f62-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1f62-111">Parameters</span></span>

<span data-ttu-id="e1f62-112">La función que controla este evento no toma ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="e1f62-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1f62-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1f62-113">Remarks</span></span>

<span data-ttu-id="e1f62-114">Los usuarios pueden cambiar el color de la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e1f62-114">Users can change the color of the Windows Media Player user interface.</span></span> <span data-ttu-id="e1f62-115">Puede usar este evento para personalizar la apariencia de la página web hospedada para que coincida con el reproductor.</span><span class="sxs-lookup"><span data-stu-id="e1f62-115">You can use this event to customize the appearance of your hosted webpage to match the Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1f62-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1f62-116">Requirements</span></span>



| <span data-ttu-id="e1f62-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1f62-117">Requirement</span></span> | <span data-ttu-id="e1f62-118">Value</span><span class="sxs-lookup"><span data-stu-id="e1f62-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f62-119">Versión</span><span class="sxs-lookup"><span data-stu-id="e1f62-119">Version</span></span><br/> | <span data-ttu-id="e1f62-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="e1f62-120">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="e1f62-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1f62-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1f62-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1f62-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1f62-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1f62-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f62-124">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="e1f62-124">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





