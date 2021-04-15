---
description: Crea un objeto de transformación de color que implementa IWICColorTransform. Este objeto COM admite el modelo de objetos de subprocesamiento libre.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: WICCreateColorTransform_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708267"
---
# <a name="wiccreatecolortransform_proxy-function"></a><span data-ttu-id="09fc3-104">\_Función de proxy WICCreateColorTransform</span><span class="sxs-lookup"><span data-stu-id="09fc3-104">WICCreateColorTransform\_Proxy function</span></span>

<span data-ttu-id="09fc3-105">Crea un objeto de transformación de color que implementa [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span><span class="sxs-lookup"><span data-stu-id="09fc3-105">Creates an color transform object that implements [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span></span> <span data-ttu-id="09fc3-106">Este objeto COM admite el modelo de objetos de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="09fc3-106">This COM object supports the free-threaded object model.</span></span>

## <a name="syntax"></a><span data-ttu-id="09fc3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09fc3-107">Syntax</span></span>


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a><span data-ttu-id="09fc3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09fc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09fc3-109">*ppIColorTransform* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="09fc3-109">*ppIColorTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09fc3-110">La transformación de color creada.</span><span class="sxs-lookup"><span data-stu-id="09fc3-110">The color transform created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09fc3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09fc3-111">Return value</span></span>

<span data-ttu-id="09fc3-112">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="09fc3-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="09fc3-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09fc3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="09fc3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09fc3-114">Requirements</span></span>



| <span data-ttu-id="09fc3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="09fc3-115">Requirement</span></span> | <span data-ttu-id="09fc3-116">Value</span><span class="sxs-lookup"><span data-stu-id="09fc3-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09fc3-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09fc3-117">DLL</span></span><br/> | <dl> <span data-ttu-id="09fc3-118"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09fc3-118"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 
