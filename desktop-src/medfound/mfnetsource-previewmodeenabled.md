---
description: Habilita o deshabilita el modo de vista previa, que permite que la aplicación sobrescriba la lógica de almacenamiento en búfer inicial.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: Propiedad MFNETSOURCE_PREVIEWMODEENABLED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1170135b0feb90a79bf5e26d36a02e262fdc1977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652875"
---
# <a name="mfnetsource_previewmodeenabled-property"></a><span data-ttu-id="f0001-103">\_Propiedad PREVIEWMODEENABLED de MFNETSOURCE</span><span class="sxs-lookup"><span data-stu-id="f0001-103">MFNETSOURCE\_PREVIEWMODEENABLED property</span></span>

<span data-ttu-id="f0001-104">Habilita o deshabilita el modo de vista previa, que permite que la aplicación sobrescriba la lógica de almacenamiento en búfer inicial.</span><span class="sxs-lookup"><span data-stu-id="f0001-104">Enables or disables preview mode, which enables the application to overwrite the initial buffering logic.</span></span>



<span data-ttu-id="f0001-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f0001-105">Data type</span></span>

<span data-ttu-id="f0001-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="f0001-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f0001-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="f0001-107">PROPVARIANT member</span></span>

<span data-ttu-id="f0001-108">**BOOLEANO**</span><span class="sxs-lookup"><span data-stu-id="f0001-108">**BOOL**</span></span>

<span data-ttu-id="f0001-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="f0001-109">VT\_BOOL</span></span>

<span data-ttu-id="f0001-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="f0001-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f0001-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0001-111">Remarks</span></span>

<span data-ttu-id="f0001-112">La constante **MFNETSOURCE \_ PREVIEWMODEENABLED** define el GUID de la clave de propiedad.</span><span class="sxs-lookup"><span data-stu-id="f0001-112">The constant **MFNETSOURCE\_PREVIEWMODEENABLED** defines the GUID for the property key.</span></span> <span data-ttu-id="f0001-113">El identificador de propiedad (PID) es cero.</span><span class="sxs-lookup"><span data-stu-id="f0001-113">The property identifier (PID) is zero.</span></span> <span data-ttu-id="f0001-114">Esta propiedad se establece en el origen de red pasando un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="f0001-114">This property is set on the network source by passing an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="f0001-115">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="f0001-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0001-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0001-116">Requirements</span></span>



| <span data-ttu-id="f0001-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0001-117">Requirement</span></span> | <span data-ttu-id="f0001-118">Value</span><span class="sxs-lookup"><span data-stu-id="f0001-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0001-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0001-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f0001-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0001-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f0001-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0001-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f0001-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0001-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f0001-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0001-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0001-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0001-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0001-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0001-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0001-126">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0001-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f0001-127">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0001-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




