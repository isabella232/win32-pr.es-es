---
title: Evento external. OnChangeViewOnlineListError
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | Evento external. OnChangeViewOnlineListError
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Media Player de eventos external. OnChangeViewOnlineListError de Windows
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700022"
---
# <a name="externalonchangeviewonlinelisterror-event"></a><span data-ttu-id="463a6-105">Evento external. OnChangeViewOnlineListError</span><span class="sxs-lookup"><span data-stu-id="463a6-105">External.OnChangeViewOnlineListError Event</span></span>

> [!Note]  
> <span data-ttu-id="463a6-106">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="463a6-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="463a6-107">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="463a6-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="463a6-108">El evento **OnChangeViewOnlineListError** se produce cuando una llamada al método [external. changeViewOnlineList](external-changeviewonlinelist.md) produce un error.</span><span class="sxs-lookup"><span data-stu-id="463a6-108">The **OnChangeViewOnlineListError** event occurs when a call to the [External.changeViewOnlineList](external-changeviewonlinelist.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a><span data-ttu-id="463a6-109">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="463a6-109">Possible Values</span></span>

<span data-ttu-id="463a6-110">Esta es una propiedad de solo escritura que especifica el nombre de la función en el script que Windows Media Player llama cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="463a6-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="463a6-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="463a6-111">Parameters</span></span>

<span data-ttu-id="463a6-112">La función que controla este error tiene los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="463a6-112">The function that handles this error has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="463a6-113"><span id="hr"></span><span id="HR"></span>*hora*</span><span class="sxs-lookup"><span data-stu-id="463a6-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="463a6-114">Código de error **HRESULT** que indica el motivo del error.</span><span class="sxs-lookup"><span data-stu-id="463a6-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="463a6-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span><span class="sxs-lookup"><span data-stu-id="463a6-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="463a6-116">La misma cadena que se pasó en el parámetro **LibraryLocationType** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="463a6-116">The same string that was passed in the **LibraryLocationType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="463a6-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span><span class="sxs-lookup"><span data-stu-id="463a6-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="463a6-118">La misma cadena que se pasó en el parámetro **LibraryLocationID** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="463a6-118">The same string that was passed in the **LibraryLocationID** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="463a6-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span><span class="sxs-lookup"><span data-stu-id="463a6-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span></span>
</dt> <dd>

<span data-ttu-id="463a6-120">La misma cadena que se pasó en el parámetro **params** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="463a6-120">The same string that was passed in the **Params** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="463a6-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="463a6-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span></span>
</dt> <dd>

<span data-ttu-id="463a6-122">La misma cadena que se pasó en el parámetro **FriendlyName** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="463a6-122">The same string that was passed in the **FriendlyName** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="463a6-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*</span><span class="sxs-lookup"><span data-stu-id="463a6-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*</span></span>
</dt> <dd>

<span data-ttu-id="463a6-124">La misma cadena que se pasó en el parámetro **ListType** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="463a6-124">The same string that was passed in the **ListType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="463a6-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span><span class="sxs-lookup"><span data-stu-id="463a6-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span></span>
</dt> <dd>

<span data-ttu-id="463a6-126">La misma cadena que se pasó en el parámetro **ViewMode** de **changeViewOnlineList**.</span><span class="sxs-lookup"><span data-stu-id="463a6-126">The same string that was passed in the **ViewMode** parameter of **changeViewOnlineList**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="463a6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="463a6-127">Requirements</span></span>



| <span data-ttu-id="463a6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="463a6-128">Requirement</span></span> | <span data-ttu-id="463a6-129">Value</span><span class="sxs-lookup"><span data-stu-id="463a6-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="463a6-130">Versión</span><span class="sxs-lookup"><span data-stu-id="463a6-130">Version</span></span><br/> | <span data-ttu-id="463a6-131">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="463a6-131">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="463a6-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="463a6-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="463a6-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="463a6-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="463a6-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="463a6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="463a6-135">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="463a6-135">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





