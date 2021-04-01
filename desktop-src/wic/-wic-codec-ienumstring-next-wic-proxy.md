---
description: 'Función de proxy de Windows Imaging Component (WIC) para IEnumString:: Next.'
ms.assetid: a3f6a32b-3043-4bea-a70b-0b4507b4e3a1
title: IEnumString_Next_WIC_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Next_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ae3e25b355268fe63025692bf116b60b45122e76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082091"
---
# <a name="ienumstring_next_wic_proxy-function"></a><span data-ttu-id="d40cf-103">IEnumString \_ siguiente \_ ( \_ función de proxy WIC)</span><span class="sxs-lookup"><span data-stu-id="d40cf-103">IEnumString\_Next\_WIC\_Proxy function</span></span>

<span data-ttu-id="d40cf-104">Función de proxy de Windows Imaging Component (WIC) para IEnumString:: Next.</span><span class="sxs-lookup"><span data-stu-id="d40cf-104">Windows Imaging Component (WIC) proxy function for IEnumString::Next.</span></span>

## <a name="syntax"></a><span data-ttu-id="d40cf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d40cf-105">Syntax</span></span>


```C++
HRESULT IEnumString_Next_WIC_Proxy(
  _In_ IEnumString *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="d40cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d40cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d40cf-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d40cf-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d40cf-108">Tipo: \**IEnumString \** _</span><span class="sxs-lookup"><span data-stu-id="d40cf-108">Type: \**IEnumString\** _</span></span>

<span data-ttu-id="d40cf-109">PARAMDESC</span><span class="sxs-lookup"><span data-stu-id="d40cf-109">PARAMDESC</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d40cf-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d40cf-110">Return value</span></span>

<span data-ttu-id="d40cf-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d40cf-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d40cf-112">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d40cf-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d40cf-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d40cf-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d40cf-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d40cf-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d40cf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d40cf-115">Requirements</span></span>



| <span data-ttu-id="d40cf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d40cf-116">Requirement</span></span> | <span data-ttu-id="d40cf-117">Value</span><span class="sxs-lookup"><span data-stu-id="d40cf-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d40cf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d40cf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d40cf-119">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d40cf-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d40cf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d40cf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d40cf-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d40cf-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d40cf-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d40cf-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d40cf-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d40cf-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




