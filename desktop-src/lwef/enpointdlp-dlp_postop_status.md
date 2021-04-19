---
description: Especifica información de estado sobre una operación DLP de punto de conexión.
title: DLP_POSTOP_STATUS estructura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495824"
---
# <a name="dlp_postop_status-structure"></a><span data-ttu-id="cd867-103">DLP_POSTOP_STATUS estructura</span><span class="sxs-lookup"><span data-stu-id="cd867-103">DLP_POSTOP_STATUS structure</span></span>

<span data-ttu-id="cd867-104">Especifica información de estado sobre una operación DLP de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="cd867-104">Specifies status information about an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd867-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd867-105">Syntax</span></span>


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a><span data-ttu-id="cd867-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd867-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd867-107">*Versión* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="cd867-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd867-108">DWORD que especifica la versión de LA API.</span><span class="sxs-lookup"><span data-stu-id="cd867-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="cd867-109">Este valor siempre se debe **DLP_POSTOP_STATUS_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="cd867-109">This value should always be **DLP_POSTOP_STATUS_V_LATEST**.</span></span> <span data-ttu-id="cd867-110">Esta constante se define en la lista de archivos de encabezado de ejemplo endpointdlp.h del artículo Prevención de [pérdida de datos de punto de conexión](endpointdlp-endpoint-data-loss-prevention.md)</span><span class="sxs-lookup"><span data-stu-id="cd867-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md)</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="cd867-111">*OperationSuccess* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="cd867-111">*OperationSuccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd867-112">Un BOOL que indica si la operación de apertura se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cd867-112">A BOOL indicating whether the open operation was successful.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="cd867-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd867-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="cd867-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd867-114">Requirements</span></span>



| <span data-ttu-id="cd867-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd867-115">Requirement</span></span>          |    <span data-ttu-id="cd867-116">Value</span><span class="sxs-lookup"><span data-stu-id="cd867-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd867-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd867-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd867-118">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="cd867-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
