---
description: El valor del campo &\# 0034; c-playerversion&\# 0034; que usa el origen de red para el registro.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: Propiedad MFNETSOURCE_PLAYERVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817915"
---
# <a name="mfnetsource_playerversion-property"></a><span data-ttu-id="62185-103">\_Propiedad PLAYERVERSION de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="62185-103">MFNETSOURCE\_PLAYERVERSION property</span></span>

<span data-ttu-id="62185-104">El valor del campo "c-playerversion" que usa el origen de red para el registro.</span><span class="sxs-lookup"><span data-stu-id="62185-104">The value of the "c-playerversion" field that the network source uses for logging.</span></span> <span data-ttu-id="62185-105">Las aplicaciones pueden establecer esta propiedad en el número de versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="62185-105">Applications can set this property to the version number of the application.</span></span>



<span data-ttu-id="62185-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="62185-106">Data type</span></span>

<span data-ttu-id="62185-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="62185-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="62185-108">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="62185-108">PROPVARIANT member</span></span>

<span data-ttu-id="62185-109">**LONGLONG**</span><span class="sxs-lookup"><span data-stu-id="62185-109">**LONGLONG**</span></span>

<span data-ttu-id="62185-110">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="62185-110">VT\_I8</span></span>

<span data-ttu-id="62185-111">**hVal**</span><span class="sxs-lookup"><span data-stu-id="62185-111">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="62185-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62185-112">Remarks</span></span>

<span data-ttu-id="62185-113">La constante **MFNETSOURCE \_ PLAYERVERSION** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="62185-113">The constant **MFNETSOURCE\_PLAYERVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="62185-114">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="62185-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="62185-115">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="62185-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="62185-116">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="62185-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="62185-117">Para obtener más información, consulte [solucionador de código fuente](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="62185-117">For more information, see [Source Resolver](source-resolver.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62185-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62185-118">Requirements</span></span>



| <span data-ttu-id="62185-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="62185-119">Requirement</span></span> | <span data-ttu-id="62185-120">Value</span><span class="sxs-lookup"><span data-stu-id="62185-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62185-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62185-121">Minimum supported client</span></span><br/> | <span data-ttu-id="62185-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="62185-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="62185-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62185-123">Minimum supported server</span></span><br/> | <span data-ttu-id="62185-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="62185-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="62185-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62185-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="62185-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62185-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62185-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="62185-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62185-128">Registro de cliente</span><span class="sxs-lookup"><span data-stu-id="62185-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="62185-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62185-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="62185-130">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62185-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




