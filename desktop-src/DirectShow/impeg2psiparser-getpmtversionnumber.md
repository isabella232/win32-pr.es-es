---
description: 'Método IMpeg2PsiParser::GetPmtVersionNumber: la implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.'
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: IMpeg2PsiParser::GetPmtVersionNumber (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6f4fd8d0eba88ba1df54a1cc058bc0a2951b9a19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084563"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a><span data-ttu-id="5dd52-104">IMpeg2PsiParser::GetPmtVersionNumber (método)</span><span class="sxs-lookup"><span data-stu-id="5dd52-104">IMpeg2PsiParser::GetPmtVersionNumber method</span></span>

<span data-ttu-id="5dd52-105">La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5dd52-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="5dd52-106">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="5dd52-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="5dd52-107">El `GetPmtVersionNumber` método recupera el campo de número de versión de un \_ PMT especificado.</span><span class="sxs-lookup"><span data-stu-id="5dd52-107">The `GetPmtVersionNumber` method retrieves the version\_number field from a specified PMT.</span></span> <span data-ttu-id="5dd52-108">El número de versión se incrementa cada vez que cambia la definición del programa.</span><span class="sxs-lookup"><span data-stu-id="5dd52-108">The version number is incremented whenever the definition of the program changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dd52-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5dd52-109">Syntax</span></span>


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a><span data-ttu-id="5dd52-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5dd52-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dd52-111">*wProgramNumber* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="5dd52-111">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd52-112">Especifica el campo de \_ número de programa del programa, como se indica en el PAT.</span><span class="sxs-lookup"><span data-stu-id="5dd52-112">Specifies the program\_number field of the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="5dd52-113">*pPmtVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5dd52-113">*pPmtVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5dd52-114">Puntero a una variable que recibe el campo de \_ número de versión.</span><span class="sxs-lookup"><span data-stu-id="5dd52-114">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dd52-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5dd52-115">Return value</span></span>

<span data-ttu-id="5dd52-116">El método devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="5dd52-116">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="5dd52-117">Los valores posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5dd52-117">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="5dd52-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5dd52-118">Return code</span></span>                                                                          | <span data-ttu-id="5dd52-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5dd52-119">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="5dd52-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5dd52-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5dd52-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="5dd52-121">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5dd52-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5dd52-122">Remarks</span></span>

<span data-ttu-id="5dd52-123">Use el **método GetRecordProgramNumber** para obtener el número de programa.</span><span class="sxs-lookup"><span data-stu-id="5dd52-123">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="5dd52-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5dd52-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dd52-125">**IMpeg2PsiParser (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="5dd52-125">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="5dd52-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="5dd52-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="5dd52-127">Ejemplo de filtro del analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="5dd52-127">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




