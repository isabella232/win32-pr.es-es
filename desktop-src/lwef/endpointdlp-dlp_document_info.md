---
description: Especifica información sobre un documento asociado a una operación DLP de punto de conexión.
title: DLP_DOCUMENT_INFO estructura (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495961"
---
# <a name="dlp_document_info-structure"></a><span data-ttu-id="07bd6-103">DLP_DOCUMENT_INFO estructura</span><span class="sxs-lookup"><span data-stu-id="07bd6-103">DLP_DOCUMENT_INFO structure</span></span>

<span data-ttu-id="07bd6-104">Especifica información sobre un documento asociado a una operación DLP de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="07bd6-104">Specifies information about a document that is associated with an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="07bd6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07bd6-105">Syntax</span></span>


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a><span data-ttu-id="07bd6-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="07bd6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07bd6-107">*Versión* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="07bd6-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bd6-108">DWORD que especifica la versión de la API.</span><span class="sxs-lookup"><span data-stu-id="07bd6-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="07bd6-109">Este valor siempre debe ser **DLP_DOCUMENT_INFO_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="07bd6-109">This value should always be **DLP_DOCUMENT_INFO_V_LATEST**.</span></span> <span data-ttu-id="07bd6-110">Esta constante se define en la lista de archivos de encabezado de ejemplo endpointdlp.h del artículo Prevención de [pérdida de datos de punto de conexión.](endpointdlp-endpoint-data-loss-prevention.md)</span><span class="sxs-lookup"><span data-stu-id="07bd6-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md).</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="07bd6-111">*PersistentFileName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="07bd6-111">*PersistentFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bd6-112">LPCWSTR que especifica la ruta de acceso original del documento.</span><span class="sxs-lookup"><span data-stu-id="07bd6-112">A LPCWSTR specifying the original path of the document.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="07bd6-113">*LocalFileName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="07bd6-113">*LocalFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bd6-114">LPCWSTR que especifica la ruta de acceso al archivo de respaldo real del documento.</span><span class="sxs-lookup"><span data-stu-id="07bd6-114">A LPCWSTR specifying the path to the real backing file of the document.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="07bd6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07bd6-115">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="07bd6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07bd6-116">Requirements</span></span>



| <span data-ttu-id="07bd6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="07bd6-117">Requirement</span></span>          |    <span data-ttu-id="07bd6-118">Value</span><span class="sxs-lookup"><span data-stu-id="07bd6-118">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07bd6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07bd6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="07bd6-120">Windows 10, versión 1809 (10.0; Compilación 17763)</span><span class="sxs-lookup"><span data-stu-id="07bd6-120">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

