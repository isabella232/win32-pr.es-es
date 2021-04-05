---
description: Matriz de cadenas con los parámetros que se van a enviar al servidor de registro.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: Propiedad MFNETSOURCE_LOGPARAMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001498"
---
# <a name="mfnetsource_logparams-property"></a><span data-ttu-id="e24b9-103">\_Propiedad LOGPARAMS de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="e24b9-103">MFNETSOURCE\_LOGPARAMS property</span></span>

<span data-ttu-id="e24b9-104">Matriz de cadenas con los parámetros que se van a enviar al servidor de registro.</span><span class="sxs-lookup"><span data-stu-id="e24b9-104">Array of strings with the parameters to send to the log server.</span></span>



<span data-ttu-id="e24b9-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e24b9-105">Data type</span></span>

<span data-ttu-id="e24b9-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="e24b9-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e24b9-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="e24b9-107">PROPVARIANT member</span></span>

<span data-ttu-id="e24b9-108">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="e24b9-108">\**WCHAR\** _</span></span>

<span data-ttu-id="e24b9-109">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="e24b9-109">VT\_LPWSTR</span></span>

<span data-ttu-id="e24b9-110">_ *pwszVal*\*</span><span class="sxs-lookup"><span data-stu-id="e24b9-110">_ *pwszVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="e24b9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e24b9-111">Remarks</span></span>

<span data-ttu-id="e24b9-112">La constante **MFNETSOURCE \_ LOGPARAMS** define el GUID de la clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e24b9-112">The **MFNETSOURCE\_LOGPARAMS** constant defines the GUID for the property key.</span></span> <span data-ttu-id="e24b9-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="e24b9-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="e24b9-114">Para establecer esta propiedad en el origen de red, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="e24b9-114">To set this property on the network source, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="e24b9-115">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="e24b9-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e24b9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e24b9-116">Requirements</span></span>



| <span data-ttu-id="e24b9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e24b9-117">Requirement</span></span> | <span data-ttu-id="e24b9-118">Value</span><span class="sxs-lookup"><span data-stu-id="e24b9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e24b9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e24b9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e24b9-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e24b9-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e24b9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e24b9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e24b9-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e24b9-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e24b9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e24b9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e24b9-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e24b9-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e24b9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e24b9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e24b9-126">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e24b9-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e24b9-127">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e24b9-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




