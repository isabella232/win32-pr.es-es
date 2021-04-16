---
description: La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'IMpeg2PsiParser:: GetRecordProgramNumber (método)'
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
ms.openlocfilehash: 2bedc5922ce90fa2fda612f30571f884e75841d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677068"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a><span data-ttu-id="9973a-104">IMpeg2PsiParser:: GetRecordProgramNumber (método)</span><span class="sxs-lookup"><span data-stu-id="9973a-104">IMpeg2PsiParser::GetRecordProgramNumber method</span></span>

<span data-ttu-id="9973a-105">La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9973a-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="9973a-106">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="9973a-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="9973a-107">El `GetRecordProgramNumber` método recupera el número de programa para un programa especificado.</span><span class="sxs-lookup"><span data-stu-id="9973a-107">The `GetRecordProgramNumber` method retrieves the program number for a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="9973a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9973a-108">Syntax</span></span>


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="9973a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9973a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9973a-110">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9973a-110">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9973a-111">Especifica la entrada de PAT que define el programa, indizada desde cero.</span><span class="sxs-lookup"><span data-stu-id="9973a-111">Specifies the entry in the PAT that defines the program, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="9973a-112">*pwVal* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9973a-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9973a-113">Puntero a una variable que recibe el \_ campo de número de programa de la Pat.</span><span class="sxs-lookup"><span data-stu-id="9973a-113">Pointer to a variable that receives the program\_number field from the PAT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9973a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9973a-114">Return value</span></span>

<span data-ttu-id="9973a-115">El método devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9973a-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="9973a-116">Entre los valores posibles se incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9973a-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="9973a-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9973a-117">Return code</span></span>                                                                          | <span data-ttu-id="9973a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="9973a-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="9973a-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9973a-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9973a-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="9973a-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9973a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9973a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9973a-122">**Interfaz IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="9973a-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="9973a-123">Ejemplo de filtro de analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="9973a-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




