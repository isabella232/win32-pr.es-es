---
description: Evento de cambio de catálogo Winsock para una operación de eliminación de un proveedor de servicios por capas (LSP).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: Evento WINSOCK_WS2HELP_LSP_REMOVE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 597cd2f8cfc3bb7727301e64af53671bafbd9469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697476"
---
# <a name="winsock_ws2help_lsp_remove-event"></a><span data-ttu-id="e7b0e-103">\_Evento de \_ eliminación de LSP de Winsock WS2HELP \_</span><span class="sxs-lookup"><span data-stu-id="e7b0e-103">WINSOCK\_WS2HELP\_LSP\_REMOVE event</span></span>

> [!Note]  
> <span data-ttu-id="e7b0e-104">Los proveedores de servicios superpuestos están desusados.</span><span class="sxs-lookup"><span data-stu-id="e7b0e-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="e7b0e-105">A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="e7b0e-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="e7b0e-106">El evento de eliminación de **\_ \_ LSP \_ de Winsock WS2HELP** es un evento de cambio de catálogo Winsock para una operación de eliminación de un proveedor de servicios por capas (LSP).</span><span class="sxs-lookup"><span data-stu-id="e7b0e-106">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is a Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="e7b0e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7b0e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b0e-108">*Nombre del LSP*</span><span class="sxs-lookup"><span data-stu-id="e7b0e-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b0e-109">Nombre del LSP obtenido del miembro **szProtocol** de la estructura de información de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="e7b0e-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> <dt>

<span data-ttu-id="e7b0e-110">*Catálogo*</span><span class="sxs-lookup"><span data-stu-id="e7b0e-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b0e-111">El catálogo Winsock (32 bits o 64 bits) en el que se va a quitar el LSP.</span><span class="sxs-lookup"><span data-stu-id="e7b0e-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="e7b0e-112">Es un valor entero que es 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="e7b0e-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="e7b0e-113">*Instalador*</span><span class="sxs-lookup"><span data-stu-id="e7b0e-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b0e-114">El nombre de archivo del módulo de la aplicación que realiza la llamada Remove de LSP.</span><span class="sxs-lookup"><span data-stu-id="e7b0e-114">The module filename of the application making the LSP remove call.</span></span>

</dd> <dt>

<span data-ttu-id="e7b0e-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e7b0e-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b0e-116">Valor GUID del proveedor de transporte Winsock del que se va a quitar el LSP.</span><span class="sxs-lookup"><span data-stu-id="e7b0e-116">The GUID value of the Winsock transport provider that the LSP is being removed from.</span></span>

</dd> <dt>

<span data-ttu-id="e7b0e-117">*Categoría*</span><span class="sxs-lookup"><span data-stu-id="e7b0e-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="e7b0e-118">El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="e7b0e-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7b0e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7b0e-119">Remarks</span></span>

<span data-ttu-id="e7b0e-120">Se realiza un seguimiento del evento de eliminación de **\_ \_ LSP \_ de Winsock WS2HELP** para una operación de eliminación de LSP cuando se quita una entrada de protocolo del catálogo de Winsock.</span><span class="sxs-lookup"><span data-stu-id="e7b0e-120">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is traced for an LSP removal operation when a protocol entry is removed from the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b0e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7b0e-121">Requirements</span></span>



| <span data-ttu-id="e7b0e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7b0e-122">Requirement</span></span> | <span data-ttu-id="e7b0e-123">Value</span><span class="sxs-lookup"><span data-stu-id="e7b0e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7b0e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7b0e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e7b0e-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e7b0e-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7b0e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7b0e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e7b0e-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7b0e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7b0e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7b0e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b0e-129">Control de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="e7b0e-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="e7b0e-130">Seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="e7b0e-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="e7b0e-131">Niveles de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="e7b0e-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="e7b0e-132">Detalles de seguimiento de cambios de catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="e7b0e-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
