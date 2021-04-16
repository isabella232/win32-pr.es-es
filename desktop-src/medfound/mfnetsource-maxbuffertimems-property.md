---
description: Cantidad máxima de datos que los búferes de origen de la red, en milisegundos.
ms.assetid: bd776dc2-341a-4d87-8a06-8063daf53ede
title: Propiedad MFNETSOURCE_MAXBUFFERTIMEMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f98cd17f33bb893dacd02b2a00669f3d2355e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696598"
---
# <a name="mfnetsource_maxbuffertimems-property"></a><span data-ttu-id="3a550-103">\_Propiedad MAXBUFFERTIMEMS de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="3a550-103">MFNETSOURCE\_MAXBUFFERTIMEMS property</span></span>

<span data-ttu-id="3a550-104">Cantidad máxima de datos que los búferes de origen de la red, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="3a550-104">Maximum amount of data the network source buffers, in milliseconds.</span></span>



<span data-ttu-id="3a550-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3a550-105">Data type</span></span>

<span data-ttu-id="3a550-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="3a550-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="3a550-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="3a550-107">PROPVARIANT member</span></span>

<span data-ttu-id="3a550-108">**DWORD** (almacenado como **Long**)</span><span class="sxs-lookup"><span data-stu-id="3a550-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="3a550-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3a550-109">VT\_I4</span></span>

<span data-ttu-id="3a550-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="3a550-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="3a550-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a550-111">Remarks</span></span>

<span data-ttu-id="3a550-112">La constante **MFNETSOURCE \_ MAXBUFFERTIMEMS** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="3a550-112">The constant **MFNETSOURCE\_MAXBUFFERTIMEMS** defines the GUID for this property key.</span></span> <span data-ttu-id="3a550-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="3a550-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="3a550-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="3a550-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="3a550-115">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="3a550-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="3a550-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="3a550-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="3a550-117">El valor predeterminado de esta propiedad es 40.000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="3a550-117">The default value of this property is 40,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a550-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a550-118">Requirements</span></span>



| <span data-ttu-id="3a550-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a550-119">Requirement</span></span> | <span data-ttu-id="3a550-120">Value</span><span class="sxs-lookup"><span data-stu-id="3a550-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a550-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a550-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a550-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3a550-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a550-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a550-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a550-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a550-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a550-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a550-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a550-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a550-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a550-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a550-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a550-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a550-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="3a550-129">Características de origen de red</span><span class="sxs-lookup"><span data-stu-id="3a550-129">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="3a550-130">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a550-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




