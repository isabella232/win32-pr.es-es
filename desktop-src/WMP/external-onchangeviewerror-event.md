---
title: Evento external. OnChangeViewError
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | Evento external. OnChangeViewError
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Media Player de eventos external. OnChangeViewError de Windows
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bcbb71e1c5324a9907d735492364561be49a60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700023"
---
# <a name="externalonchangeviewerror-event"></a><span data-ttu-id="684e3-105">Evento external. OnChangeViewError</span><span class="sxs-lookup"><span data-stu-id="684e3-105">External.OnChangeViewError Event</span></span>

> [!Note]  
> <span data-ttu-id="684e3-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="684e3-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="684e3-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="684e3-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="684e3-108">El evento **OnChangeViewError** se produce cuando una llamada al método [external. changeView](external-changeview.md) produce un error.</span><span class="sxs-lookup"><span data-stu-id="684e3-108">The **OnChangeViewError** event occurs when a call to the [External.changeView](external-changeview.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="684e3-109">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="684e3-109">Possible Values</span></span>

<span data-ttu-id="684e3-110">Esta es una propiedad de solo escritura que especifica el nombre de la función en el script que Windows Media Player llama cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="684e3-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="684e3-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="684e3-111">Parameters</span></span>

<span data-ttu-id="684e3-112">La función que controla este evento tiene los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="684e3-112">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="684e3-113"><span id="hr"></span><span id="HR"></span>*hora*</span><span class="sxs-lookup"><span data-stu-id="684e3-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="684e3-114">Código de error **HRESULT** que indica el motivo del error.</span><span class="sxs-lookup"><span data-stu-id="684e3-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="684e3-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span><span class="sxs-lookup"><span data-stu-id="684e3-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="684e3-116">La misma cadena que se pasó en el parámetro **LibraryLocationType** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="684e3-116">The same string that was passed in the **LibraryLocationType** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="684e3-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span><span class="sxs-lookup"><span data-stu-id="684e3-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="684e3-118">La misma cadena thatwas se pasa en el parámetro **LibraryLocationID** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="684e3-118">The same string thatwas passed in the **LibraryLocationID** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="684e3-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filtro*</span><span class="sxs-lookup"><span data-stu-id="684e3-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filter*</span></span>
</dt> <dd>

<span data-ttu-id="684e3-120">La misma cadena que se pasó en el parámetro de **filtro** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="684e3-120">The same string that was passed in the **Filter** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="684e3-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span><span class="sxs-lookup"><span data-stu-id="684e3-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span></span>
</dt> <dd>

<span data-ttu-id="684e3-122">La misma cadena que se pasó en el parámetro **ViewParams** de **changeView**.</span><span class="sxs-lookup"><span data-stu-id="684e3-122">The same string that was passed in the **ViewParams** parameter of **changeView**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="684e3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="684e3-123">Requirements</span></span>



| <span data-ttu-id="684e3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="684e3-124">Requirement</span></span> | <span data-ttu-id="684e3-125">Value</span><span class="sxs-lookup"><span data-stu-id="684e3-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="684e3-126">Versión</span><span class="sxs-lookup"><span data-stu-id="684e3-126">Version</span></span><br/> | <span data-ttu-id="684e3-127">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="684e3-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="684e3-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="684e3-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="684e3-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="684e3-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="684e3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="684e3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684e3-131">**ExternalObject para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="684e3-131">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





