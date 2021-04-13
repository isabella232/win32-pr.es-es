---
title: IDWriteFactory2 GetSystemFontFallback, método
description: Crea un objeto de reserva de fuente a partir de la lista de reserva del sistema.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Método GetSystemFontFallback de escritura directa
- Método GetSystemFontFallback de escritura directa, interfaz IDWriteFactory2
- Interfaz IDWriteFactory2 Direct Write, método GetSystemFontFallback
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f0eb73ee80dc3e6195267d25f6043225b8613ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421161"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a><span data-ttu-id="ab7be-106">IDWriteFactory2:: GetSystemFontFallback (método)</span><span class="sxs-lookup"><span data-stu-id="ab7be-106">IDWriteFactory2::GetSystemFontFallback method</span></span>

<span data-ttu-id="ab7be-107">Crea un objeto de reserva de fuente a partir de la lista de reserva del sistema.</span><span class="sxs-lookup"><span data-stu-id="ab7be-107">Creates a font fallback object from the system font fallback list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab7be-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab7be-108">Syntax</span></span>


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a><span data-ttu-id="ab7be-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab7be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab7be-110">*fontFallback* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab7be-110">*fontFallback* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab7be-111">Tipo: **[ **IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span><span class="sxs-lookup"><span data-stu-id="ab7be-111">Type: **[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span></span>

<span data-ttu-id="ab7be-112">Contiene una dirección de un puntero al objeto de reserva de fuente recién creado.</span><span class="sxs-lookup"><span data-stu-id="ab7be-112">Contains an address of a pointer to the newly created font fallback object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab7be-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab7be-113">Return value</span></span>

<span data-ttu-id="ab7be-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ab7be-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ab7be-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ab7be-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab7be-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab7be-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab7be-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab7be-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7be-118">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="ab7be-118">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

 