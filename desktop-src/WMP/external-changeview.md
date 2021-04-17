---
title: External. changeView (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método changeView cambia la vista en Windows Media Player.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- método changeView de Windows Media Player
- método changeView de Windows Media Player, clase externa
- Clase externa Windows Media Player, método changeView
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35adb253d5dd14d755353c29f9278b1c122133d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698601"
---
# <a name="externalchangeview-method"></a><span data-ttu-id="1e495-108">External. changeView (método)</span><span class="sxs-lookup"><span data-stu-id="1e495-108">External.changeView method</span></span>

> [!Note]  
> <span data-ttu-id="1e495-109">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="1e495-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="1e495-110">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="1e495-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="1e495-111">El método **changeView** cambia la vista en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1e495-111">The **changeView** method changes the view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e495-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e495-112">Syntax</span></span>


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a><span data-ttu-id="1e495-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e495-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e495-114">*LibraryLocationType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e495-114">*LibraryLocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e495-115">Una [constante de ubicación de biblioteca](library-location-constants.md) que especifica el tipo de la nueva vista.</span><span class="sxs-lookup"><span data-stu-id="1e495-115">A [library location constant](library-location-constants.md) that specifies the type of the new view.</span></span> <span data-ttu-id="1e495-116">Por ejemplo, la constante CPGenreID especifica que la nueva vista mostrará un género determinado.</span><span class="sxs-lookup"><span data-stu-id="1e495-116">For example, the constant CPGenreID specifies that the new view will show a particular genre.</span></span>

</dd> <dt>

<span data-ttu-id="1e495-117">*LibraryLocationID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e495-117">*LibraryLocationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e495-118">**Cadena** que contiene el identificador del elemento específico que se va a mostrar en la nueva vista.</span><span class="sxs-lookup"><span data-stu-id="1e495-118">**String** containing the ID of the specific item to show in the new view.</span></span> <span data-ttu-id="1e495-119">Por ejemplo, si *LibraryLocationType* es CPGenreID, este parámetro especifica el identificador del género que se va a mostrar en la nueva vista.</span><span class="sxs-lookup"><span data-stu-id="1e495-119">For example, if *LibraryLocationType* is CPGenreID, then this parameter specifies the ID of the genre to show in the new view.</span></span> <span data-ttu-id="1e495-120">Esta cadena puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="1e495-120">This string can be empty.</span></span> <span data-ttu-id="1e495-121">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="1e495-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1e495-122">*Filtro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1e495-122">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e495-123">**Cadena** que contiene el filtro para la nueva vista.</span><span class="sxs-lookup"><span data-stu-id="1e495-123">**String** containing the filter for the new view.</span></span> <span data-ttu-id="1e495-124">La vista se filtrará como si el usuario hubiera escrito este texto en el control de rueda de palabras del reproductor.</span><span class="sxs-lookup"><span data-stu-id="1e495-124">The view will be filtered as if the user had entered this text in the Player's word wheel control.</span></span> <span data-ttu-id="1e495-125">Esta cadena puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="1e495-125">This string can be empty.</span></span>

</dd> <dt>

<span data-ttu-id="1e495-126">*ViewParams* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e495-126">*ViewParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e495-127">**Cadena** que contiene los parámetros que Windows Media Player pone a disposición de la nueva página de detección que se muestra con la nueva vista.</span><span class="sxs-lookup"><span data-stu-id="1e495-127">**String** containing parameters that Windows Media Player makes available to the new discovery page that is displayed with the new view.</span></span> <span data-ttu-id="1e495-128">Estos parámetros no son interpretados por Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="1e495-128">These parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="1e495-129">Los crea la tienda en línea y solo tienen significado en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="1e495-129">They are created by the online store and have meaning only to the online store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e495-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e495-130">Return value</span></span>

<span data-ttu-id="1e495-131">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1e495-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e495-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e495-132">Remarks</span></span>

<span data-ttu-id="1e495-133">En algunos casos, tiene sentido establecer el parámetro *LibraryLocationID* en la cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="1e495-133">In some cases, it makes sense to set the *LibraryLocationID* parameter to the empty string.</span></span> <span data-ttu-id="1e495-134">Por ejemplo, si establece el parámetro *LibraryLocationType* en AllCPAlbumIDs, la nueva vista representará todos los álbumes.</span><span class="sxs-lookup"><span data-stu-id="1e495-134">For example, if you set the *LibraryLocationType* parameter to AllCPAlbumIDs, the new view will represent all albums.</span></span> <span data-ttu-id="1e495-135">Ningún álbum individual será el foco de la nueva vista, por lo que no es necesario proporcionar un identificador de álbum en el parámetro *LibraryLocationID* .</span><span class="sxs-lookup"><span data-stu-id="1e495-135">No individual album will be the focus of the new view, so there is no need to supply an album ID in the *LibraryLocationID* parameter.</span></span>

<span data-ttu-id="1e495-136">El parámetro *ViewParams* proporciona una manera de que una página de detección se comunique con otra página de detección.</span><span class="sxs-lookup"><span data-stu-id="1e495-136">The *ViewParams* parameter provides a way for a discovery page to communicate with another discovery page.</span></span> <span data-ttu-id="1e495-137">Cuando el script de una página de detección llama a **changeView**, Windows Media Player ajusta su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1e495-137">When script on a discovery page calls **changeView**, Windows Media Player adjusts its user interface.</span></span> <span data-ttu-id="1e495-138">Ese ajuste hace que el reproductor llame al método [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) del complemento para obtener la dirección URL de una nueva página de detección.</span><span class="sxs-lookup"><span data-stu-id="1e495-138">That adjustment causes the Player to call the plug-in's [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to get the URL of a new discovery page.</span></span> <span data-ttu-id="1e495-139">La cadena que la página de detección original pasa en el parámetro *ViewParams* no se pasa a **GetTemplate**.</span><span class="sxs-lookup"><span data-stu-id="1e495-139">The string that the original discovery page passes in the *ViewParams* parameter does not get passed to **GetTemplate**.</span></span> <span data-ttu-id="1e495-140">Sin embargo, la nueva página de detección puede recuperar la cadena *ViewParams* llamando a [external. viewParameters](external-viewparameters.md).</span><span class="sxs-lookup"><span data-stu-id="1e495-140">However, the new discovery page can retrieve the *ViewParams* string by calling [External.viewParameters](external-viewparameters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e495-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e495-141">Requirements</span></span>



| <span data-ttu-id="1e495-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e495-142">Requirement</span></span> | <span data-ttu-id="1e495-143">Value</span><span class="sxs-lookup"><span data-stu-id="1e495-143">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e495-144">Versión</span><span class="sxs-lookup"><span data-stu-id="1e495-144">Version</span></span><br/> | <span data-ttu-id="1e495-145">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="1e495-145">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="1e495-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e495-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="1e495-147"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e495-147"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e495-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e495-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e495-149">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="1e495-149">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="1e495-150">**External. changeViewOnlineList**</span><span class="sxs-lookup"><span data-stu-id="1e495-150">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="1e495-151">**External. libraryLocationID**</span><span class="sxs-lookup"><span data-stu-id="1e495-151">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="1e495-152">**External. libraryLocationType**</span><span class="sxs-lookup"><span data-stu-id="1e495-152">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="1e495-153">**External. viewParameters**</span><span class="sxs-lookup"><span data-stu-id="1e495-153">**External.viewParameters**</span></span>](external-viewparameters.md)
</dt> </dl>

 

 





