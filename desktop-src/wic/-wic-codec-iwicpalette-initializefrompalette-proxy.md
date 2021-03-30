---
description: Función de proxy para el método InitializeFromPalette.
ms.assetid: e7156cae-8d59-4dbd-8845-0e892e10107b
title: IWICPalette_InitializeFromPalette_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 130c135d3c32135aeefd25fe8799e50c0b5ec855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912626"
---
# <a name="iwicpalette_initializefrompalette_proxy-function"></a><span data-ttu-id="49973-103">IWICPalette \_ InitializeFromPalette \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="49973-103">IWICPalette\_InitializeFromPalette\_Proxy function</span></span>

<span data-ttu-id="49973-104">Función de proxy para el método [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) .</span><span class="sxs-lookup"><span data-stu-id="49973-104">Proxy function for the [**InitializeFromPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrompalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="49973-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49973-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromPalette_Proxy(
  _In_ IWICPalette *THIS_PTR,
  _In_ IWICPalette *pIMILPalette
);
```



## <a name="parameters"></a><span data-ttu-id="49973-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49973-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49973-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="49973-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49973-108">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="49973-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="49973-109">Puntero a este objeto [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="49973-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="49973-110">*pIMILPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49973-110">*pIMILPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49973-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="49973-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="49973-112">Puntero a la paleta de origen.</span><span class="sxs-lookup"><span data-stu-id="49973-112">Pointer to the source palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49973-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49973-113">Return value</span></span>

<span data-ttu-id="49973-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="49973-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="49973-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="49973-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49973-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="49973-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="49973-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49973-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="49973-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49973-118">Requirements</span></span>



| <span data-ttu-id="49973-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="49973-119">Requirement</span></span> | <span data-ttu-id="49973-120">Value</span><span class="sxs-lookup"><span data-stu-id="49973-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49973-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49973-121">Minimum supported client</span></span><br/> | <span data-ttu-id="49973-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49973-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="49973-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49973-123">Minimum supported server</span></span><br/> | <span data-ttu-id="49973-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="49973-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="49973-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49973-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49973-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49973-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




