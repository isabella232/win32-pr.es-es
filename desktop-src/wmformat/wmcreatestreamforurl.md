---
title: WMCreateStreamForURL función)
description: La aplicación implementa la función WMCreateStreamForURL para crear un objeto IStream COM para una dirección URL determinada.
ms.assetid: df8d0e57-9f71-4be3-a0b0-cf61b68611bc
keywords:
- Función WMCreateStreamForURL formato de Windows Media
topic_type:
- apiref
api_name:
- WMCreateStreamForURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05fddd6d5359f1eada6a2691b51a692217d4a9dd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419603"
---
# <a name="wmcreatestreamforurl-function"></a><span data-ttu-id="a5420-104">WMCreateStreamForURL función)</span><span class="sxs-lookup"><span data-stu-id="a5420-104">WMCreateStreamForURL function</span></span>

<span data-ttu-id="a5420-105">La aplicación implementa la función **WMCreateStreamForURL** para crear un objeto **IStream** com para una dirección URL determinada.</span><span class="sxs-lookup"><span data-stu-id="a5420-105">The **WMCreateStreamForURL** function is implemented by the application to create a COM **IStream** object for a given URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5420-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5420-106">Syntax</span></span>


```C++
HRESULT WMCreateStreamForURL(
  _In_  LPCWSTR pwszURL,
  _Out_ BOOL    *pfCorrectSource,
  _Out_ IStream **ppStream
);
```



## <a name="parameters"></a><span data-ttu-id="a5420-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5420-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5420-108">*pwszURL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a5420-108">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5420-109">Puntero a una cadena de caracteres anchos que contiene la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="a5420-109">Pointer to a wide-character string containing the URL.</span></span>

</dd> <dt>

<span data-ttu-id="a5420-110">*pfCorrectSource* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a5420-110">*pfCorrectSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5420-111">Puntero a una marca, true impedirá que el SDK intente otros complementos de origen para esta dirección URL.</span><span class="sxs-lookup"><span data-stu-id="a5420-111">Pointer to a flag, true will prevent the SDK from trying other source plug-ins for this URL.</span></span>

</dd> <dt>

<span data-ttu-id="a5420-112">*ppStream* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a5420-112">*ppStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5420-113">Puntero a un puntero al objeto **IStream** creado por el método.</span><span class="sxs-lookup"><span data-stu-id="a5420-113">Pointer to a pointer to the **IStream** object created by the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5420-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5420-114">Return value</span></span>

<span data-ttu-id="a5420-115">Si la función se ejecuta correctamente, debe devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a5420-115">If the function succeeds, it must return S\_OK.</span></span> <span data-ttu-id="a5420-116">Si se produce un error, debe devolver un código de error **HRESULT** adecuado y \* *ppStream* debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="a5420-116">If it fails, it must return an appropriate **HRESULT** error code, and \**ppStream* should be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5420-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5420-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5420-118">**Complementos de origen**</span><span class="sxs-lookup"><span data-stu-id="a5420-118">**Source Plug-ins**</span></span>](source-plug-ins.md)
</dt> </dl>

 

 




