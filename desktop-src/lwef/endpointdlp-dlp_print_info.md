---
description: Especifica información sobre un documento asociado a una operación de impresión DLP de punto de conexión.
title: DLP_PRINT_INFO estructura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 37bde9f62de07083aac6a3d2fb367b021caf3732
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495958"
---
# <a name="dlp_print_info-structure"></a><span data-ttu-id="3a498-103">DLP_PRINT_INFO estructura</span><span class="sxs-lookup"><span data-stu-id="3a498-103">DLP_PRINT_INFO structure</span></span>

<span data-ttu-id="3a498-104">Especifica información sobre un documento asociado a una operación de impresión DLP de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="3a498-104">Specifies information about a document that is associated with an endpoint DLP print operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a498-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a498-105">Syntax</span></span>


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a><span data-ttu-id="3a498-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="3a498-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3a498-107">*Versión* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3a498-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a498-108">DWORD que especifica la versión de LA API.</span><span class="sxs-lookup"><span data-stu-id="3a498-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="3a498-109">Este valor siempre debe ser **DLP_PRINT_INFO_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="3a498-109">This value should always be **DLP_PRINT_INFO_V_LATEST**.</span></span> <span data-ttu-id="3a498-110">Esta constante se define en la lista de archivos de encabezado de ejemplo endpointdlp.h del artículo Prevención de [pérdida de datos de punto de conexión.](endpointdlp-endpoint-data-loss-prevention.md)</span><span class="sxs-lookup"><span data-stu-id="3a498-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3a498-111">*PrinterName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3a498-111">*PrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a498-112">LPCWSTR que identifica la impresora de destino.</span><span class="sxs-lookup"><span data-stu-id="3a498-112">A LPCWSTR identifying the destination printer.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3a498-113">*JobName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3a498-113">*JobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a498-114">LPCWSTR que especifica el nombre del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="3a498-114">A LPCWSTR specifying print job name.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="3a498-115">*OutputFileName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3a498-115">*OutputFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a498-116">LPCWSTR que especifica la ruta de acceso al archivo de salida al imprimir en un archivo.</span><span class="sxs-lookup"><span data-stu-id="3a498-116">A LPCWSTR specifying the path to the output file, when printing to a file.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="3a498-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a498-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="3a498-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a498-118">Requirements</span></span>



| <span data-ttu-id="3a498-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a498-119">Requirement</span></span>          |    <span data-ttu-id="3a498-120">Value</span><span class="sxs-lookup"><span data-stu-id="3a498-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a498-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a498-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a498-122">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="3a498-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

