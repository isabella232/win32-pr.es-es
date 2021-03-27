---
description: Indica que ha finalizado una búsqueda.
title: 'IShellFolderSearchableCallback:: RunEnd (método)'
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
ms.openlocfilehash: 73155e65f4b6edb4a4b4b9b0d52ab5b042fa68b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997444"
---
# <a name="ishellfoldersearchablecallbackrunend-method"></a><span data-ttu-id="5ae79-103">IShellFolderSearchableCallback:: RunEnd (método)</span><span class="sxs-lookup"><span data-stu-id="5ae79-103">IShellFolderSearchableCallback::RunEnd method</span></span>

<span data-ttu-id="5ae79-104">Indica que ha finalizado una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5ae79-104">Indicates that a search has finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae79-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ae79-105">Syntax</span></span>


```C++
HRESULT RunEnd(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="5ae79-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ae79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ae79-107">*dwReserved* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ae79-107">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae79-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5ae79-108">Type: **DWORD**</span></span>

<span data-ttu-id="5ae79-109">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5ae79-109">Reserved.</span></span> <span data-ttu-id="5ae79-110">Se debe establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="5ae79-110">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ae79-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ae79-111">Return value</span></span>

<span data-ttu-id="5ae79-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5ae79-112">Type: **HRESULT**</span></span>

<span data-ttu-id="5ae79-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5ae79-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5ae79-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5ae79-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ae79-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ae79-115">Requirements</span></span>



| <span data-ttu-id="5ae79-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ae79-116">Requirement</span></span> | <span data-ttu-id="5ae79-117">Value</span><span class="sxs-lookup"><span data-stu-id="5ae79-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae79-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ae79-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5ae79-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5ae79-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5ae79-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ae79-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5ae79-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5ae79-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5ae79-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ae79-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ae79-123"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ae79-123"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




