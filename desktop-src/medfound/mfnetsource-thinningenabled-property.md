---
description: Especifica si la conmutación de secuencias está habilitada en el origen de red.
ms.assetid: 691a3549-eaf8-4e3d-ad0e-e5b013658f78
title: Propiedad MFNETSOURCE_THINNINGENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d5b1b362f8776e80e3d12b591dbf2116217846
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000861"
---
# <a name="mfnetsource_thinningenabled-property"></a><span data-ttu-id="22af7-103">\_Propiedad THINNINGENABLED de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="22af7-103">MFNETSOURCE\_THINNINGENABLED property</span></span>

<span data-ttu-id="22af7-104">Especifica si la conmutación de secuencias está habilitada en el origen de red.</span><span class="sxs-lookup"><span data-stu-id="22af7-104">Specifies whether stream switching is enabled on the network source.</span></span> <span data-ttu-id="22af7-105">La conmutación por secuencias permite que el servidor multimedia cambie las secuencias en un archivo de velocidad de bits múltiple (MBR), en función del ancho de banda disponible.</span><span class="sxs-lookup"><span data-stu-id="22af7-105">Stream switching enables the media server to change streams in a multiple bit-rate (MBR) file, based on available bandwidth.</span></span>



<span data-ttu-id="22af7-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="22af7-106">Data type</span></span>

<span data-ttu-id="22af7-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="22af7-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="22af7-108">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="22af7-108">PROPVARIANT member</span></span>

<span data-ttu-id="22af7-109">Booleano (**Long**)</span><span class="sxs-lookup"><span data-stu-id="22af7-109">Boolean (**LONG**)</span></span>

<span data-ttu-id="22af7-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="22af7-110">VT\_I4</span></span>

<span data-ttu-id="22af7-111">**lVal**</span><span class="sxs-lookup"><span data-stu-id="22af7-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="22af7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22af7-112">Remarks</span></span>

<span data-ttu-id="22af7-113">La constante **MFNETSOURCE \_ THINNINGENABLED** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="22af7-113">The constant **MFNETSOURCE\_THINNINGENABLED** defines the GUID for this property key.</span></span> <span data-ttu-id="22af7-114">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="22af7-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="22af7-115">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="22af7-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="22af7-116">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="22af7-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="22af7-117">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="22af7-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="22af7-118">El valor predeterminado de esta propiedad es **true**.</span><span class="sxs-lookup"><span data-stu-id="22af7-118">The default value of this property is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="22af7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22af7-119">Requirements</span></span>



| <span data-ttu-id="22af7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="22af7-120">Requirement</span></span> | <span data-ttu-id="22af7-121">Value</span><span class="sxs-lookup"><span data-stu-id="22af7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22af7-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22af7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="22af7-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="22af7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="22af7-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22af7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="22af7-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="22af7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="22af7-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22af7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="22af7-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22af7-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22af7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="22af7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22af7-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="22af7-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="22af7-130">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="22af7-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




