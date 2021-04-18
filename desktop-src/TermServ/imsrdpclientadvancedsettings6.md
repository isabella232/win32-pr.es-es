---
title: Interfaz IMsRdpClientAdvancedSettings6
description: Expone propiedades que administran la configuración avanzada de controles ActiveX.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686033"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a><span data-ttu-id="53cbc-105">Interfaz IMsRdpClientAdvancedSettings6</span><span class="sxs-lookup"><span data-stu-id="53cbc-105">IMsRdpClientAdvancedSettings6 interface</span></span>

<span data-ttu-id="53cbc-106">Expone propiedades que administran la configuración avanzada de controles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="53cbc-106">Exposes properties that manage advanced ActiveX control settings.</span></span> <span data-ttu-id="53cbc-107">La interfaz **IMsRdpClientAdvancedSettings6** se deriva de la interfaz [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="53cbc-107">The **IMsRdpClientAdvancedSettings6** interface is derived from the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="53cbc-108">Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="53cbc-108">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="53cbc-109">A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **IID \_ IMsRdpClientAdvancedSettings6** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="53cbc-109">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings6** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="53cbc-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="53cbc-110">Members</span></span>

<span data-ttu-id="53cbc-111">La interfaz **IMsRdpClientAdvancedSettings6** hereda de [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span><span class="sxs-lookup"><span data-stu-id="53cbc-111">The **IMsRdpClientAdvancedSettings6** interface inherits from [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span></span> <span data-ttu-id="53cbc-112">**IMsRdpClientAdvancedSettings6** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="53cbc-112">**IMsRdpClientAdvancedSettings6** also has these types of members:</span></span>

-   [<span data-ttu-id="53cbc-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53cbc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53cbc-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53cbc-114">Properties</span></span>

<span data-ttu-id="53cbc-115">La interfaz **IMsRdpClientAdvancedSettings6** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="53cbc-115">The **IMsRdpClientAdvancedSettings6** interface has these properties.</span></span>



| <span data-ttu-id="53cbc-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53cbc-116">Property</span></span>                                                                                                  | <span data-ttu-id="53cbc-117">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="53cbc-117">Access type</span></span>           | <span data-ttu-id="53cbc-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="53cbc-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53cbc-119">**AuthenticationServiceClass**</span><span class="sxs-lookup"><span data-stu-id="53cbc-119">**AuthenticationServiceClass**</span></span>](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | <span data-ttu-id="53cbc-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53cbc-120">Read/write</span></span><br/> | <span data-ttu-id="53cbc-121">Especifica el nombre de entidad de seguridad de servicio (SPN) que se va a usar para la autenticación en el servidor.</span><span class="sxs-lookup"><span data-stu-id="53cbc-121">Specifies the service principal name (SPN) to use for authentication to the server.</span></span><br/>                                     |
| [<span data-ttu-id="53cbc-122">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="53cbc-122">**AuthenticationType**</span></span>](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | <span data-ttu-id="53cbc-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="53cbc-123">Read-only</span></span><br/>  | <span data-ttu-id="53cbc-124">Especifica el tipo de autenticación utilizado para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="53cbc-124">Specifies the type of authentication used for this connection.</span></span><br/>                                                          |
| [<span data-ttu-id="53cbc-125">**ConnectToAdministerServer**</span><span class="sxs-lookup"><span data-stu-id="53cbc-125">**ConnectToAdministerServer**</span></span>](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | <span data-ttu-id="53cbc-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53cbc-126">Read/write</span></span><br/> | <span data-ttu-id="53cbc-127">Recupera o especifica si el control ActiveX debe intentar conectarse al servidor con fines administrativos.</span><span class="sxs-lookup"><span data-stu-id="53cbc-127">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span><br/> |
| [<span data-ttu-id="53cbc-128">**EnableCredSspSupport**</span><span class="sxs-lookup"><span data-stu-id="53cbc-128">**EnableCredSspSupport**</span></span>](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | <span data-ttu-id="53cbc-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53cbc-129">Read/write</span></span><br/> | <span data-ttu-id="53cbc-130">Especifica si el proveedor de servicios de seguridad de credenciales (CredSSP) está habilitado para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="53cbc-130">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span><br/>                    |
| [<span data-ttu-id="53cbc-131">**HotKeyFocusReleaseLeft**</span><span class="sxs-lookup"><span data-stu-id="53cbc-131">**HotKeyFocusReleaseLeft**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | <span data-ttu-id="53cbc-132">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53cbc-132">Read/write</span></span><br/> | <span data-ttu-id="53cbc-133">Especifica el código de tecla virtual que se va a agregar a CTRL + ALT para determinar el reemplazo de la tecla de cambio de teclas para CTRL + ALT + Flecha izquierda.</span><span class="sxs-lookup"><span data-stu-id="53cbc-133">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+LEFT ARROW.</span></span><br/>          |
| [<span data-ttu-id="53cbc-134">**HotKeyFocusReleaseRight**</span><span class="sxs-lookup"><span data-stu-id="53cbc-134">**HotKeyFocusReleaseRight**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | <span data-ttu-id="53cbc-135">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53cbc-135">Read/write</span></span><br/> | <span data-ttu-id="53cbc-136">Especifica el código de tecla virtual que se va a agregar a CTRL + ALT para determinar el reemplazo de la tecla de cambio de teclas para CTRL + ALT + Flecha derecha.</span><span class="sxs-lookup"><span data-stu-id="53cbc-136">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+RIGHT ARROW.</span></span><br/>         |
| [<span data-ttu-id="53cbc-137">**IMPRESO**</span><span class="sxs-lookup"><span data-stu-id="53cbc-137">**PCB**</span></span>](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | <span data-ttu-id="53cbc-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53cbc-138">Read/write</span></span><br/> | <span data-ttu-id="53cbc-139">Especifica la configuración del BLOB de preconexión (PCB) que se va a usar antes de la conexión para la transmisión al servidor.</span><span class="sxs-lookup"><span data-stu-id="53cbc-139">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span><br/>               |
| [<span data-ttu-id="53cbc-140">**RelativeMouseMode**</span><span class="sxs-lookup"><span data-stu-id="53cbc-140">**RelativeMouseMode**</span></span>](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | <span data-ttu-id="53cbc-141">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53cbc-141">Read/write</span></span><br/> | <span data-ttu-id="53cbc-142">Especifica si el mouse debe usar el modo relativo.</span><span class="sxs-lookup"><span data-stu-id="53cbc-142">Specifies whether the mouse should use relative mode.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="53cbc-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53cbc-143">Remarks</span></span>

<span data-ttu-id="53cbc-144">La interfaz [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) ha extendido esta interfaz, heredando todos los métodos y propiedades de las interfaces anteriores.</span><span class="sxs-lookup"><span data-stu-id="53cbc-144">This interface has been extended by the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface, inheriting all the methods and properties of the previous interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="53cbc-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53cbc-145">Requirements</span></span>



| <span data-ttu-id="53cbc-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="53cbc-146">Requirement</span></span> | <span data-ttu-id="53cbc-147">Value</span><span class="sxs-lookup"><span data-stu-id="53cbc-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53cbc-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53cbc-148">Minimum supported client</span></span><br/> | <span data-ttu-id="53cbc-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53cbc-149">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="53cbc-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53cbc-150">Minimum supported server</span></span><br/> | <span data-ttu-id="53cbc-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53cbc-151">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="53cbc-152">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="53cbc-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="53cbc-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53cbc-153"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="53cbc-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53cbc-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53cbc-155"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53cbc-155"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="53cbc-156">IID</span><span class="sxs-lookup"><span data-stu-id="53cbc-156">IID</span></span><br/>                      | <span data-ttu-id="53cbc-157">IID \_ IMsRdpClientAdvancedSettings6 se define como 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="53cbc-157">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53cbc-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="53cbc-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53cbc-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="53cbc-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="53cbc-160">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="53cbc-160">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="53cbc-161">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="53cbc-161">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="53cbc-162">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="53cbc-162">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="53cbc-163">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="53cbc-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="53cbc-164">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="53cbc-164">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

