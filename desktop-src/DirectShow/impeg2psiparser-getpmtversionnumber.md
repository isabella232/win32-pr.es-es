---
description: La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'IMpeg2PsiParser:: GetPmtVersionNumber (método)'
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
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677069"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a><span data-ttu-id="1b5f2-104">IMpeg2PsiParser:: GetPmtVersionNumber (método)</span><span class="sxs-lookup"><span data-stu-id="1b5f2-104">IMpeg2PsiParser::GetPmtVersionNumber method</span></span>

<span data-ttu-id="1b5f2-105">La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1b5f2-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="1b5f2-106">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="1b5f2-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="1b5f2-107">El `GetPmtVersionNumber` método recupera el \_ campo de número de versión de un valor de PMT especificado.</span><span class="sxs-lookup"><span data-stu-id="1b5f2-107">The `GetPmtVersionNumber` method retrieves the version\_number field from a specified PMT.</span></span> <span data-ttu-id="1b5f2-108">El número de versión se incrementa siempre que cambia la definición del programa.</span><span class="sxs-lookup"><span data-stu-id="1b5f2-108">The version number is incremented whenever the definition of the program changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b5f2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b5f2-109">Syntax</span></span>


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a><span data-ttu-id="1b5f2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b5f2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b5f2-111">*wProgramNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1b5f2-111">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b5f2-112">Especifica el \_ campo de número de programa del programa, tal como se indica en el valor de Pat.</span><span class="sxs-lookup"><span data-stu-id="1b5f2-112">Specifies the program\_number field of the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="1b5f2-113">*pPmtVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1b5f2-113">*pPmtVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b5f2-114">Puntero a una variable que recibe el campo de número de versión \_ .</span><span class="sxs-lookup"><span data-stu-id="1b5f2-114">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b5f2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b5f2-115">Return value</span></span>

<span data-ttu-id="1b5f2-116">El método devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b5f2-116">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="1b5f2-117">Entre los valores posibles se incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1b5f2-117">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="1b5f2-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1b5f2-118">Return code</span></span>                                                                          | <span data-ttu-id="1b5f2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b5f2-119">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="1b5f2-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1b5f2-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1b5f2-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1b5f2-121">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1b5f2-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b5f2-122">Remarks</span></span>

<span data-ttu-id="1b5f2-123">Use el método **GetRecordProgramNumber** para obtener el número de programa.</span><span class="sxs-lookup"><span data-stu-id="1b5f2-123">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b5f2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b5f2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b5f2-125">**Interfaz IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="1b5f2-125">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="1b5f2-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="1b5f2-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="1b5f2-127">Ejemplo de filtro de analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="1b5f2-127">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




