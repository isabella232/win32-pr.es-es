---
description: Recupera las características de la fuente.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'ID3DX10Font:: GetTextMetrics (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72decdcf0a9573f7ad8ba0f4e363df6df3599477
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547942"
---
# <a name="id3dx10fontgettextmetrics-method"></a><span data-ttu-id="f05f2-103">ID3DX10Font:: GetTextMetrics (método)</span><span class="sxs-lookup"><span data-stu-id="f05f2-103">ID3DX10Font::GetTextMetrics method</span></span>

<span data-ttu-id="f05f2-104">Recupera las características de la fuente.</span><span class="sxs-lookup"><span data-stu-id="f05f2-104">Retrieve font characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="f05f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f05f2-105">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="f05f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f05f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f05f2-107">*pTextMetrics* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f05f2-107">*pTextMetrics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f05f2-108">Tipo: **TEXTMETRIC \***</span><span class="sxs-lookup"><span data-stu-id="f05f2-108">Type: **TEXTMETRIC\***</span></span>

<span data-ttu-id="f05f2-109">Puntero a una estructura [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) , que contiene las propiedades de fuente.</span><span class="sxs-lookup"><span data-stu-id="f05f2-109">Pointer to a [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) structure, which contains font properties.</span></span> <span data-ttu-id="f05f2-110">Si se define Unicode, la función devuelve una estructura TEXTMETRICW.</span><span class="sxs-lookup"><span data-stu-id="f05f2-110">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="f05f2-111">De lo contrario, la función devuelve una estructura TEXTMETRICA.</span><span class="sxs-lookup"><span data-stu-id="f05f2-111">Otherwise, the function returns a TEXTMETRICA structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f05f2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f05f2-112">Return value</span></span>

<span data-ttu-id="f05f2-113">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f05f2-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f05f2-114">Es distinto de cero si la función se realiza correctamente; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="f05f2-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f05f2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f05f2-115">Requirements</span></span>



| <span data-ttu-id="f05f2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f05f2-116">Requirement</span></span> | <span data-ttu-id="f05f2-117">Value</span><span class="sxs-lookup"><span data-stu-id="f05f2-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f05f2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f05f2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f05f2-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f05f2-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f05f2-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f05f2-120">Library</span></span><br/> | <dl> <span data-ttu-id="f05f2-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f05f2-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f05f2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f05f2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f05f2-123">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="f05f2-123">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="f05f2-124">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="f05f2-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
