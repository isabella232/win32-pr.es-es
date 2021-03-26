---
description: Expone métodos que permiten a las páginas HTML que se hospedan en una extensión de asistente comunicarse con el asistente.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Objeto WebWizardHost (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 1fbaf53db11fda577e9e9c5384af5f7c62fe1944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001892"
---
# <a name="webwizardhost-object"></a><span data-ttu-id="0b9fb-103">Objeto WebWizardHost</span><span class="sxs-lookup"><span data-stu-id="0b9fb-103">WebWizardHost object</span></span>

<span data-ttu-id="0b9fb-104">Expone métodos que permiten a las páginas HTML que se hospedan en una extensión de asistente comunicarse con el asistente.</span><span class="sxs-lookup"><span data-stu-id="0b9fb-104">Exposes methods that enable HTML pages which are hosted in a wizard extension to communicate with the wizard.</span></span>

## <a name="members"></a><span data-ttu-id="0b9fb-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b9fb-105">Members</span></span>

<span data-ttu-id="0b9fb-106">El objeto **WebWizardHost** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0b9fb-106">The **WebWizardHost** object has these types of members:</span></span>

-   [<span data-ttu-id="0b9fb-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b9fb-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="0b9fb-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b9fb-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0b9fb-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0b9fb-109">Methods</span></span>

<span data-ttu-id="0b9fb-110">El objeto **WebWizardHost** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0b9fb-110">The **WebWizardHost** object has these methods.</span></span>



| <span data-ttu-id="0b9fb-111">Método</span><span class="sxs-lookup"><span data-stu-id="0b9fb-111">Method</span></span>                                                      | <span data-ttu-id="0b9fb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b9fb-112">Description</span></span>                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b9fb-113">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="0b9fb-113">**Cancel**</span></span>](iwebwizardhost-cancel.md)                     | <span data-ttu-id="0b9fb-114">Simula un clic del botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="0b9fb-114">Simulates a **Cancel** button click.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="0b9fb-115">**FinalBack**</span><span class="sxs-lookup"><span data-stu-id="0b9fb-115">**FinalBack**</span></span>](iwebwizardhost-finalback.md)               | <span data-ttu-id="0b9fb-116">Navega a la página del lado cliente inmediatamente anterior a la página que hospeda las páginas HTML del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="0b9fb-116">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span><br/>                                                                    |
| [<span data-ttu-id="0b9fb-117">**FinalNext**</span><span class="sxs-lookup"><span data-stu-id="0b9fb-117">**FinalNext**</span></span>](iwebwizardhost-finalnext.md)               | <span data-ttu-id="0b9fb-118">Navega a la página del asistente del lado cliente que sigue a la página que hospeda las páginas HTML del lado servidor o finaliza el asistente si no hay más páginas del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="0b9fb-118">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span><br/> |
| [<span data-ttu-id="0b9fb-119">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="0b9fb-119">**SetHeaderText**</span></span>](iwebwizardhost-setheadertext.md)       | <span data-ttu-id="0b9fb-120">Establece el título y el subtítulo que aparecen en el encabezado del asistente.</span><span class="sxs-lookup"><span data-stu-id="0b9fb-120">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="0b9fb-121">En general, el cliente mostrará el encabezado sobre el código HTML y debajo de la barra de título.</span><span class="sxs-lookup"><span data-stu-id="0b9fb-121">In general, the client will display the header above the HTML and below the title bar.</span></span><br/>                    |
| [<span data-ttu-id="0b9fb-122">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="0b9fb-122">**SetWizardButtons**</span></span>](iwebwizardhost-setwizardbuttons.md) | <span data-ttu-id="0b9fb-123">Actualiza los botones **atrás**, **siguiente** y **Finalizar** en el marco del asistente del cliente.</span><span class="sxs-lookup"><span data-stu-id="0b9fb-123">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="0b9fb-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b9fb-124">Properties</span></span>

<span data-ttu-id="0b9fb-125">El objeto **WebWizardHost** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0b9fb-125">The **WebWizardHost** object has these properties.</span></span>



| <span data-ttu-id="0b9fb-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b9fb-126">Property</span></span>                                               | <span data-ttu-id="0b9fb-127">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="0b9fb-127">Access type</span></span>           | <span data-ttu-id="0b9fb-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b9fb-128">Description</span></span>                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="0b9fb-129">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0b9fb-129">**Caption**</span></span>](iwebwizardhost-caption.md)<br/>   | <span data-ttu-id="0b9fb-130">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b9fb-130">Read/write</span></span><br/> | <span data-ttu-id="0b9fb-131">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="0b9fb-131">Not implemented.</span></span><br/>                              |
| [<span data-ttu-id="0b9fb-132">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="0b9fb-132">**Property**</span></span>](iwebwizardhost-property.md)<br/> | <span data-ttu-id="0b9fb-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b9fb-133">Read/write</span></span><br/> | <span data-ttu-id="0b9fb-134">Establece o recupera el valor actual de una propiedad.</span><span class="sxs-lookup"><span data-stu-id="0b9fb-134">Sets or retrieves a property's current value.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0b9fb-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b9fb-135">Requirements</span></span>



| <span data-ttu-id="0b9fb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b9fb-136">Requirement</span></span> | <span data-ttu-id="0b9fb-137">Value</span><span class="sxs-lookup"><span data-stu-id="0b9fb-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9fb-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b9fb-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0b9fb-139">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0b9fb-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0b9fb-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b9fb-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0b9fb-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b9fb-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0b9fb-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b9fb-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b9fb-143"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b9fb-143"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b9fb-144">IDL</span><span class="sxs-lookup"><span data-stu-id="0b9fb-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0b9fb-145"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0b9fb-145"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="0b9fb-146">IID</span><span class="sxs-lookup"><span data-stu-id="0b9fb-146">IID</span></span><br/>                      | <span data-ttu-id="0b9fb-147">CLSID \_ WebWizardHost</span><span class="sxs-lookup"><span data-stu-id="0b9fb-147">CLSID\_WebWizardHost</span></span><br/>                                                        |



 

 




