---
description: Habilita el modo de descarga privada en el origen de red.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: Propiedad MFNETSOURCE_ENABLE_PRIVATEMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53aa0bde3bf76ded278e0e3ee37465adb717972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715363"
---
# <a name="mfnetsource_enable_privatemode-property"></a><span data-ttu-id="0868d-103">MFNETSOURCE \_ habilitar \_ propiedad PRIVATEMODE</span><span class="sxs-lookup"><span data-stu-id="0868d-103">MFNETSOURCE\_ENABLE\_PRIVATEMODE property</span></span>

<span data-ttu-id="0868d-104">Habilita el modo de descarga privada en el origen de red.</span><span class="sxs-lookup"><span data-stu-id="0868d-104">Enables private download mode in the network source.</span></span>



<span data-ttu-id="0868d-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0868d-105">Data type</span></span>

<span data-ttu-id="0868d-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="0868d-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="0868d-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="0868d-107">PROPVARIANT member</span></span>

<span data-ttu-id="0868d-108">**BOOLEANO**</span><span class="sxs-lookup"><span data-stu-id="0868d-108">**BOOL**</span></span>

<span data-ttu-id="0868d-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="0868d-109">VT\_I4</span></span>

<span data-ttu-id="0868d-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="0868d-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="0868d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0868d-111">Remarks</span></span>

<span data-ttu-id="0868d-112">Si esta propiedad es **true**, la memoria caché se borra cuando finaliza la sesión.</span><span class="sxs-lookup"><span data-stu-id="0868d-112">If this property is **TRUE**, the cache is cleared when the session ends.</span></span>

<span data-ttu-id="0868d-113">La constante **MFNETSOURCE \_ CLIENTGUID** define el GUID de la clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="0868d-113">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="0868d-114">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="0868d-114">The property identifier (PID) is zero.</span></span> <span data-ttu-id="0868d-115">Para establecer esta propiedad en el origen de red, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="0868d-115">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="0868d-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="0868d-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0868d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0868d-117">Requirements</span></span>



| <span data-ttu-id="0868d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0868d-118">Requirement</span></span> | <span data-ttu-id="0868d-119">Value</span><span class="sxs-lookup"><span data-stu-id="0868d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0868d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0868d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0868d-121">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0868d-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0868d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0868d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0868d-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0868d-123">None supported</span></span><br/>                                                          |
| <span data-ttu-id="0868d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0868d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0868d-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0868d-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0868d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0868d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0868d-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0868d-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0868d-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0868d-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




