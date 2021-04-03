---
description: Almacena una matriz de bytes que representa la licencia DRM asociada a la secuencia de bytes.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: Propiedad MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810994"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a><span data-ttu-id="0fd09-103">\_Propiedad de \_ representación de licencia de MFNETSOURCE DRMNET \_</span><span class="sxs-lookup"><span data-stu-id="0fd09-103">MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION property</span></span>

<span data-ttu-id="0fd09-104">Almacena una matriz de bytes que representa la licencia DRM asociada a la secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="0fd09-104">Stores an array of bytes that represents the DRM license associated with the byte stream.</span></span>



<span data-ttu-id="0fd09-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0fd09-105">Data type</span></span>

<span data-ttu-id="0fd09-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="0fd09-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="0fd09-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="0fd09-107">PROPVARIANT member</span></span>

<span data-ttu-id="0fd09-108">Matriz de bytes (**BLOB**)</span><span class="sxs-lookup"><span data-stu-id="0fd09-108">Byte array (**BLOB**)</span></span>

<span data-ttu-id="0fd09-109">BLOB de VT \_</span><span class="sxs-lookup"><span data-stu-id="0fd09-109">VT\_BLOB</span></span>

<span data-ttu-id="0fd09-110">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="0fd09-110">**blob**</span></span>



## <a name="remarks"></a><span data-ttu-id="0fd09-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fd09-111">Remarks</span></span>

<span data-ttu-id="0fd09-112">La **representación de \_ \_ licencia \_ Constant MFNETSOURCE DRMNET** define el GUID de esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="0fd09-112">The constant **MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION** defines the GUID for this property key.</span></span> <span data-ttu-id="0fd09-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="0fd09-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="0fd09-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0fd09-114">This property is read-only.</span></span> <span data-ttu-id="0fd09-115">Para obtener el valor de propiedad de la secuencia de bytes de red, llame a **IPropertyStore:: GetValue** y pase la estructura **PROPERTYKEY** en el parámetro *key* .</span><span class="sxs-lookup"><span data-stu-id="0fd09-115">To get the property value from the network byte stream, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="0fd09-116">El miembro **fmtid** de **PROPERTYKEY** debe establecerse en el GUID de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0fd09-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd09-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fd09-117">Requirements</span></span>



| <span data-ttu-id="0fd09-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fd09-118">Requirement</span></span> | <span data-ttu-id="0fd09-119">Value</span><span class="sxs-lookup"><span data-stu-id="0fd09-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd09-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fd09-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd09-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0fd09-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0fd09-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fd09-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd09-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0fd09-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0fd09-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fd09-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fd09-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd09-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fd09-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fd09-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd09-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0fd09-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0fd09-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0fd09-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




