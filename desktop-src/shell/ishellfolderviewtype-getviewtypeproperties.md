---
description: Obtiene las propiedades de la vista.
title: 'IShellFolderViewType:: GetViewTypeProperties (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: f4368edf6eae3e6892a3d81147401e061548f6e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984623"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="613cd-103">IShellFolderViewType:: GetViewTypeProperties (método)</span><span class="sxs-lookup"><span data-stu-id="613cd-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="613cd-104">Obtiene las propiedades de la vista.</span><span class="sxs-lookup"><span data-stu-id="613cd-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="613cd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="613cd-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="613cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="613cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="613cd-107">*PIDL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="613cd-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="613cd-108">Tipo: **PCUITEMID \_ secundario**</span><span class="sxs-lookup"><span data-stu-id="613cd-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="613cd-109">UN PIDL.</span><span class="sxs-lookup"><span data-stu-id="613cd-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="613cd-110">*pdwFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="613cd-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="613cd-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="613cd-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="613cd-112">Puntero a una variable de entero sin signo que recibe las propiedades de la vista, que indican qué hacer cuando se selecciona la vista.</span><span class="sxs-lookup"><span data-stu-id="613cd-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="613cd-113">Las marcas pueden ser cualquier combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="613cd-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="613cd-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG \_ Notify \_ Create*\* (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="613cd-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *SFVTFLAG\_NOTIFY\_CREATE*\* (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="613cd-115">Crear elemento de vista si no lo está.</span><span class="sxs-lookup"><span data-stu-id="613cd-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="613cd-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFICAr a \_ Resort** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="613cd-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="613cd-117">Vuelva a insertar PIDL y vuelva a ordenar.</span><span class="sxs-lookup"><span data-stu-id="613cd-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="613cd-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="613cd-118">Return value</span></span>

<span data-ttu-id="613cd-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="613cd-119">Type: **HRESULT**</span></span>

<span data-ttu-id="613cd-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="613cd-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="613cd-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="613cd-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="613cd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="613cd-122">Requirements</span></span>



| <span data-ttu-id="613cd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="613cd-123">Requirement</span></span> | <span data-ttu-id="613cd-124">Value</span><span class="sxs-lookup"><span data-stu-id="613cd-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="613cd-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="613cd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="613cd-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="613cd-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="613cd-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="613cd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="613cd-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="613cd-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="613cd-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="613cd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="613cd-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="613cd-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




