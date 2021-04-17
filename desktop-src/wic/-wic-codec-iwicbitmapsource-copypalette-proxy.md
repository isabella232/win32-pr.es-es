---
description: Función de proxy para el método CopyPalette.
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: IWICBitmapSource_CopyPalette_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 792738a6be3966e898527c357c99a8cd6c5cfdb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707367"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="51e89-103">Función de proxy de \_ CopyPalette de IWICBitmapSource \_</span><span class="sxs-lookup"><span data-stu-id="51e89-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="51e89-104">Función de proxy para el método [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="51e89-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51e89-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="51e89-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51e89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e89-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="51e89-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e89-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="51e89-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="51e89-109">Puntero a este objeto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="51e89-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="51e89-110">*pIPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="51e89-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e89-111">Tipo: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="51e89-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="51e89-112">Paleta.</span><span class="sxs-lookup"><span data-stu-id="51e89-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e89-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51e89-113">Return value</span></span>

<span data-ttu-id="51e89-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="51e89-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="51e89-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="51e89-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51e89-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51e89-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e89-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51e89-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="51e89-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51e89-118">Requirements</span></span>



| <span data-ttu-id="51e89-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="51e89-119">Requirement</span></span> | <span data-ttu-id="51e89-120">Value</span><span class="sxs-lookup"><span data-stu-id="51e89-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e89-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51e89-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51e89-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51e89-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="51e89-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51e89-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51e89-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="51e89-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="51e89-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="51e89-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51e89-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51e89-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




