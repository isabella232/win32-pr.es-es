---
title: Métodos opcionales
description: Métodos opcionales
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149644"
---
# <a name="optional-methods"></a><span data-ttu-id="add5e-103">Métodos opcionales</span><span class="sxs-lookup"><span data-stu-id="add5e-103">Optional Methods</span></span>

<span data-ttu-id="add5e-104">Un componente OLE puede implementar una interfaz sin implementar toda la semántica de cada método en la interfaz, en lugar de devolver E \_ NOTIMPL o S \_ correctos según corresponda.</span><span class="sxs-lookup"><span data-stu-id="add5e-104">An OLE component can implement an interface without implementing all the semantics of every method in the interface, instead returning E\_NOTIMPL or S\_OK as appropriate.</span></span> <span data-ttu-id="add5e-105">En la tabla siguiente se describen los métodos que no es necesario que implemente un contenedor de controles ActiveX (es decir, el contenedor de control puede devolver E \_ NOTIMPL).</span><span class="sxs-lookup"><span data-stu-id="add5e-105">The following table describes those methods that an ActiveX control container is not required to implement (i.e. the control container can return E\_NOTIMPL).</span></span>

<span data-ttu-id="add5e-106">En la tabla siguiente se describen los métodos opcionales; Tenga en cuenta que el método todavía debe existir, pero simplemente puede devolver E \_ NOTIMPL en lugar de implementar semántica real.</span><span class="sxs-lookup"><span data-stu-id="add5e-106">The table below describes optional methods; note that the method must still exist, but can simply return E\_NOTIMPL instead of implementing real semantics.</span></span> <span data-ttu-id="add5e-107">Tenga en cuenta que los métodos de una interfaz obligatoria que no se enumeran a continuación deben considerarse obligatorios y no pueden devolver E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="add5e-107">Note that any method from a mandatory interface that is not listed below must be considered mandatory and may not return E\_NOTIMPL.</span></span>

## <a name="ioleclientsite"></a><span data-ttu-id="add5e-108">IOleClientSite</span><span class="sxs-lookup"><span data-stu-id="add5e-108">IOleClientSite</span></span>



| <span data-ttu-id="add5e-109">Método</span><span class="sxs-lookup"><span data-stu-id="add5e-109">Method</span></span>                                                     | <span data-ttu-id="add5e-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="add5e-110">Comments</span></span>                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="add5e-111">**SaveObject**</span><span class="sxs-lookup"><span data-stu-id="add5e-111">**SaveObject**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | <span data-ttu-id="add5e-112">Necesario para que la persistencia se admita correctamente.</span><span class="sxs-lookup"><span data-stu-id="add5e-112">Necessary for persistence to be successfully supported.</span></span><br/>                                       |
| [<span data-ttu-id="add5e-113">**GetMoniker**</span><span class="sxs-lookup"><span data-stu-id="add5e-113">**GetMoniker**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | <span data-ttu-id="add5e-114">Solo es necesario si el contenedor admite la vinculación a controles dentro de su propio formulario o documento.</span><span class="sxs-lookup"><span data-stu-id="add5e-114">Necessary only if the container supports linking to controls within its own form or document.</span></span><br/> |



 

## <a name="ioleinplacesite"></a><span data-ttu-id="add5e-115">IOleInPlaceSite</span><span class="sxs-lookup"><span data-stu-id="add5e-115">IOleInPlaceSite</span></span>



| <span data-ttu-id="add5e-116">Método</span><span class="sxs-lookup"><span data-stu-id="add5e-116">Method</span></span>                                                                     | <span data-ttu-id="add5e-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="add5e-117">Comments</span></span>                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="add5e-118">**ContextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="add5e-118">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | <span data-ttu-id="add5e-119">Opcionales</span><span class="sxs-lookup"><span data-stu-id="add5e-119">Optional</span></span><br/>                                      |
| [<span data-ttu-id="add5e-120">**Scroll**</span><span class="sxs-lookup"><span data-stu-id="add5e-120">**Scroll**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | <span data-ttu-id="add5e-121">Puede devolver S \_ false sin ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="add5e-121">May return S\_FALSE with no action.</span></span><br/>           |
| [<span data-ttu-id="add5e-122">**DiscardUndoState**</span><span class="sxs-lookup"><span data-stu-id="add5e-122">**DiscardUndoState**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | <span data-ttu-id="add5e-123">Puede devolver S \_ OK sin ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="add5e-123">Can return S\_OK with no action.</span></span><br/>              |
| [<span data-ttu-id="add5e-124">**DeactivateAndUndo**</span><span class="sxs-lookup"><span data-stu-id="add5e-124">**DeactivateAndUndo**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | <span data-ttu-id="add5e-125">La desactivación es obligatoria; Undo es opcional.</span><span class="sxs-lookup"><span data-stu-id="add5e-125">Deactivation is mandatory; Undo is optional.</span></span> <br/> |



 

## <a name="iolecontrolsite"></a><span data-ttu-id="add5e-126">IOleControlSite</span><span class="sxs-lookup"><span data-stu-id="add5e-126">IOleControlSite</span></span>



| <span data-ttu-id="add5e-127">Método</span><span class="sxs-lookup"><span data-stu-id="add5e-127">Method</span></span>                                                                          | <span data-ttu-id="add5e-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="add5e-128">Comments</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="add5e-129">**GetExtendedControl**</span><span class="sxs-lookup"><span data-stu-id="add5e-129">**GetExtendedControl**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | <span data-ttu-id="add5e-130">Necesario para los contenedores que admiten controles extendidos.</span><span class="sxs-lookup"><span data-stu-id="add5e-130">Necessary for containers that support extended controls.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="add5e-131">**ShowPropertyFrame**</span><span class="sxs-lookup"><span data-stu-id="add5e-131">**ShowPropertyFrame**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | <span data-ttu-id="add5e-132">Necesario para los contenedores que desean incluir sus propias páginas de propiedades para controlar las propiedades de control extendidas además de las proporcionadas por un control.</span><span class="sxs-lookup"><span data-stu-id="add5e-132">Necessary for containers that wish to include their own property pages to handle extended control properties in addition to those provided by a control.</span></span><br/> |
| [<span data-ttu-id="add5e-133">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="add5e-133">**TranslateAccelerator**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | <span data-ttu-id="add5e-134">Puede devolver S \_ false sin ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="add5e-134">May return S\_FALSE with no action.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="add5e-135">**LockInPlaceActive**</span><span class="sxs-lookup"><span data-stu-id="add5e-135">**LockInPlaceActive**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | <span data-ttu-id="add5e-136">Opcionales</span><span class="sxs-lookup"><span data-stu-id="add5e-136">Optional</span></span><br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a><span data-ttu-id="add5e-137">IDispatch (propiedades de ambiente)</span><span class="sxs-lookup"><span data-stu-id="add5e-137">IDispatch (Ambient properties)</span></span>



| <span data-ttu-id="add5e-138">Método</span><span class="sxs-lookup"><span data-stu-id="add5e-138">Method</span></span>                      | <span data-ttu-id="add5e-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="add5e-139">Comments</span></span>                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="add5e-140">GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="add5e-140">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="add5e-141">Necesario para los contenedores que admiten propiedades de ambiente no estándar.</span><span class="sxs-lookup"><span data-stu-id="add5e-141">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="add5e-142">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="add5e-142">GetTypeInfo</span></span><br/>      | <span data-ttu-id="add5e-143">Necesario para los contenedores que admiten propiedades de ambiente no estándar.</span><span class="sxs-lookup"><span data-stu-id="add5e-143">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="add5e-144">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="add5e-144">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="add5e-145">Necesario para los contenedores que admiten propiedades de ambiente no estándar.</span><span class="sxs-lookup"><span data-stu-id="add5e-145">Necessary for containers that support non-standard ambient properties.</span></span><br/> |



 

## <a name="idispatch-event-sink"></a><span data-ttu-id="add5e-146">IDispatch (receptor de eventos)</span><span class="sxs-lookup"><span data-stu-id="add5e-146">IDispatch (Event sink)</span></span>



| <span data-ttu-id="add5e-147">Método</span><span class="sxs-lookup"><span data-stu-id="add5e-147">Method</span></span>                      | <span data-ttu-id="add5e-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="add5e-148">Comments</span></span>                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="add5e-149">GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="add5e-149">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="add5e-150">El control conoce su propia información de tipo, por lo que no tiene necesidad de llamar a.</span><span class="sxs-lookup"><span data-stu-id="add5e-150">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="add5e-151">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="add5e-151">GetTypeInfo</span></span><br/>      | <span data-ttu-id="add5e-152">El control conoce su propia información de tipo, por lo que no tiene necesidad de llamar a.</span><span class="sxs-lookup"><span data-stu-id="add5e-152">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="add5e-153">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="add5e-153">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="add5e-154">El control conoce su propia información de tipo, por lo que no tiene necesidad de llamar a.</span><span class="sxs-lookup"><span data-stu-id="add5e-154">The control knows its own type information, so it has no need to call this.</span></span><br/> |



 

## <a name="ioleinplaceframe"></a><span data-ttu-id="add5e-155">IOleInPlaceFrame</span><span class="sxs-lookup"><span data-stu-id="add5e-155">IOleInPlaceFrame</span></span>



| <span data-ttu-id="add5e-156">Método</span><span class="sxs-lookup"><span data-stu-id="add5e-156">Method</span></span>                                                                           | <span data-ttu-id="add5e-157">Comentarios</span><span class="sxs-lookup"><span data-stu-id="add5e-157">Comments</span></span>                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="add5e-158">**ContextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="add5e-158">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [<span data-ttu-id="add5e-159">**GetBorder**</span><span class="sxs-lookup"><span data-stu-id="add5e-159">**GetBorder**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | <span data-ttu-id="add5e-160">Necesario para contenedores con la interfaz de usuario de la barra de herramientas (que es opcional)</span><span class="sxs-lookup"><span data-stu-id="add5e-160">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="add5e-161">**RequestBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="add5e-161">**RequestBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | <span data-ttu-id="add5e-162">Necesario para contenedores con la interfaz de usuario de la barra de herramientas (que es opcional)</span><span class="sxs-lookup"><span data-stu-id="add5e-162">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="add5e-163">**SetBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="add5e-163">**SetBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | <span data-ttu-id="add5e-164">Necesario para contenedores con la interfaz de usuario de la barra de herramientas (que es opcional)</span><span class="sxs-lookup"><span data-stu-id="add5e-164">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="add5e-165">**InsertMenus**</span><span class="sxs-lookup"><span data-stu-id="add5e-165">**InsertMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | <span data-ttu-id="add5e-166">Necesario para contenedores con la interfaz de usuario de menú (que es opcional)</span><span class="sxs-lookup"><span data-stu-id="add5e-166">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="add5e-167">**SetMenu**</span><span class="sxs-lookup"><span data-stu-id="add5e-167">**SetMenu**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | <span data-ttu-id="add5e-168">Necesario para contenedores con la interfaz de usuario de menú (que es opcional)</span><span class="sxs-lookup"><span data-stu-id="add5e-168">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="add5e-169">**RemoveMenus**</span><span class="sxs-lookup"><span data-stu-id="add5e-169">**RemoveMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | <span data-ttu-id="add5e-170">Necesario para contenedores con la interfaz de usuario de menú (que es opcional)</span><span class="sxs-lookup"><span data-stu-id="add5e-170">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="add5e-171">**SetStatusText**</span><span class="sxs-lookup"><span data-stu-id="add5e-171">**SetStatusText**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | <span data-ttu-id="add5e-172">Solo es necesario para los contenedores que tienen una línea de estado</span><span class="sxs-lookup"><span data-stu-id="add5e-172">Necessary only for containers that have a status line</span></span><br/>        |
| [<span data-ttu-id="add5e-173">**EnableModeless**</span><span class="sxs-lookup"><span data-stu-id="add5e-173">**EnableModeless**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | <span data-ttu-id="add5e-174">Opcionales</span><span class="sxs-lookup"><span data-stu-id="add5e-174">Optional</span></span><br/>                                                     |
| [<span data-ttu-id="add5e-175">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="add5e-175">**TranslateAccelerator**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | <span data-ttu-id="add5e-176">Opcionales</span><span class="sxs-lookup"><span data-stu-id="add5e-176">Optional</span></span><br/>                                                     |



 

## <a name="iolecontainer"></a><span data-ttu-id="add5e-177">IOleContainer</span><span class="sxs-lookup"><span data-stu-id="add5e-177">IOleContainer</span></span>



| <span data-ttu-id="add5e-178">Método</span><span class="sxs-lookup"><span data-stu-id="add5e-178">Method</span></span>                                                                    | <span data-ttu-id="add5e-179">Comentarios</span><span class="sxs-lookup"><span data-stu-id="add5e-179">Comments</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="add5e-180">**ParseDisplayName**</span><span class="sxs-lookup"><span data-stu-id="add5e-180">**ParseDisplayName**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | <span data-ttu-id="add5e-181">Solo si se admite la vinculación a controles u otras inserciones en el contenedor, ya que esto es necesario para el enlace de moniker.</span><span class="sxs-lookup"><span data-stu-id="add5e-181">Only if linking to controls or other embeddings in the container is supported, as this is necessary for moniker binding.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="add5e-182">**LockContainer**</span><span class="sxs-lookup"><span data-stu-id="add5e-182">**LockContainer**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | <span data-ttu-id="add5e-183">Como para ParseDisplayName</span><span class="sxs-lookup"><span data-stu-id="add5e-183">As for ParseDisplayName</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="add5e-184">**EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="add5e-184">**EnumObjects**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | <span data-ttu-id="add5e-185">Devuelve todos los controles ActiveX a través de un enumerador con [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), pero no necesariamente todos los objetos (porque no hay ninguna garantía de que todos los objetos sean controles ActiveX; algunos pueden ser controles normales de Windows).</span><span class="sxs-lookup"><span data-stu-id="add5e-185">Returns all ActiveX controls through an enumerator with [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), but not necessarily all objects (because there's no guarantee that all objects are ActiveX controls; some may be regular Windows controls).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="add5e-186">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="add5e-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="add5e-187">Contenedores</span><span class="sxs-lookup"><span data-stu-id="add5e-187">Containers</span></span>](containers.md)
</dt> </dl>

 

