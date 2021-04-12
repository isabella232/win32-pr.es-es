---
description: Obtiene el resultado de una acción asincrónica.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: 'IAsyncAction:: GetResults (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 292c73846227f1bb8884b24b7e709bc6b2296e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275413"
---
# <a name="iasyncactiongetresults-method"></a><span data-ttu-id="25e05-103">IAsyncAction:: GetResults (método)</span><span class="sxs-lookup"><span data-stu-id="25e05-103">IAsyncAction::GetResults method</span></span>

<span data-ttu-id="25e05-104">Obtiene el resultado de una acción asincrónica.</span><span class="sxs-lookup"><span data-stu-id="25e05-104">Gets the outcome of an asynchronous action.</span></span>

## <a name="syntax"></a><span data-ttu-id="25e05-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25e05-105">Syntax</span></span>


```C++
HRESULT GetResults();
```



## <a name="parameters"></a><span data-ttu-id="25e05-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25e05-106">Parameters</span></span>

<span data-ttu-id="25e05-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="25e05-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25e05-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25e05-108">Return value</span></span>

<span data-ttu-id="25e05-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="25e05-109">Type: **HRESULT**</span></span>

<span data-ttu-id="25e05-110">Este método siempre devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="25e05-110">This method always returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="25e05-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25e05-111">Remarks</span></span>

<span data-ttu-id="25e05-112">La llamada al método **GetResults** no tiene ningún efecto si la implementación actual tiene un tipo dinámico de [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span><span class="sxs-lookup"><span data-stu-id="25e05-112">Calling the **GetResults** method has no effect if the current implementation has a dynamic type of [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span></span>

## <a name="requirements"></a><span data-ttu-id="25e05-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25e05-113">Requirements</span></span>



| <span data-ttu-id="25e05-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="25e05-114">Requirement</span></span> | <span data-ttu-id="25e05-115">Value</span><span class="sxs-lookup"><span data-stu-id="25e05-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25e05-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25e05-116">Minimum supported client</span></span><br/> | <span data-ttu-id="25e05-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="25e05-117">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="25e05-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25e05-118">Minimum supported server</span></span><br/> | <span data-ttu-id="25e05-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="25e05-119">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="25e05-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25e05-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="25e05-121"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25e05-121"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e05-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="25e05-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e05-123">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="25e05-123">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
