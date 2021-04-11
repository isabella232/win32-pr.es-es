---
description: Identificador único por el que el servidor identifica el cliente.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: Propiedad MFNETSOURCE_CLIENTGUID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154964"
---
# <a name="mfnetsource_clientguid-property"></a><span data-ttu-id="9c2be-103">\_Propiedad CLIENTGUID de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="9c2be-103">MFNETSOURCE\_CLIENTGUID property</span></span>

<span data-ttu-id="9c2be-104">Identificador único por el que el servidor identifica el cliente.</span><span class="sxs-lookup"><span data-stu-id="9c2be-104">Unique identifier by which the server identifies the client.</span></span>



<span data-ttu-id="9c2be-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9c2be-105">Data type</span></span>

<span data-ttu-id="9c2be-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="9c2be-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="9c2be-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="9c2be-107">PROPVARIANT member</span></span>

<span data-ttu-id="9c2be-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="9c2be-108">**GUID**</span></span>

<span data-ttu-id="9c2be-109">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="9c2be-109">VT\_CLSID</span></span>

<span data-ttu-id="9c2be-110">**puuid**</span><span class="sxs-lookup"><span data-stu-id="9c2be-110">**puuid**</span></span>



## <a name="remarks"></a><span data-ttu-id="9c2be-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c2be-111">Remarks</span></span>

<span data-ttu-id="9c2be-112">La constante **MFNETSOURCE \_ CLIENTGUID** define el GUID de la clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9c2be-112">The **MFNETSOURCE\_CLIENTGUID** constant defines the GUID for the property key.</span></span> <span data-ttu-id="9c2be-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="9c2be-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="9c2be-114">Para establecer esta propiedad en el origen de red, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="9c2be-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="9c2be-115">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="9c2be-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="9c2be-116">Si no se establece o se establece como **GUID \_ NULL**, Microsoft Media Foundation genera un GUID anónimo por sesión que garantiza la privacidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="9c2be-116">If not set or set as **GUID\_NULL**, Microsoft Media Foundation generates an anonymous GUID per session that ensures the user's privacy.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c2be-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c2be-117">Requirements</span></span>



| <span data-ttu-id="9c2be-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c2be-118">Requirement</span></span> | <span data-ttu-id="9c2be-119">Value</span><span class="sxs-lookup"><span data-stu-id="9c2be-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c2be-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c2be-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9c2be-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c2be-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9c2be-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c2be-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9c2be-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c2be-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9c2be-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c2be-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c2be-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c2be-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c2be-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c2be-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c2be-127">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c2be-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9c2be-128">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9c2be-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




