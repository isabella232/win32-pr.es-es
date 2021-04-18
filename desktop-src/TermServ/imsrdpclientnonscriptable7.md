---
title: Interfaz IMsRdpClientNonScriptable7
description: Proporciona acceso a las propiedades que no admiten scripts de la sesión remota de un cliente en el control ActiveX Escritorio remoto. Deriva de la interfaz IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable7, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8becf3bbf66ea18b2df87069ba38bab44c56db70
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "105720244"
---
# <a name="imsrdpclientnonscriptable7-interface"></a><span data-ttu-id="c2d23-106">Interfaz IMsRdpClientNonScriptable7</span><span class="sxs-lookup"><span data-stu-id="c2d23-106">IMsRdpClientNonScriptable7 interface</span></span>

<span data-ttu-id="c2d23-107">Proporciona acceso a las propiedades que no admiten scripts de la sesión remota de un cliente en el control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c2d23-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="c2d23-108">Deriva de la interfaz [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) .</span><span class="sxs-lookup"><span data-stu-id="c2d23-108">Derives from the [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) interface.</span></span> <span data-ttu-id="c2d23-109">Solo se puede tener acceso a los métodos de esta interfaz a través de vtable; no están disponibles para los clientes con scripts.</span><span class="sxs-lookup"><span data-stu-id="c2d23-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="c2d23-110">Una instancia de esta interfaz se obtiene llamando a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto [**IMsTscAx**](imstscax-interface.md) y pasando **IID \_ IMsRdpClientNonScriptable7**.</span><span class="sxs-lookup"><span data-stu-id="c2d23-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable7**.</span></span>

## <a name="members"></a><span data-ttu-id="c2d23-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2d23-111">Members</span></span>

<span data-ttu-id="c2d23-112">La interfaz **IMsRdpClientNonScriptable7** hereda de [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="c2d23-112">The **IMsRdpClientNonScriptable7** interface inherits from [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="c2d23-113">**IMsRdpClientNonScriptable7** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c2d23-113">**IMsRdpClientNonScriptable7** also has these types of members:</span></span>

- [<span data-ttu-id="c2d23-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2d23-114">Methods</span></span>](#methods)
- [<span data-ttu-id="c2d23-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2d23-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c2d23-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2d23-116">Methods</span></span>

<span data-ttu-id="c2d23-117">La interfaz **IMsRdpClientNonScriptable7** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c2d23-117">The **IMsRdpClientNonScriptable7** interface has these methods.</span></span>


| <span data-ttu-id="c2d23-118">Método</span><span class="sxs-lookup"><span data-stu-id="c2d23-118">Method</span></span>            | <span data-ttu-id="c2d23-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2d23-119">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="c2d23-120">**DisableDpiCursorScalingForProcess**</span><span class="sxs-lookup"><span data-stu-id="c2d23-120">**DisableDpiCursorScalingForProcess**</span></span>](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  <span data-ttu-id="c2d23-121">Deshabilita el escalado local del cursor del mouse recibido del servidor, asegurándose de que la forma del cursor se represente correctamente sin modificarla.</span><span class="sxs-lookup"><span data-stu-id="c2d23-121">Disables local scaling of the mouse cursor received from the server, ensuring that the cursor shape is rendered correctly without modification.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="c2d23-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2d23-122">Properties</span></span>

<span data-ttu-id="c2d23-123">La interfaz **IMsRdpClientNonScriptable7** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2d23-123">The **IMsRdpClientNonScriptable7** interface has these properties.</span></span>

| <span data-ttu-id="c2d23-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c2d23-124">Property</span></span>         | <span data-ttu-id="c2d23-125">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="c2d23-125">Access type</span></span>           | <span data-ttu-id="c2d23-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2d23-126">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="c2d23-127">**CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="c2d23-127">**CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | <span data-ttu-id="c2d23-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d23-128">Read-only</span></span> |  <span data-ttu-id="c2d23-129">Obtiene la colección de cámaras (y las configuraciones asociadas) que están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="c2d23-129">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>   |
| [<span data-ttu-id="c2d23-130">**Portapapeles**</span><span class="sxs-lookup"><span data-stu-id="c2d23-130">**Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)                       | <span data-ttu-id="c2d23-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c2d23-131">Read-only</span></span> |    <span data-ttu-id="c2d23-132">Obtiene el controlador del portapapeles que se usa para sincronizar los portapapeles locales y remotos si está habilitada la sincronización manual del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="c2d23-132">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="c2d23-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2d23-133">Requirements</span></span>

| <span data-ttu-id="c2d23-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2d23-134">Requirement</span></span> | <span data-ttu-id="c2d23-135">Value</span><span class="sxs-lookup"><span data-stu-id="c2d23-135">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="c2d23-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2d23-136">Minimum supported client</span></span>| <span data-ttu-id="c2d23-137">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="c2d23-137">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="c2d23-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c2d23-138">Type library</span></span>            | <span data-ttu-id="c2d23-139">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c2d23-139">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="c2d23-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2d23-140">DLL</span></span>                  | <span data-ttu-id="c2d23-141">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c2d23-141">MsTscAx.dll</span></span>     |
| <span data-ttu-id="c2d23-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="c2d23-142">CLSID</span></span>                    | <span data-ttu-id="c2d23-143">CLSID \_ MsRdpClient12 se define como 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="c2d23-143">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="c2d23-144">CLSID \_ MsRdpClient12NotSafeForScripting se define como 3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="c2d23-144">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="c2d23-145">CLSID \_ MsRdpClient11 se define como 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="c2d23-145">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="c2d23-146">CLSID \_ MsRdpClient11NotSafeForScripting se define como 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="c2d23-146">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="c2d23-147">IID</span><span class="sxs-lookup"><span data-stu-id="c2d23-147">IID</span></span>                      | <span data-ttu-id="c2d23-148">IID \_ IMsRdpClientNonScriptable7 se define como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="c2d23-148">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>            |

## <a name="see-also"></a><span data-ttu-id="c2d23-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2d23-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2d23-150">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="c2d23-150">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
