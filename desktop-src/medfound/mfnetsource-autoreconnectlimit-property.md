---
description: El número de veces que el origen de red intenta volver a conectarse al servidor y reanudar el streaming si se pierde la conexión.
ms.assetid: 185e15c6-910b-4e27-9087-cfe30a174194
title: Propiedad MFNETSOURCE_AUTORECONNECTLIMIT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac2a81cb4d47d8113059924877670458ac22ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811000"
---
# <a name="mfnetsource_autoreconnectlimit-property"></a><span data-ttu-id="e941e-103">\_Propiedad AUTORECONNECTLIMIT de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="e941e-103">MFNETSOURCE\_AUTORECONNECTLIMIT property</span></span>

<span data-ttu-id="e941e-104">El número de veces que el origen de red intenta volver a conectarse al servidor y reanudar el streaming si se pierde la conexión.</span><span class="sxs-lookup"><span data-stu-id="e941e-104">The number of times the network source tries to reconnect to the server and resume streaming if the connection is lost.</span></span>



<span data-ttu-id="e941e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e941e-105">Data type</span></span>

<span data-ttu-id="e941e-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e941e-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e941e-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e941e-107">PROPVARIANT member</span></span>

<span data-ttu-id="e941e-108">**DWORD** (almacenado como **Long**)</span><span class="sxs-lookup"><span data-stu-id="e941e-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="e941e-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e941e-109">VT\_I4</span></span>

<span data-ttu-id="e941e-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="e941e-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="e941e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e941e-111">Remarks</span></span>

<span data-ttu-id="e941e-112">La constante **MFNETSOURCE \_ AUTORECONNECTLIMIT** define el GUID para esta clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e941e-112">The constant **MFNETSOURCE\_AUTORECONNECTLIMIT** defines the GUID for this property key.</span></span> <span data-ttu-id="e941e-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="e941e-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="e941e-114">Las aplicaciones pueden utilizar esta propiedad para configurar el origen de red.</span><span class="sxs-lookup"><span data-stu-id="e941e-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="e941e-115">Para establecer la propiedad, pase un objeto **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="e941e-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="e941e-116">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e941e-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e941e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e941e-117">Requirements</span></span>



| <span data-ttu-id="e941e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e941e-118">Requirement</span></span> | <span data-ttu-id="e941e-119">Value</span><span class="sxs-lookup"><span data-stu-id="e941e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e941e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e941e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e941e-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e941e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e941e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e941e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e941e-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e941e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e941e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e941e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e941e-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e941e-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e941e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e941e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e941e-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e941e-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e941e-128">Características de origen de red</span><span class="sxs-lookup"><span data-stu-id="e941e-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="e941e-129">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e941e-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




