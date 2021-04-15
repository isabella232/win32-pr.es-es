---
description: El valor del campo &\# 0034; c-hostexever&\# 0034; que usa el origen de red para el registro.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: Propiedad MFNETSOURCE_HOSTVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f10c1a66bc2ab52455140733a6b60f25863c8f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497656"
---
# <a name="mfnetsource_hostversion-property"></a><span data-ttu-id="6997a-103">\_Propiedad HOSTVERSION de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="6997a-103">MFNETSOURCE\_HOSTVERSION property</span></span>

<span data-ttu-id="6997a-104">El valor del campo "c-hostexever" que usa el origen de red para el registro.</span><span class="sxs-lookup"><span data-stu-id="6997a-104">The value of the "c-hostexever" field that the network source uses for logging.</span></span> <span data-ttu-id="6997a-105">Las aplicaciones pueden establecer esta propiedad en el número de versión de la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="6997a-105">Applications can set this property to the version number of the host application.</span></span> <span data-ttu-id="6997a-106">La aplicación host es el archivo. exe que se identifica mediante el campo c-hostexe.</span><span class="sxs-lookup"><span data-stu-id="6997a-106">The host application is the .exe file identified by the c-hostexe field.</span></span>



<span data-ttu-id="6997a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6997a-107">Data type</span></span>

<span data-ttu-id="6997a-108">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="6997a-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6997a-109">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="6997a-109">PROPVARIANT member</span></span>

<span data-ttu-id="6997a-110">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="6997a-110">**LONGLONG**</span></span>

<span data-ttu-id="6997a-111">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="6997a-111">VT\_I8</span></span>

<span data-ttu-id="6997a-112">**hVal**</span><span class="sxs-lookup"><span data-stu-id="6997a-112">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="6997a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6997a-113">Remarks</span></span>

<span data-ttu-id="6997a-114">La constante **MFNETSOURCE \_ HOSTVERSION** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6997a-114">The constant **MFNETSOURCE\_HOSTVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="6997a-115">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="6997a-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="6997a-116">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="6997a-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="6997a-117">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="6997a-117">To set the property, pass an **IPropertyStore** pointer to the Source resolver.</span></span> <span data-ttu-id="6997a-118">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="6997a-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6997a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6997a-119">Requirements</span></span>



| <span data-ttu-id="6997a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6997a-120">Requirement</span></span> | <span data-ttu-id="6997a-121">Value</span><span class="sxs-lookup"><span data-stu-id="6997a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6997a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6997a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6997a-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6997a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6997a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6997a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6997a-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6997a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6997a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6997a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6997a-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6997a-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6997a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6997a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6997a-129">Registro de cliente</span><span class="sxs-lookup"><span data-stu-id="6997a-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="6997a-130">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6997a-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6997a-131">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6997a-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




