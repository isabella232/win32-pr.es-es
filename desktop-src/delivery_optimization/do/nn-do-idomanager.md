---
title: Interfaz IDOManager
description: Se usa para crear una nueva descarga y para enumerar las descargas existentes.
keywords:
- Interfaz IDOManager
topic_type:
- apiref
api_name:
- IDOManager
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a8755615e4d2f0fd074117438f8f305dce0cb681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720168"
---
# <a name="idomanager-interface"></a><span data-ttu-id="fb450-104">Interfaz IDOManager</span><span class="sxs-lookup"><span data-stu-id="fb450-104">IDOManager interface</span></span>

<span data-ttu-id="fb450-105">La interfaz **IDOManager** se usa para crear una nueva descarga y enumerar las descargas existentes.</span><span class="sxs-lookup"><span data-stu-id="fb450-105">The **IDOManager** interface is used to create a new download, and to enumerate existing downloads.</span></span>

## <a name="methods"></a><span data-ttu-id="fb450-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="fb450-106">Methods</span></span>

<span data-ttu-id="fb450-107">La interfaz **IDOManager** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fb450-107">The **IDOManager** interface has these methods.</span></span>

| <span data-ttu-id="fb450-108">Método</span><span class="sxs-lookup"><span data-stu-id="fb450-108">Method</span></span> | <span data-ttu-id="fb450-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb450-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="fb450-110">IDOManager::CreateDownload</span><span class="sxs-lookup"><span data-stu-id="fb450-110">IDOManager::CreateDownload</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="fb450-111">Crea una nueva descarga.</span><span class="sxs-lookup"><span data-stu-id="fb450-111">Creates a new download.</span></span> |
| [<span data-ttu-id="fb450-112">IDOManager::EnumDownloads</span><span class="sxs-lookup"><span data-stu-id="fb450-112">IDOManager::EnumDownloads</span></span>](./nf-do-idomanager-enumdownloads.md) | <span data-ttu-id="fb450-113">Recupera un puntero de interfaz a un objeto de enumerador que se usa para enumerar las descargas existentes.</span><span class="sxs-lookup"><span data-stu-id="fb450-113">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span> |

## <a name="requirements"></a><span data-ttu-id="fb450-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb450-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fb450-115">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="fb450-115">**Minimum supported client**</span></span> | <span data-ttu-id="fb450-116">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb450-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="fb450-117">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="fb450-117">**Minimum supported server**</span></span> | <span data-ttu-id="fb450-118">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="fb450-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="fb450-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="fb450-119">**Header**</span></span> | <span data-ttu-id="fb450-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="fb450-120">Do.h</span></span> |