---
description: Obtiene las propiedades de la vista.
title: IShellFolderViewType::GetViewTypeProperties (método)
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
ms.openlocfilehash: f5c7c6b75c89711a69ac578b3d04a72362b1eac9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842706"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a><span data-ttu-id="4467f-103">IShellFolderViewType::GetViewTypeProperties (método)</span><span class="sxs-lookup"><span data-stu-id="4467f-103">IShellFolderViewType::GetViewTypeProperties method</span></span>

<span data-ttu-id="4467f-104">Obtiene las propiedades de la vista.</span><span class="sxs-lookup"><span data-stu-id="4467f-104">Gets the properties of the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="4467f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4467f-105">Syntax</span></span>


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4467f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4467f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4467f-107">*pidl* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4467f-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4467f-108">Tipo: **PCUITEMID \_ CHILD**</span><span class="sxs-lookup"><span data-stu-id="4467f-108">Type: **PCUITEMID\_CHILD**</span></span>

<span data-ttu-id="4467f-109">A PIDL.</span><span class="sxs-lookup"><span data-stu-id="4467f-109">A PIDL.</span></span>

</dd> <dt>

<span data-ttu-id="4467f-110">*pdwFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4467f-110">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4467f-111">Tipo: **DWORD \***</span><span class="sxs-lookup"><span data-stu-id="4467f-111">Type: **DWORD\***</span></span>

<span data-ttu-id="4467f-112">Puntero a una variable de entero sin signo que recibe las propiedades de vista, que indican qué hacer cuando se selecciona la vista.</span><span class="sxs-lookup"><span data-stu-id="4467f-112">A pointer to an unsigned integer variable that receives the view properties, which indicate what to do when the view is selected.</span></span> <span data-ttu-id="4467f-113">Las marcas pueden ser cualquier combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4467f-113">Flags may be any combination of the following values.</span></span>

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span data-ttu-id="4467f-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG \_ NOTIFY \_ CREATE** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="4467f-114"><span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG\_NOTIFY\_CREATE** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="4467f-115">Cree un elemento de vista si no está ahí.</span><span class="sxs-lookup"><span data-stu-id="4467f-115">Create view item if not there.</span></span>

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span data-ttu-id="4467f-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_ NOTIFY \_ RESORT** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="4467f-116"><span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG\_NOTIFY\_RESORT** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="4467f-117">Vuelva a insertar PIDL y vuelva a ordenar.</span><span class="sxs-lookup"><span data-stu-id="4467f-117">Reinsert PIDL and re-sort.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4467f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4467f-118">Return value</span></span>

<span data-ttu-id="4467f-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4467f-119">Type: **HRESULT**</span></span>

<span data-ttu-id="4467f-120">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4467f-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4467f-121">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="4467f-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4467f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4467f-122">Requirements</span></span>



| <span data-ttu-id="4467f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4467f-123">Requirement</span></span> | <span data-ttu-id="4467f-124">Value</span><span class="sxs-lookup"><span data-stu-id="4467f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4467f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4467f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4467f-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4467f-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4467f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4467f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4467f-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4467f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4467f-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4467f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4467f-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4467f-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




