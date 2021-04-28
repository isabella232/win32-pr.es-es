---
description: 'Método IMpeg2PsiParser::GetCountOfPrograms: la implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.'
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: IMpeg2PsiParser::GetCountOfPrograms (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: d6bfe698a45ea1cfe0a4bac6e65b839292bc1996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119433"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a><span data-ttu-id="0f2e3-104">IMpeg2PsiParser::GetCountOfPrograms (método)</span><span class="sxs-lookup"><span data-stu-id="0f2e3-104">IMpeg2PsiParser::GetCountOfPrograms method</span></span>

<span data-ttu-id="0f2e3-105">La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="0f2e3-106">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="0f2e3-107">El `GetCountOfPrograms` método recupera el número de programas de la secuencia de transporte.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-107">The `GetCountOfPrograms` method retrieves the number of programs in the transport stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f2e3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f2e3-108">Syntax</span></span>


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a><span data-ttu-id="0f2e3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f2e3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f2e3-110">*pNumOfPrograms* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0f2e3-110">*pNumOfPrograms* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f2e3-111">Puntero a una variable que recibe el número de programas.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-111">Pointer to a variable that receives the number of programs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f2e3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-112">Return value</span></span>

<span data-ttu-id="0f2e3-113">El método devuelve un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-113">The method returns an HRESULT value.</span></span> <span data-ttu-id="0f2e3-114">Los valores posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-114">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="0f2e3-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0f2e3-115">Return code</span></span>                                                                          | <span data-ttu-id="0f2e3-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f2e3-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="0f2e3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f2e3-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0f2e3-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0f2e3-118">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="0f2e3-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0f2e3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f2e3-120">**IMpeg2PsiParser (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="0f2e3-120">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="0f2e3-121">Ejemplo de filtro del analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="0f2e3-121">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




