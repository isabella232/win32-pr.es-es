---
title: Interfaz IDODownloadInternal
description: Se usa para obtener o establecer las propiedades de descarga extendida.
keywords:
- Interfaz IDODownloadInternal
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149461"
---
# <a name="idodownloadinternal-interface"></a><span data-ttu-id="fbf49-104">Interfaz IDODownloadInternal</span><span class="sxs-lookup"><span data-stu-id="fbf49-104">IDODownloadInternal interface</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fbf49-105">La interfaz **IDODownloadInternal** está en desuso.</span><span class="sxs-lookup"><span data-stu-id="fbf49-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="fbf49-106">En su lugar, use la interfaz [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="fbf49-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="fbf49-107">La interfaz **IDODownloadInternal** se usa para obtener o establecer las propiedades de descarga extendida.</span><span class="sxs-lookup"><span data-stu-id="fbf49-107">The **IDODownloadInternal** interface is used to get or set extended download properties.</span></span>

## <a name="methods"></a><span data-ttu-id="fbf49-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="fbf49-108">Methods</span></span>

<span data-ttu-id="fbf49-109">La interfaz **IDODownloadInternal** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fbf49-109">The **IDODownloadInternal** interface has these methods.</span></span>

| <span data-ttu-id="fbf49-110">Método</span><span class="sxs-lookup"><span data-stu-id="fbf49-110">Method</span></span> | <span data-ttu-id="fbf49-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbf49-111">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="fbf49-112">IDODownloadInternal::GetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="fbf49-112">IDODownloadInternal::GetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | <span data-ttu-id="fbf49-113">Recupera un puntero a una **variante** que contiene un valor de propiedad de descarga extendida específico.</span><span class="sxs-lookup"><span data-stu-id="fbf49-113">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span> |
| [<span data-ttu-id="fbf49-114">IDODownloadInternal::SetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="fbf49-114">IDODownloadInternal::SetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | <span data-ttu-id="fbf49-115">Establece una propiedad de descarga extendida.</span><span class="sxs-lookup"><span data-stu-id="fbf49-115">Sets an extended download property.</span></span> <span data-ttu-id="fbf49-116">El método acepta un puntero a una **variante** que contiene un valor de propiedad específico que se va a aplicar a la descarga.</span><span class="sxs-lookup"><span data-stu-id="fbf49-116">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="fbf49-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbf49-117">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fbf49-118">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="fbf49-118">**Minimum supported client**</span></span> | <span data-ttu-id="fbf49-119">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbf49-119">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="fbf49-120">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="fbf49-120">**Minimum supported server**</span></span> | <span data-ttu-id="fbf49-121">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="fbf49-121">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="fbf49-122">**Header**</span><span class="sxs-lookup"><span data-stu-id="fbf49-122">**Header**</span></span> | <span data-ttu-id="fbf49-123">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="fbf49-123">DODownloadInternal.h</span></span> |