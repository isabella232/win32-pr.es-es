---
description: 'Método IMpeg2PsiParser::GetRecordProgramNumber: la implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.'
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: IMpeg2PsiParser::GetRecordProgramNumber (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0fd99178edaa23f2cdf32672a746f79c368b4265
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089143"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a><span data-ttu-id="dc221-104">IMpeg2PsiParser::GetRecordProgramNumber (método)</span><span class="sxs-lookup"><span data-stu-id="dc221-104">IMpeg2PsiParser::GetRecordProgramNumber method</span></span>

<span data-ttu-id="dc221-105">La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="dc221-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="dc221-106">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="dc221-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="dc221-107">El `GetRecordProgramNumber` método recupera el número de programa para un programa especificado.</span><span class="sxs-lookup"><span data-stu-id="dc221-107">The `GetRecordProgramNumber` method retrieves the program number for a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc221-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc221-108">Syntax</span></span>


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="dc221-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc221-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc221-110">*dwIndex* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="dc221-110">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc221-111">Especifica la entrada en el PAT que define el programa, indizado desde cero.</span><span class="sxs-lookup"><span data-stu-id="dc221-111">Specifies the entry in the PAT that defines the program, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="dc221-112">*pwVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dc221-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc221-113">Puntero a una variable que recibe el campo \_ de número de programa del PAT.</span><span class="sxs-lookup"><span data-stu-id="dc221-113">Pointer to a variable that receives the program\_number field from the PAT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc221-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc221-114">Return value</span></span>

<span data-ttu-id="dc221-115">El método devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="dc221-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="dc221-116">Los valores posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dc221-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="dc221-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dc221-117">Return code</span></span>                                                                          | <span data-ttu-id="dc221-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc221-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="dc221-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dc221-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dc221-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="dc221-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="dc221-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dc221-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc221-122">**IMpeg2PsiParser (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="dc221-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="dc221-123">Ejemplo de filtro del analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="dc221-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




