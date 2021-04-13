---
description: Define un método que determina si se permitirá que el shell mueva, copie, elimine o cambie el nombre de una carpeta en la raíz de sincronización de un proveedor de la nube.
title: Interfaz de IStorageProviderCopyHook
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422185"
---
# <a name="istorageprovidercopyhook-interface"></a><span data-ttu-id="c0a22-103">Interfaz de IStorageProviderCopyHook</span><span class="sxs-lookup"><span data-stu-id="c0a22-103">IStorageProviderCopyHook interface</span></span>

<span data-ttu-id="c0a22-104">Expone un método que determina si el shell podrá moverse, copiar, eliminar o cambiar el nombre de una carpeta en la raíz de sincronización de un proveedor de la nube.</span><span class="sxs-lookup"><span data-stu-id="c0a22-104">Exposes a method that determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="members"></a><span data-ttu-id="c0a22-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="c0a22-105">Members</span></span>

<span data-ttu-id="c0a22-106">La interfaz **IStorageProviderCopyHook** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c0a22-106">The **IStorageProviderCopyHook** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c0a22-107">**IStorageProviderCopyHook** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c0a22-107">**IStorageProviderCopyHook** also has these types of members:</span></span>

- [<span data-ttu-id="c0a22-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c0a22-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0a22-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c0a22-109">Methods</span></span>

<span data-ttu-id="c0a22-110">La interfaz **IStorageProviderCopyHook** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c0a22-110">The **IStorageProviderCopyHook** interface has these methods.</span></span>



| <span data-ttu-id="c0a22-111">Método</span><span class="sxs-lookup"><span data-stu-id="c0a22-111">Method</span></span>                                           | <span data-ttu-id="c0a22-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0a22-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0a22-113">**CopyCallback**</span><span class="sxs-lookup"><span data-stu-id="c0a22-113">**CopyCallback**</span></span>](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  <span data-ttu-id="c0a22-114">Determina si se permitirá que el shell mueva, copie, elimine o cambie el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.</span><span class="sxs-lookup"><span data-stu-id="c0a22-114">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>                                                           |


## <a name="requirements"></a><span data-ttu-id="c0a22-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0a22-115">Requirements</span></span>

| <span data-ttu-id="c0a22-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0a22-116">Requirement</span></span> | <span data-ttu-id="c0a22-117">Value</span><span class="sxs-lookup"><span data-stu-id="c0a22-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a22-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0a22-118">Minimum supported client</span></span> | <span data-ttu-id="c0a22-119">Compilación 19624 de Windows 10 Insider Preview</span><span class="sxs-lookup"><span data-stu-id="c0a22-119">Windows 10 Insider Preview Build 19624</span></span>                                                |
| <span data-ttu-id="c0a22-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0a22-120">Header</span></span><br/>                   | <span data-ttu-id="c0a22-121">shobjidl. h</span><span class="sxs-lookup"><span data-stu-id="c0a22-121">shobjidl.h</span></span>   |
