---
description: Reconstruye un puntero a una lista de identificadores de elemento (PIDL) a partir de una representación jerárquica de la carpeta de Shell en una representación diferente.
title: 'IShellFolderViewType:: TranslateViewPidl (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.TranslateViewPidl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b7fa6c4-3d02-44ed-b63d-80a799e4017a
ms.openlocfilehash: 75876e5088c610c1f9f02ba9374db5cea4a6023c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543107"
---
# <a name="ishellfolderviewtypetranslateviewpidl-method"></a><span data-ttu-id="08d84-103">IShellFolderViewType:: TranslateViewPidl (método)</span><span class="sxs-lookup"><span data-stu-id="08d84-103">IShellFolderViewType::TranslateViewPidl method</span></span>

<span data-ttu-id="08d84-104">Reconstruye un puntero a una lista de identificadores de elemento (PIDL) a partir de una representación jerárquica de la carpeta de Shell en una representación diferente.</span><span class="sxs-lookup"><span data-stu-id="08d84-104">Reconstructs a pointer to an item identifier list (PIDL) from one hierarchical representation of the Shell folder into a different representation.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d84-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08d84-105">Syntax</span></span>


```C++
HRESULT TranslateViewPidl(
  [in] PCUIDLIST_RELATIVE pidl,
  [in] PCUIDLIST_RELATIVE pidlView,
  [in] PCUIDLIST_RELATIVE *ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="08d84-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08d84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d84-107">*PIDL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08d84-107">*pidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08d84-108">Tipo: **PCUIDLIST \_ relativo**</span><span class="sxs-lookup"><span data-stu-id="08d84-108">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="08d84-109">La matriz de identificadores de elemento relativa a la carpeta raíz.</span><span class="sxs-lookup"><span data-stu-id="08d84-109">The array of item IDs relative to the root folder.</span></span>

</dd> <dt>

<span data-ttu-id="08d84-110">*pidlView* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08d84-110">*pidlView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08d84-111">Tipo: **PCUIDLIST \_ relativo**</span><span class="sxs-lookup"><span data-stu-id="08d84-111">Type: **PCUIDLIST\_RELATIVE**</span></span>

<span data-ttu-id="08d84-112">PIDL especial de la vista.</span><span class="sxs-lookup"><span data-stu-id="08d84-112">Special PIDL of the view.</span></span>

</dd> <dt>

<span data-ttu-id="08d84-113">*ppidlOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08d84-113">*ppidlOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08d84-114">Tipo: \**PCUIDLIST \_ relative \** _</span><span class="sxs-lookup"><span data-stu-id="08d84-114">Type: \**PCUIDLIST\_RELATIVE\** _</span></span>

<span data-ttu-id="08d84-115">La dirección de una variable PIDL para recibir la traducción.</span><span class="sxs-lookup"><span data-stu-id="08d84-115">The address of a PIDL variable to receive the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08d84-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08d84-116">Return value</span></span>

<span data-ttu-id="08d84-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="08d84-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="08d84-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="08d84-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="08d84-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08d84-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="08d84-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08d84-120">Remarks</span></span>

<span data-ttu-id="08d84-121">Cuando termine, debe liberar el PIDL devuelto con [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span><span class="sxs-lookup"><span data-stu-id="08d84-121">When finished, you should free the returned PIDL with [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="08d84-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08d84-122">Requirements</span></span>



| <span data-ttu-id="08d84-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="08d84-123">Requirement</span></span> | <span data-ttu-id="08d84-124">Value</span><span class="sxs-lookup"><span data-stu-id="08d84-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08d84-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08d84-125">Minimum supported client</span></span><br/> | <span data-ttu-id="08d84-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="08d84-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="08d84-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08d84-127">Minimum supported server</span></span><br/> | <span data-ttu-id="08d84-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08d84-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="08d84-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08d84-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08d84-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08d84-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




