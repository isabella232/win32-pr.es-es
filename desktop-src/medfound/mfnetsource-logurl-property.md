---
description: Lista de direcciones URL a las que el origen de red enviará información de registro.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: Propiedad MFNETSOURCE_LOGURL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6956a7deb251ee9a25261a1b6c6a723973f7a03b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154628"
---
# <a name="mfnetsource_logurl-property"></a><span data-ttu-id="c0426-103">\_Propiedad LOGURL de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="c0426-103">MFNETSOURCE\_LOGURL property</span></span>

<span data-ttu-id="c0426-104">Lista de direcciones URL a las que el origen de red enviará información de registro.</span><span class="sxs-lookup"><span data-stu-id="c0426-104">List of URLs to which the network source will send logging information.</span></span>



<span data-ttu-id="c0426-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c0426-105">Data type</span></span>

<span data-ttu-id="c0426-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="c0426-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c0426-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="c0426-107">PROPVARIANT member</span></span>

<span data-ttu-id="c0426-108">Matriz de cadenas de caracteres anchos (**CALPWSTR**)</span><span class="sxs-lookup"><span data-stu-id="c0426-108">Array of wide-character strings (**CALPWSTR**)</span></span>

<span data-ttu-id="c0426-109">VT \_ Vector \| VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="c0426-109">VT\_VECTOR \| VT\_LPWSTR</span></span>

<span data-ttu-id="c0426-110">**calpwstr**</span><span class="sxs-lookup"><span data-stu-id="c0426-110">**calpwstr**</span></span>



## <a name="remarks"></a><span data-ttu-id="c0426-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0426-111">Remarks</span></span>

<span data-ttu-id="c0426-112">La constante **MFNETSOURCE \_ LOGURL** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="c0426-112">The constant **MFNETSOURCE\_LOGURL** defines the GUID for this property key.</span></span> <span data-ttu-id="c0426-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="c0426-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="c0426-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="c0426-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="c0426-115">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="c0426-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="c0426-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="c0426-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0426-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0426-117">Requirements</span></span>



| <span data-ttu-id="c0426-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0426-118">Requirement</span></span> | <span data-ttu-id="c0426-119">Value</span><span class="sxs-lookup"><span data-stu-id="c0426-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0426-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0426-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c0426-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c0426-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c0426-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0426-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c0426-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0426-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c0426-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0426-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0426-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0426-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0426-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0426-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0426-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0426-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c0426-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c0426-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




