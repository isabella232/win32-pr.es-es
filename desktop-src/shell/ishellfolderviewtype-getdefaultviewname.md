---
description: Obtiene el nombre de la vista predeterminada. Llame a GetDisplayNameOf para recuperar los nombres de las otras vistas.
title: IShellFolderViewType::GetDefaultViewName (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetDefaultViewName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 99229d13-40dc-4750-81a7-48a2f608b778
ms.openlocfilehash: 808f68093512e2da602d5e73775b47943b140a46
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842766"
---
# <a name="ishellfolderviewtypegetdefaultviewname-method"></a><span data-ttu-id="cc671-104">IShellFolderViewType::GetDefaultViewName (método)</span><span class="sxs-lookup"><span data-stu-id="cc671-104">IShellFolderViewType::GetDefaultViewName method</span></span>

<span data-ttu-id="cc671-105">Obtiene el nombre de la vista predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cc671-105">Gets the name of the default view.</span></span> <span data-ttu-id="cc671-106">Llame [**a GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para recuperar los nombres de las otras vistas.</span><span class="sxs-lookup"><span data-stu-id="cc671-106">Call [**GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc671-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc671-107">Syntax</span></span>


```C++
HRESULT GetDefaultViewName(
  [in]  DWORD  uFlags,
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="cc671-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc671-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc671-109">*uFlags* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="cc671-109">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc671-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cc671-110">Type: **DWORD**</span></span>

<span data-ttu-id="cc671-111">Marcas opcionales; debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="cc671-111">Optional flags; should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="cc671-112">*ppwszName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cc671-112">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc671-113">Tipo: **LPWSTR \***</span><span class="sxs-lookup"><span data-stu-id="cc671-113">Type: **LPWSTR\***</span></span>

<span data-ttu-id="cc671-114">Dirección de un puntero de cadena que recibe el nombre de vista predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cc671-114">The address of a string pointer that receives the default view name.</span></span> <span data-ttu-id="cc671-115">La memoria de la cadena se asigna con [**SHStrDup.**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa)</span><span class="sxs-lookup"><span data-stu-id="cc671-115">The memory for the string is allocated with [**SHStrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc671-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc671-116">Return value</span></span>

<span data-ttu-id="cc671-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cc671-117">Type: **HRESULT**</span></span>

<span data-ttu-id="cc671-118">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cc671-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc671-119">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="cc671-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc671-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc671-120">Requirements</span></span>



| <span data-ttu-id="cc671-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc671-121">Requirement</span></span> | <span data-ttu-id="cc671-122">Value</span><span class="sxs-lookup"><span data-stu-id="cc671-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc671-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc671-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cc671-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cc671-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cc671-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc671-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cc671-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cc671-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cc671-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc671-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc671-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc671-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




