---
description: Indica que ha finalizado una búsqueda.
title: IShellFolderSearchableCallback::RunEnd (Método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunEnd
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91700764-6cdf-488d-adc0-e34d9b4cb71d
ms.openlocfilehash: c23d461fdbd175a80a8fa94fcc238f6cf2f89869
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842826"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="456e4-103">IShellFolderSearchableCallback::RunEnd (Método)</span><span class="sxs-lookup"><span data-stu-id="456e4-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="456e4-104">Indica que ha finalizado una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="456e4-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="456e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="456e4-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="456e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="456e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="456e4-107">*dwReserved* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="456e4-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="456e4-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="456e4-108">Type: **DWORD**</span></span>

<span data-ttu-id="456e4-109">Reservado.</span><span class="sxs-lookup"><span data-stu-id="456e4-109">Reserved.</span></span> <span data-ttu-id="456e4-110">Se debe establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="456e4-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="456e4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="456e4-111">Return value</span></span>

<span data-ttu-id="456e4-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="456e4-112">Type: **HRESULT**</span></span>

<span data-ttu-id="456e4-113">Si este método se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="456e4-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="456e4-114">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="456e4-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="456e4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="456e4-115">Requirements</span></span>



| <span data-ttu-id="456e4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="456e4-116">Requirement</span></span> | <span data-ttu-id="456e4-117">Value</span><span class="sxs-lookup"><span data-stu-id="456e4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="456e4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="456e4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="456e4-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="456e4-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="456e4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="456e4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="456e4-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="456e4-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="456e4-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="456e4-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="456e4-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="456e4-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




