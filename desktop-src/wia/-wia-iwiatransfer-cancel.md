---
description: Cancela la operación de transferencia actual.
ms.assetid: 42c6b2c3-7b6a-45d2-a7ce-844e95fe277b
title: 'IWiaTransfer:: CANCEL (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Cancel
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 4764e922498a3c33278555cae37d09c1822959dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541971"
---
# <a name="iwiatransfercancel-method"></a><span data-ttu-id="10c8a-103">IWiaTransfer:: CANCEL (método)</span><span class="sxs-lookup"><span data-stu-id="10c8a-103">IWiaTransfer::Cancel method</span></span>

<span data-ttu-id="10c8a-104">Cancela la operación de transferencia actual.</span><span class="sxs-lookup"><span data-stu-id="10c8a-104">Cancels the current transfer operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10c8a-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="10c8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10c8a-106">Parameters</span></span>

<span data-ttu-id="10c8a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="10c8a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10c8a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10c8a-108">Return value</span></span>

<span data-ttu-id="10c8a-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="10c8a-109">Type: **HRESULT**</span></span>

<span data-ttu-id="10c8a-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="10c8a-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="10c8a-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="10c8a-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="10c8a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10c8a-112">Requirements</span></span>



| <span data-ttu-id="10c8a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="10c8a-113">Requirement</span></span> | <span data-ttu-id="10c8a-114">Value</span><span class="sxs-lookup"><span data-stu-id="10c8a-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10c8a-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10c8a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="10c8a-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="10c8a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="10c8a-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10c8a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="10c8a-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="10c8a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="10c8a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10c8a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="10c8a-120"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="10c8a-120"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="10c8a-121">IDL</span><span class="sxs-lookup"><span data-stu-id="10c8a-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="10c8a-122"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10c8a-122"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="10c8a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="10c8a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="10c8a-124"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10c8a-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




