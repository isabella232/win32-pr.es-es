---
description: Extiende el objeto FolderItems. Admite un método adicional.
title: Objeto FolderItems2 (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0ca0efb3-6831-4561-9fd1-6d0b62704931
ms.openlocfilehash: ade67fe931b443e40ea063d4a2ca46e212c35b86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984166"
---
# <a name="folderitems2-object"></a><span data-ttu-id="cb095-104">Objeto FolderItems2</span><span class="sxs-lookup"><span data-stu-id="cb095-104">FolderItems2 object</span></span>

<span data-ttu-id="cb095-105">Extiende el objeto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="cb095-105">Extends the [**FolderItems**](folderitems.md) object.</span></span> <span data-ttu-id="cb095-106">Admite un método adicional.</span><span class="sxs-lookup"><span data-stu-id="cb095-106">It supports one additional method.</span></span>

## <a name="members"></a><span data-ttu-id="cb095-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cb095-107">Members</span></span>

<span data-ttu-id="cb095-108">El objeto **FolderItems2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cb095-108">The **FolderItems2** object has these types of members:</span></span>

-   [<span data-ttu-id="cb095-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb095-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cb095-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb095-110">Methods</span></span>

<span data-ttu-id="cb095-111">El objeto **FolderItems2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cb095-111">The **FolderItems2** object has these methods.</span></span>



| <span data-ttu-id="cb095-112">Método</span><span class="sxs-lookup"><span data-stu-id="cb095-112">Method</span></span>                                            | <span data-ttu-id="cb095-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb095-113">Description</span></span>                                                                                                                                                                                                                                         |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb095-114">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="cb095-114">**InvokeVerbEx**</span></span>](folderitems2-invokeverbex.md) | <span data-ttu-id="cb095-115">Ejecuta un verbo en una colección de objetos [**carpeta**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="cb095-115">Executes a verb on a collection of [**FolderItem**](folderitem.md) objects.</span></span> <span data-ttu-id="cb095-116">Este método es una extensión del método [**InvokeVerb**](folderitem-invokeverb.md) , lo que permite un control adicional de la operación a través de un conjunto de marcas.</span><span class="sxs-lookup"><span data-stu-id="cb095-116">This method is an extension of the [**InvokeVerb**](folderitem-invokeverb.md) method, allowing additional control of the operation through a set of flags.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cb095-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb095-117">Requirements</span></span>



| <span data-ttu-id="cb095-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb095-118">Requirement</span></span> | <span data-ttu-id="cb095-119">Value</span><span class="sxs-lookup"><span data-stu-id="cb095-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb095-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb095-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cb095-121">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="cb095-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb095-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb095-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cb095-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb095-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cb095-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb095-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb095-125"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb095-125"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cb095-126">IDL</span><span class="sxs-lookup"><span data-stu-id="cb095-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb095-127"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb095-127"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cb095-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb095-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb095-129"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="cb095-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb095-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb095-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb095-131">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="cb095-131">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[<span data-ttu-id="cb095-132">**ShellExecuteEx**</span><span class="sxs-lookup"><span data-stu-id="cb095-132">**ShellExecuteEx**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)
</dt> </dl>

 

 




