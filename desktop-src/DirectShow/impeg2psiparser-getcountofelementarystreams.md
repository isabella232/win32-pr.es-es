---
description: 'Método IMpeg2PsiParser::GetCountOfElementaryStreams: la implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.'
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: IMpeg2PsiParser::GetCountOfElementaryStreams (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: fc81c0a66751751a73a3895fd31fe8651aee8caf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089163"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a><span data-ttu-id="644bc-104">IMpeg2PsiParser::GetCountOfElementaryStreams (método)</span><span class="sxs-lookup"><span data-stu-id="644bc-104">IMpeg2PsiParser::GetCountOfElementaryStreams method</span></span>

<span data-ttu-id="644bc-105">La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="644bc-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="644bc-106">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="644bc-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="644bc-107">El `GetCountOfElementaryStreams` método recupera el número de secuencias elementales en un programa especificado.</span><span class="sxs-lookup"><span data-stu-id="644bc-107">The `GetCountOfElementaryStreams` method retrieves the number of elementary streams in a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="644bc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="644bc-108">Syntax</span></span>


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="644bc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="644bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="644bc-110">*wProgramNumber* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="644bc-110">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="644bc-111">Especifica el campo de \_ número de programa para el programa, como se indica en el PAT.</span><span class="sxs-lookup"><span data-stu-id="644bc-111">Specifies the program\_number field for the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="644bc-112">*pwVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="644bc-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="644bc-113">Puntero a una variable que recibe el número de secuencias elementales del programa.</span><span class="sxs-lookup"><span data-stu-id="644bc-113">Pointer to a variable that receives the number of elementary streams in the program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="644bc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="644bc-114">Return value</span></span>

<span data-ttu-id="644bc-115">El método devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="644bc-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="644bc-116">Los valores posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="644bc-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="644bc-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="644bc-117">Return code</span></span>                                                                          | <span data-ttu-id="644bc-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="644bc-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="644bc-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="644bc-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="644bc-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="644bc-120">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="644bc-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="644bc-121">Remarks</span></span>

<span data-ttu-id="644bc-122">Use el **método GetRecordProgramNumber** para obtener el número de programa.</span><span class="sxs-lookup"><span data-stu-id="644bc-122">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="644bc-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="644bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="644bc-124">**IMpeg2PsiParser (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="644bc-124">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="644bc-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="644bc-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="644bc-126">Ejemplo de filtro del analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="644bc-126">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




