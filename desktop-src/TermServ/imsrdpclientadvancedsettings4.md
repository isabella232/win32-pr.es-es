---
title: Interfaz IMsRdpClientAdvancedSettings4
description: Administra la configuración de cliente avanzada. Deriva de la interfaz IMsRdpClientAdvancedSettings3.
ms.assetid: cb1785d6-1f94-4423-bdda-0e3e4e9b8641
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d840206a139e3c3272551eab6a187a7b18416e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422278"
---
# <a name="imsrdpclientadvancedsettings4-interface"></a><span data-ttu-id="5bcdf-106">Interfaz IMsRdpClientAdvancedSettings4</span><span class="sxs-lookup"><span data-stu-id="5bcdf-106">IMsRdpClientAdvancedSettings4 interface</span></span>

<span data-ttu-id="5bcdf-107">Administra la configuración de cliente avanzada.</span><span class="sxs-lookup"><span data-stu-id="5bcdf-107">Manages advanced client settings.</span></span> <span data-ttu-id="5bcdf-108">Deriva de la interfaz [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="5bcdf-108">Derives from the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="5bcdf-109">Esta interfaz incluye métodos para recuperar y establecer propiedades avanzadas (opcionales) para el control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5bcdf-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="5bcdf-110">Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="5bcdf-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="5bcdf-111">A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **IID \_ IMsRdpClientAdvancedSettings4** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="5bcdf-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings4** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="5bcdf-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="5bcdf-112">Members</span></span>

<span data-ttu-id="5bcdf-113">La interfaz **IMsRdpClientAdvancedSettings4** hereda de [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span><span class="sxs-lookup"><span data-stu-id="5bcdf-113">The **IMsRdpClientAdvancedSettings4** interface inherits from [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span></span> <span data-ttu-id="5bcdf-114">**IMsRdpClientAdvancedSettings4** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5bcdf-114">**IMsRdpClientAdvancedSettings4** also has these types of members:</span></span>

-   [<span data-ttu-id="5bcdf-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5bcdf-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5bcdf-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5bcdf-116">Properties</span></span>

<span data-ttu-id="5bcdf-117">La interfaz **IMsRdpClientAdvancedSettings4** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5bcdf-117">The **IMsRdpClientAdvancedSettings4** interface has these properties.</span></span>



| <span data-ttu-id="5bcdf-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5bcdf-118">Property</span></span>                                                                                    | <span data-ttu-id="5bcdf-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="5bcdf-119">Access type</span></span>           | <span data-ttu-id="5bcdf-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bcdf-120">Description</span></span>                                                              |
|:--------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="5bcdf-121">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="5bcdf-121">**AuthenticationLevel**</span></span>](imsrdpclientadvancedsettings4-authenticationlevel.md)<br/> | <span data-ttu-id="5bcdf-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5bcdf-122">Read/write</span></span><br/> | <span data-ttu-id="5bcdf-123">Especifica el nivel de autenticación que se va a utilizar para la conexión.</span><span class="sxs-lookup"><span data-stu-id="5bcdf-123">Specifies the authentication level to use for the connection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5bcdf-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bcdf-124">Remarks</span></span>

<span data-ttu-id="5bcdf-125">Esta interfaz se ha extendido mediante las siguientes interfaces, con cada nueva interfaz que hereda todos los métodos y propiedades de las interfaces anteriores:</span><span class="sxs-lookup"><span data-stu-id="5bcdf-125">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="5bcdf-126">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="5bcdf-126">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="5bcdf-127">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="5bcdf-127">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="5bcdf-128">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5bcdf-128">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="5bcdf-129">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5bcdf-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5bcdf-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bcdf-130">Requirements</span></span>



| <span data-ttu-id="5bcdf-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bcdf-131">Requirement</span></span> | <span data-ttu-id="5bcdf-132">Value</span><span class="sxs-lookup"><span data-stu-id="5bcdf-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bcdf-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bcdf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5bcdf-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5bcdf-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="5bcdf-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bcdf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5bcdf-136">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="5bcdf-136">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="5bcdf-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5bcdf-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="5bcdf-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bcdf-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5bcdf-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5bcdf-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bcdf-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bcdf-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5bcdf-141">IID</span><span class="sxs-lookup"><span data-stu-id="5bcdf-141">IID</span></span><br/>                      | <span data-ttu-id="5bcdf-142">IID \_ IMsRdpClientAdvancedSettings4 se define como FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="5bcdf-142">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5bcdf-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bcdf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bcdf-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="5bcdf-144">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="5bcdf-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="5bcdf-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="5bcdf-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="5bcdf-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5bcdf-147">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="5bcdf-147">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5bcdf-148">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="5bcdf-148">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

