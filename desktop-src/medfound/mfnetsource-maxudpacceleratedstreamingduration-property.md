---
description: Duración máxima de la transmisión por secuencias acelerada, en milisegundos, en que el origen de red utiliza el transporte UDP.
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: Propiedad MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083327"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a><span data-ttu-id="d3e0c-103">\_Propiedad MAXUDPACCELERATEDSTREAMINGDURATION de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="d3e0c-103">MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="d3e0c-104">Duración máxima de la transmisión por secuencias acelerada, en milisegundos, en que el origen de red utiliza el transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-104">Maximum duration of accelerated streaming, in milliseconds, when the network source uses UDP transport.</span></span>



<span data-ttu-id="d3e0c-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d3e0c-105">Data type</span></span>

<span data-ttu-id="d3e0c-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="d3e0c-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d3e0c-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="d3e0c-107">PROPVARIANT member</span></span>

<span data-ttu-id="d3e0c-108">**DWORD** (almacenado como **Long**)</span><span class="sxs-lookup"><span data-stu-id="d3e0c-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="d3e0c-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d3e0c-109">VT\_I4</span></span>

<span data-ttu-id="d3e0c-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="d3e0c-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="d3e0c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3e0c-111">Remarks</span></span>

<span data-ttu-id="d3e0c-112">La constante **MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-112">The constant **MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="d3e0c-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="d3e0c-114">En el transporte UDP, esta propiedad invalida la propiedad [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) si el valor de esta propiedad es inferior.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-114">For UDP transport, this property overrides the [**MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) property if the value of this property is lower.</span></span>

<span data-ttu-id="d3e0c-115">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="d3e0c-116">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="d3e0c-117">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="d3e0c-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="d3e0c-118">El valor predeterminado de esta propiedad es 8.000 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="d3e0c-118">The default value of this property is 8,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e0c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3e0c-119">Requirements</span></span>



| <span data-ttu-id="d3e0c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3e0c-120">Requirement</span></span> | <span data-ttu-id="d3e0c-121">Value</span><span class="sxs-lookup"><span data-stu-id="d3e0c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e0c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3e0c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e0c-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d3e0c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d3e0c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3e0c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e0c-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3e0c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d3e0c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3e0c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e0c-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e0c-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3e0c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3e0c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e0c-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3e0c-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d3e0c-130">Características de origen de red</span><span class="sxs-lookup"><span data-stu-id="d3e0c-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="d3e0c-131">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3e0c-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




