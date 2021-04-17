---
description: La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'IMpeg2PsiParser:: GetCountOfElementaryStreams (método)'
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
ms.openlocfilehash: 6593b699592c913940b14c2c26aea42057acfa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677071"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a><span data-ttu-id="60bda-104">IMpeg2PsiParser:: GetCountOfElementaryStreams (método)</span><span class="sxs-lookup"><span data-stu-id="60bda-104">IMpeg2PsiParser::GetCountOfElementaryStreams method</span></span>

<span data-ttu-id="60bda-105">La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="60bda-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="60bda-106">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="60bda-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="60bda-107">El `GetCountOfElementaryStreams` método recupera el número de flujos elementales en un programa especificado.</span><span class="sxs-lookup"><span data-stu-id="60bda-107">The `GetCountOfElementaryStreams` method retrieves the number of elementary streams in a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="60bda-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60bda-108">Syntax</span></span>


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="60bda-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60bda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60bda-110">*wProgramNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60bda-110">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60bda-111">Especifica el \_ campo de número de programa para el programa, como se indica en el valor de Pat.</span><span class="sxs-lookup"><span data-stu-id="60bda-111">Specifies the program\_number field for the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="60bda-112">*pwVal* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60bda-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60bda-113">Puntero a una variable que recibe el número de flujos elementales del programa.</span><span class="sxs-lookup"><span data-stu-id="60bda-113">Pointer to a variable that receives the number of elementary streams in the program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60bda-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60bda-114">Return value</span></span>

<span data-ttu-id="60bda-115">El método devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="60bda-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="60bda-116">Entre los valores posibles se incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="60bda-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="60bda-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="60bda-117">Return code</span></span>                                                                          | <span data-ttu-id="60bda-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="60bda-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="60bda-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="60bda-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="60bda-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="60bda-120">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60bda-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60bda-121">Remarks</span></span>

<span data-ttu-id="60bda-122">Use el método **GetRecordProgramNumber** para obtener el número de programa.</span><span class="sxs-lookup"><span data-stu-id="60bda-122">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="60bda-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="60bda-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60bda-124">**Interfaz IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="60bda-124">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="60bda-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="60bda-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="60bda-126">Ejemplo de filtro de analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="60bda-126">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




