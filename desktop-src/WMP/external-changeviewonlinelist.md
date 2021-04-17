---
title: External. changeViewOnlineList (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. | External. changeViewOnlineList (método)
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- método changeViewOnlineList de Windows Media Player
- método changeViewOnlineList de Windows Media Player, clase externa
- Clase externa Windows Media Player, método changeViewOnlineList
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75e36adfa79b62863c3de78acf2adbd65011417b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700026"
---
# <a name="externalchangeviewonlinelist-method"></a><span data-ttu-id="fb60a-107">External. changeViewOnlineList (método)</span><span class="sxs-lookup"><span data-stu-id="fb60a-107">External.changeViewOnlineList method</span></span>

> [!Note]  
> <span data-ttu-id="fb60a-108">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="fb60a-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="fb60a-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="fb60a-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="fb60a-110">El método **changeViewOnlineList** cambia la vista en Windows Media Player para mostrar una lista generada dinámicamente por la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="fb60a-110">The **changeViewOnlineList** method changes the view in Windows Media Player to display a list generated dynamically by the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb60a-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb60a-111">Syntax</span></span>


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
)
```



## <a name="parameters"></a><span data-ttu-id="fb60a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb60a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb60a-113">*LibraryLocationType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb60a-113">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb60a-114">Una [constante de ubicación de biblioteca](library-location-constants.md) que especifica el tipo de la nueva vista.</span><span class="sxs-lookup"><span data-stu-id="fb60a-114">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="fb60a-115">Por ejemplo, la constante CPGenreID especifica que la nueva vista mostrará un género determinado.</span><span class="sxs-lookup"><span data-stu-id="fb60a-115">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="fb60a-116">*LibraryLocationID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb60a-116">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb60a-117">**Cadena** que contiene el identificador del elemento específico que se va a mostrar en la nueva vista.</span><span class="sxs-lookup"><span data-stu-id="fb60a-117">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="fb60a-118">Por ejemplo, si *LibraryLocationType* es CPGenreID, este parámetro especifica el identificador del género que se va a mostrar en la nueva vista.</span><span class="sxs-lookup"><span data-stu-id="fb60a-118">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="fb60a-119">Esta cadena puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="fb60a-119">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="fb60a-120">*Parámetros* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb60a-120">*Params* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb60a-121">**Cadena** que contiene los parámetros que Windows Media Player pasa al complemento de la tienda en línea mediante una llamada a [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span><span class="sxs-lookup"><span data-stu-id="fb60a-121">**String** containing parameters that Windows Media Player passes along to the online store's plug-in by calling [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate).</span></span> <span data-ttu-id="fb60a-122">Estos parámetros no son interpretados por Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="fb60a-122">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="fb60a-123">Los crea la tienda en línea y solo tienen significado en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="fb60a-123">They are created by the online store and have meaning only to the online store.</span></span> <span data-ttu-id="fb60a-124">Esta cadena puede estar vacía</span><span class="sxs-lookup"><span data-stu-id="fb60a-124">This string can be empty</span></span>

</dd> <dt>

<span data-ttu-id="fb60a-125">*FriendlyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb60a-125">*FriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb60a-126">**Cadena** que contiene un nombre descriptivo que se mostrará en Windows Media Player para la lista dinámica.</span><span class="sxs-lookup"><span data-stu-id="fb60a-126">**String** containing a friendly name, to be displayed by Windows Media Player, for the dynamic list.</span></span>

</dd> <dt>

<span data-ttu-id="fb60a-127">*ListType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb60a-127">*ListType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb60a-128">Una constante de ubicación de biblioteca que especifica el tipo de los elementos de la lista generada dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="fb60a-128">A library location constant that specifies the type of the items in the dynamically generated list.</span></span> <span data-ttu-id="fb60a-129">Por ejemplo, si el valor de este parámetro es CPTrackID, la lista dinámica contendrá pistas.</span><span class="sxs-lookup"><span data-stu-id="fb60a-129">For example, if the value of this parameter is CPTrackID, then the dynamic list will contain tracks.</span></span>

</dd> <dt>

<span data-ttu-id="fb60a-130">*ViewMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb60a-130">*ViewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb60a-131">**Cadena** que especifica el modo que Windows Media Player usará para mostrar la lista dinámica.</span><span class="sxs-lookup"><span data-stu-id="fb60a-131">**String** that specifies the mode that Windows Media Player will use to display the dynamic list.</span></span> <span data-ttu-id="fb60a-132">El autor de la llamada debe establecer este parámetro en uno de los valores siguientes, que se definen en contentpartner. h:</span><span class="sxs-lookup"><span data-stu-id="fb60a-132">The caller must set this parameter to one of the following values, which are defined in contentpartner.h:</span></span>

<span data-ttu-id="fb60a-133">ViewModeReport</span><span class="sxs-lookup"><span data-stu-id="fb60a-133">ViewModeReport</span></span>

<span data-ttu-id="fb60a-134">ViewModeDetails</span><span class="sxs-lookup"><span data-stu-id="fb60a-134">ViewModeDetails</span></span>

<span data-ttu-id="fb60a-135">ViewModeIcon</span><span class="sxs-lookup"><span data-stu-id="fb60a-135">ViewModeIcon</span></span>

<span data-ttu-id="fb60a-136">ViewModeTile</span><span class="sxs-lookup"><span data-stu-id="fb60a-136">ViewModeTile</span></span>

<span data-ttu-id="fb60a-137">ViewModeOrderedList</span><span class="sxs-lookup"><span data-stu-id="fb60a-137">ViewModeOrderedList</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb60a-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb60a-138">Return value</span></span>

<span data-ttu-id="fb60a-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fb60a-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb60a-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb60a-140">Remarks</span></span>

<span data-ttu-id="fb60a-141">Cuando el script de una página de detección llama a **changeViewOnlineList**, Windows Media Player pasa algunos de los parámetros a los métodos [IWMPContentPartner:: GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) y [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) , que se implementan mediante el complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="fb60a-141">When script on a discovery page calls **changeViewOnlineList**, Windows Media Player passes some of the parameters along to the [IWMPContentPartner::GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) and [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) methods, which are implemented by the online store's plug-in.</span></span> <span data-ttu-id="fb60a-142">En la tabla siguiente se muestra la correspondencia entre los parámetros de los tres métodos.</span><span class="sxs-lookup"><span data-stu-id="fb60a-142">The following table shows the correspondence between the parameters of the three methods.</span></span>



| <span data-ttu-id="fb60a-143">parámetro changeViewOnlineList</span><span class="sxs-lookup"><span data-stu-id="fb60a-143">changeViewOnlineList parameter</span></span> | <span data-ttu-id="fb60a-144">Parámetro GetListContents</span><span class="sxs-lookup"><span data-stu-id="fb60a-144">GetListContents parameter</span></span> | <span data-ttu-id="fb60a-145">Parámetro GetTemplate</span><span class="sxs-lookup"><span data-stu-id="fb60a-145">GetTemplate parameter</span></span> |
|--------------------------------|---------------------------|-----------------------|
| <span data-ttu-id="fb60a-146">*LocationType (*</span><span class="sxs-lookup"><span data-stu-id="fb60a-146">*LocationType*</span></span>                 | <span data-ttu-id="fb60a-147">*ubicación*</span><span class="sxs-lookup"><span data-stu-id="fb60a-147">*location*</span></span>                | <span data-ttu-id="fb60a-148">*ubicación*</span><span class="sxs-lookup"><span data-stu-id="fb60a-148">*location*</span></span>            |
| <span data-ttu-id="fb60a-149">*LocationID*</span><span class="sxs-lookup"><span data-stu-id="fb60a-149">*LocationID*</span></span>                   | <span data-ttu-id="fb60a-150">*pContext*</span><span class="sxs-lookup"><span data-stu-id="fb60a-150">*pContext*</span></span>                | <span data-ttu-id="fb60a-151">*pContext*</span><span class="sxs-lookup"><span data-stu-id="fb60a-151">*pContext*</span></span>            |
| <span data-ttu-id="fb60a-152">*Params*</span><span class="sxs-lookup"><span data-stu-id="fb60a-152">*Params*</span></span>                       | <span data-ttu-id="fb60a-153">*bstrParams*</span><span class="sxs-lookup"><span data-stu-id="fb60a-153">*bstrParams*</span></span>              | <span data-ttu-id="fb60a-154">*bstrViewParams*</span><span class="sxs-lookup"><span data-stu-id="fb60a-154">*bstrViewParams*</span></span>      |
| <span data-ttu-id="fb60a-155">*ListType*</span><span class="sxs-lookup"><span data-stu-id="fb60a-155">*ListType*</span></span>                     | <span data-ttu-id="fb60a-156">*bstrListType*</span><span class="sxs-lookup"><span data-stu-id="fb60a-156">*bstrListType*</span></span>            | <span data-ttu-id="fb60a-157">no aplicable</span><span class="sxs-lookup"><span data-stu-id="fb60a-157">not applicable</span></span>        |



 

<span data-ttu-id="fb60a-158">Dado que los tres métodos que se muestran en la tabla anterior se implementan en la tienda en línea, tiene cierta flexibilidad en la forma de usar los parámetros.</span><span class="sxs-lookup"><span data-stu-id="fb60a-158">Because all three of the methods shown in the preceding table are implemented by the online store, you have some flexibility in how you use the parameters.</span></span> <span data-ttu-id="fb60a-159">La idea es que proporcione información suficiente para **GetListContents** con el fin de determinar qué lista debe recuperar y **GetTemplate** para determinar qué página de detección debe mostrarse a continuación.</span><span class="sxs-lookup"><span data-stu-id="fb60a-159">The idea is that you provide enough information for **GetListContents** to determine which list it should retrieve and for **GetTemplate** to determine which discovery page should be displayed next.</span></span> <span data-ttu-id="fb60a-160">En los siguientes ejemplos se muestran dos posibilidades.</span><span class="sxs-lookup"><span data-stu-id="fb60a-160">The following examples illustrate two possibilities.</span></span>

<span data-ttu-id="fb60a-161">**Ejemplo 1: una lista dinámica que está en el catálogo de la tienda en línea**</span><span class="sxs-lookup"><span data-stu-id="fb60a-161">**Example 1: A dynamic list that is in the online store's catalog**</span></span>

<span data-ttu-id="fb60a-162">Supongamos que desea que el complemento obtenga el contenido de la lista dinámica que tiene un identificador de 6 en el catálogo de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="fb60a-162">Suppose you want the plug-in to get the contents of the dynamic list that has an ID of 6 in the online store's catalog.</span></span> <span data-ttu-id="fb60a-163">Supongamos que la lista 6 es una lista de pistas.</span><span class="sxs-lookup"><span data-stu-id="fb60a-163">Assume that list 6 is a list of tracks.</span></span> <span data-ttu-id="fb60a-164">Puede proporcionar suficiente información al complemento realizando la siguiente llamada.</span><span class="sxs-lookup"><span data-stu-id="fb60a-164">You could provide the plug-in with enough information by making the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="fb60a-165">Tenga en cuenta que el parámetro *params* está vacío; el complemento tiene suficiente información en los otros parámetros.</span><span class="sxs-lookup"><span data-stu-id="fb60a-165">Note that the *Params* parameter is empty; the plug-in has enough information in the other parameters.</span></span>

<span data-ttu-id="fb60a-166">**Ejemplo 2: lista dinámica que no está en el catálogo de la tienda en línea**</span><span class="sxs-lookup"><span data-stu-id="fb60a-166">**Example 2: A dynamic list that is not in the online store's catalog**</span></span>

<span data-ttu-id="fb60a-167">Supongamos que desea que el complemento obtenga el contenido de una lista dinámica que no está en el catálogo de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="fb60a-167">Suppose that you want the plug-in to get the contents of a dynamic list that is not in the online store's catalog.</span></span> <span data-ttu-id="fb60a-168">Es posible que haya decidido tener una lista dinámica que incluye canciones recogidas por un intérprete determinado.</span><span class="sxs-lookup"><span data-stu-id="fb60a-168">Perhaps you have decided to have a dynamic list that includes songs picked by a particular artist.</span></span> <span data-ttu-id="fb60a-169">Supongamos que el artista tiene un identificador de 2 en el catálogo de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="fb60a-169">Assume the artist has an ID of 2 in the online store's catalog.</span></span> <span data-ttu-id="fb60a-170">Podría hacer la siguiente llamada.</span><span class="sxs-lookup"><span data-stu-id="fb60a-170">You could make the following call.</span></span>


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



<span data-ttu-id="fb60a-171">Tenga en cuenta que los parámetros *LocationType (* y *LocationID* no especifican la lista.</span><span class="sxs-lookup"><span data-stu-id="fb60a-171">Note that the *LocationType* and *LocationID* parameters do not specify the list.</span></span> <span data-ttu-id="fb60a-172">En su lugar, el parámetro *params* especifica la lista.</span><span class="sxs-lookup"><span data-stu-id="fb60a-172">Instead, the *Params* parameter specifies the list.</span></span> <span data-ttu-id="fb60a-173">Los parámetros *LocationType (* y *LocationID* se pasan a **IWMPContentPartner:: GetListContents**, pero en este caso, **GetListContents** pueden omitirlos.</span><span class="sxs-lookup"><span data-stu-id="fb60a-173">The *LocationType* and *LocationID* parameters are passed to **IWMPContentPartner::GetListContents**, but in this case, **GetListContents** can ignore them.</span></span> <span data-ttu-id="fb60a-174">Los parámetros *LocationType (* y *LocationID* también se pasan a **IWMPContentPartner:: GetTemplate**, que puede usarlos para determinar qué página de detección debe mostrarse con la lista dinámica.</span><span class="sxs-lookup"><span data-stu-id="fb60a-174">The *LocationType* and *LocationID* parameters are also passed to **IWMPContentPartner::GetTemplate**, which can use them to determine which discovery page should be displayed with the dynamic list.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb60a-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb60a-175">Requirements</span></span>



| <span data-ttu-id="fb60a-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb60a-176">Requirement</span></span> | <span data-ttu-id="fb60a-177">Value</span><span class="sxs-lookup"><span data-stu-id="fb60a-177">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb60a-178">Versión</span><span class="sxs-lookup"><span data-stu-id="fb60a-178">Version</span></span><br/> | <span data-ttu-id="fb60a-179">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="fb60a-179">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="fb60a-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb60a-180">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb60a-181"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb60a-181"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb60a-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb60a-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb60a-183">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="fb60a-183">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="fb60a-184">**IWMPContentPartner::GetListContents**</span><span class="sxs-lookup"><span data-stu-id="fb60a-184">**IWMPContentPartner::GetListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[<span data-ttu-id="fb60a-185">**IWMPContentPartnerCallback::AddListContents**</span><span class="sxs-lookup"><span data-stu-id="fb60a-185">**IWMPContentPartnerCallback::AddListContents**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[<span data-ttu-id="fb60a-186">**IWMPContentPartner::GetTemplate**</span><span class="sxs-lookup"><span data-stu-id="fb60a-186">**IWMPContentPartner::GetTemplate**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[<span data-ttu-id="fb60a-187">**Ubicación y elemento seleccionado**</span><span class="sxs-lookup"><span data-stu-id="fb60a-187">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





