---
description: Evento de cambio de catálogo Winsock para una operación de restablecimiento del catálogo Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: Evento WINSOCK_WS2HELP_LSP_RESET
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 219eb85dec0cdda77ca8741ae42df1f63d1a7dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697475"
---
# <a name="winsock_ws2help_lsp_reset-event"></a><span data-ttu-id="8cb1d-103">\_Evento de \_ restablecimiento de LSP de WS2HELP de Winsock \_</span><span class="sxs-lookup"><span data-stu-id="8cb1d-103">WINSOCK\_WS2HELP\_LSP\_RESET event</span></span>

> [!Note]  
> <span data-ttu-id="8cb1d-104">Los proveedores de servicios superpuestos están desusados.</span><span class="sxs-lookup"><span data-stu-id="8cb1d-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="8cb1d-105">A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="8cb1d-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="8cb1d-106">El evento de **\_ restablecimiento de \_ LSP \_ de Winsock WS2HELP** es un evento de cambio de catálogo Winsock para una operación de restablecimiento del catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="8cb1d-106">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is a Winsock catalog change event for a Winsock catalog reset operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="8cb1d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cb1d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cb1d-108">*Catálogo*</span><span class="sxs-lookup"><span data-stu-id="8cb1d-108">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="8cb1d-109">Catálogo Winsock (32 bits o 64 bits) que se va a restablecer.</span><span class="sxs-lookup"><span data-stu-id="8cb1d-109">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="8cb1d-110">Es un valor entero que es 32 o 64.</span><span class="sxs-lookup"><span data-stu-id="8cb1d-110">This is an integer value that is either 32 or 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cb1d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cb1d-111">Remarks</span></span>

<span data-ttu-id="8cb1d-112">Se realiza un seguimiento del evento **Winsock \_ WS2HELP \_ LSP \_ RESET** para una operación de proveedor de servicios por capas (LSP) de Winsock cuando se restablece el catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="8cb1d-112">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is traced for an Winsock Layered Service Provider (LSP) operation when the Winsock catalog is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cb1d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cb1d-113">Requirements</span></span>



| <span data-ttu-id="8cb1d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cb1d-114">Requirement</span></span> | <span data-ttu-id="8cb1d-115">Value</span><span class="sxs-lookup"><span data-stu-id="8cb1d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8cb1d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cb1d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8cb1d-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8cb1d-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8cb1d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cb1d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8cb1d-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8cb1d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8cb1d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cb1d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cb1d-121">Control de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="8cb1d-121">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="8cb1d-122">Seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="8cb1d-122">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="8cb1d-123">Niveles de seguimiento de Winsock</span><span class="sxs-lookup"><span data-stu-id="8cb1d-123">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="8cb1d-124">Detalles de seguimiento de cambios de catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="8cb1d-124">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
