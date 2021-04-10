---
description: Contiene un puntero a la interfaz IMFSourceOpenMonitor de las aplicaciones.
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: Propiedad MFPKEY_SourceOpenMonitor (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a49826ee16a733993b9052e12d9e6fcd5003410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156072"
---
# <a name="mfpkey_sourceopenmonitor-property"></a><span data-ttu-id="77b46-103">\_Propiedad SourceOpenMonitor de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="77b46-103">MFPKEY\_SourceOpenMonitor property</span></span>

<span data-ttu-id="77b46-104">Contiene un puntero a la interfaz [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="77b46-104">Contains a pointer to the application's [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>



<span data-ttu-id="77b46-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="77b46-105">Data type</span></span>

<span data-ttu-id="77b46-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="77b46-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="77b46-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="77b46-107">PROPVARIANT member</span></span>

<span data-ttu-id="77b46-108">**IUnknown** (puntero)</span><span class="sxs-lookup"><span data-stu-id="77b46-108">**IUnknown** pointer</span></span>

<span data-ttu-id="77b46-109">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="77b46-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="77b46-110">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="77b46-110">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="77b46-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77b46-111">Remarks</span></span>

<span data-ttu-id="77b46-112">Las aplicaciones pueden pasar esta propiedad al solucionador de origen para obtener notificaciones de eventos del origen de red.</span><span class="sxs-lookup"><span data-stu-id="77b46-112">Applications can pass this property to the source resolver to get event notifications from the network source.</span></span>

## <a name="requirements"></a><span data-ttu-id="77b46-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77b46-113">Requirements</span></span>



| <span data-ttu-id="77b46-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="77b46-114">Requirement</span></span> | <span data-ttu-id="77b46-115">Value</span><span class="sxs-lookup"><span data-stu-id="77b46-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77b46-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77b46-116">Minimum supported client</span></span><br/> | <span data-ttu-id="77b46-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="77b46-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="77b46-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77b46-118">Minimum supported server</span></span><br/> | <span data-ttu-id="77b46-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="77b46-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="77b46-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77b46-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="77b46-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77b46-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77b46-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="77b46-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b46-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="77b46-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




