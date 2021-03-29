---
description: Evento de cambio de catálogo Winsock para una operación de deshabilitación de un proveedor de servicios por capas (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: Evento WINSOCK_WS2HELP_LSP_DISABLE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648551"
---
# <a name="winsock_ws2help_lsp_disable-event"></a><span data-ttu-id="b4d5a-103">\_Evento de \_ \_ deshabilitación de LSP de Winsock WS2HELP</span><span class="sxs-lookup"><span data-stu-id="b4d5a-103">WINSOCK\_WS2HELP\_LSP\_DISABLE event</span></span>

> [!Note]  
> <span data-ttu-id="b4d5a-104">Los proveedores de servicios superpuestos están desusados.</span><span class="sxs-lookup"><span data-stu-id="b4d5a-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="b4d5a-105">A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="b4d5a-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="b4d5a-106">El evento **Winsock \_ WS2HELP \_ LSP \_ Disable** es un evento de cambio de catálogo Winsock para una operación de deshabilitación de un proveedor de servicios por capas (LSP).</span><span class="sxs-lookup"><span data-stu-id="b4d5a-106">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is a Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="b4d5a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4d5a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4d5a-108">*Nombre del LSP*</span><span class="sxs-lookup"><span data-stu-id="b4d5a-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="b4d5a-109">Nombre del LSP tal y como se obtiene del miembro **szProtocol** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="b4d5a-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="b4d5a-110">*Catálogo*</span><span class="sxs-lookup"><span data-stu-id="b4d5a-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="b4d5a-111">El catálogo Winsock (32 bits o 64 bits) en el que se deshabilita el LSP.</span><span class="sxs-lookup"><span data-stu-id="b4d5a-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="b4d5a-112">Es un valor entero que es 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="b4d5a-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="b4d5a-113">*Instalador*</span><span class="sxs-lookup"><span data-stu-id="b4d5a-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="b4d5a-114">El nombre de archivo del módulo de la aplicación que realiza la llamada de deshabilitación de LSP.</span><span class="sxs-lookup"><span data-stu-id="b4d5a-114">The module filename of the application making the LSP disable call.</span></span>

</dd> <dt>

<span data-ttu-id="b4d5a-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b4d5a-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="b4d5a-116">Valor GUID del proveedor de transporte Winsock en el que se va a deshabilitar el LSP.</span><span class="sxs-lookup"><span data-stu-id="b4d5a-116">The GUID value of the Winsock transport provider that the LSP is being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="b4d5a-117">*Categoría*</span><span class="sxs-lookup"><span data-stu-id="b4d5a-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="b4d5a-118">El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="b4d5a-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> </dl>

<span data-ttu-id="b4d5a-119">Este evento no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b4d5a-119">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4d5a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4d5a-120">Remarks</span></span>

<span data-ttu-id="b4d5a-121">Se realiza un seguimiento del evento de **\_ \_ \_ deshabilitación de LSP de Winsock WS2HELP** para una operación de deshabilitación de LSP cuando una entrada de protocolo está deshabilitada en el catálogo de Winsock.</span><span class="sxs-lookup"><span data-stu-id="b4d5a-121">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is traced for an LSP disable operation when a protocol entry is disabled in the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4d5a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4d5a-122">Requirements</span></span>



| <span data-ttu-id="b4d5a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4d5a-123">Requirement</span></span> | <span data-ttu-id="b4d5a-124">Value</span><span class="sxs-lookup"><span data-stu-id="b4d5a-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b4d5a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4d5a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b4d5a-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b4d5a-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b4d5a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4d5a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b4d5a-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4d5a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4d5a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4d5a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d5a-130">Control de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="b4d5a-130">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="b4d5a-131">Seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="b4d5a-131">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="b4d5a-132">Niveles de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="b4d5a-132">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="b4d5a-133">Detalles de seguimiento de cambios de catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="b4d5a-133">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
