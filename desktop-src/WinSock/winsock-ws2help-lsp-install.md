---
description: Evento de cambio de catálogo Winsock para una operación de instalación de un proveedor de servicios por capas (LSP).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: Evento WINSOCK_WS2HELP_LSP_INSTALL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2d95a77f68bafd29fde3bbf34336d9b31d2a412e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002518"
---
# <a name="winsock_ws2help_lsp_install-event"></a><span data-ttu-id="73fcd-103">Evento de instalación de WS2HELP de LSP de WINSOCK \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="73fcd-103">WINSOCK\_WS2HELP\_LSP\_INSTALL event</span></span>

> [!Note]  
> <span data-ttu-id="73fcd-104">Los proveedores de servicios superpuestos están desusados.</span><span class="sxs-lookup"><span data-stu-id="73fcd-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="73fcd-105">A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="73fcd-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="73fcd-106">El evento de instalación de **Winsock \_ WS2HELP \_ LSP \_** es un evento de cambio de catálogo Winsock para una operación de instalación de un proveedor de servicios por capas (LSP).</span><span class="sxs-lookup"><span data-stu-id="73fcd-106">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is a Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="73fcd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73fcd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fcd-108">*Nombre del LSP*</span><span class="sxs-lookup"><span data-stu-id="73fcd-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="73fcd-109">El nombre del LSP tal como se obtuvo del miembro **szProtocol** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se está instalando.</span><span class="sxs-lookup"><span data-stu-id="73fcd-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> <dt>

<span data-ttu-id="73fcd-110">*Catálogo*</span><span class="sxs-lookup"><span data-stu-id="73fcd-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="73fcd-111">El catálogo Winsock (32 bits o 64 bits) en el que se está instalando el LSP.</span><span class="sxs-lookup"><span data-stu-id="73fcd-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="73fcd-112">Es un valor entero que es 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="73fcd-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="73fcd-113">*Instalador*</span><span class="sxs-lookup"><span data-stu-id="73fcd-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="73fcd-114">El nombre de archivo del módulo de la aplicación que realiza la llamada de instalación de LSP.</span><span class="sxs-lookup"><span data-stu-id="73fcd-114">The module filename of the application making the LSP install call.</span></span>

</dd> <dt>

<span data-ttu-id="73fcd-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="73fcd-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="73fcd-116">Valor GUID del proveedor de transporte Winsock en el que se está instalando el LSP.</span><span class="sxs-lookup"><span data-stu-id="73fcd-116">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span>

</dd> <dt>

<span data-ttu-id="73fcd-117">*Categoría*</span><span class="sxs-lookup"><span data-stu-id="73fcd-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="73fcd-118">El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se está instalando.</span><span class="sxs-lookup"><span data-stu-id="73fcd-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73fcd-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73fcd-119">Remarks</span></span>

<span data-ttu-id="73fcd-120">Se realiza un seguimiento del evento de **\_ instalación de WS2HELP \_ LSP \_ de Winsock** para una operación de instalación de LSP cuando se instala una entrada de protocolo en el catálogo de Winsock.</span><span class="sxs-lookup"><span data-stu-id="73fcd-120">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is traced for an LSP install operation when a protocol entry is installed into the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="73fcd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73fcd-121">Requirements</span></span>



| <span data-ttu-id="73fcd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="73fcd-122">Requirement</span></span> | <span data-ttu-id="73fcd-123">Value</span><span class="sxs-lookup"><span data-stu-id="73fcd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="73fcd-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73fcd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="73fcd-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="73fcd-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="73fcd-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73fcd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="73fcd-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="73fcd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73fcd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="73fcd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73fcd-129">Control de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="73fcd-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="73fcd-130">Seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="73fcd-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="73fcd-131">Niveles de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="73fcd-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="73fcd-132">Detalles de seguimiento de cambios de catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="73fcd-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
