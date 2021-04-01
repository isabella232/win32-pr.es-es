---
description: La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: 'IMpeg2PsiParser:: GetCountOfPrograms (método)'
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
ms.openlocfilehash: e4f01b2a360465b9670b52547cff1ff4c312a705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906708"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a><span data-ttu-id="cc794-104">IMpeg2PsiParser:: GetCountOfPrograms (método)</span><span class="sxs-lookup"><span data-stu-id="cc794-104">IMpeg2PsiParser::GetCountOfPrograms method</span></span>

<span data-ttu-id="cc794-105">La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cc794-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="cc794-106">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="cc794-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="cc794-107">El `GetCountOfPrograms` método recupera el número de programas en el flujo de transporte.</span><span class="sxs-lookup"><span data-stu-id="cc794-107">The `GetCountOfPrograms` method retrieves the number of programs in the transport stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc794-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc794-108">Syntax</span></span>


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a><span data-ttu-id="cc794-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc794-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc794-110">*pNumOfPrograms* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cc794-110">*pNumOfPrograms* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc794-111">Puntero a una variable que recibe el número de programas.</span><span class="sxs-lookup"><span data-stu-id="cc794-111">Pointer to a variable that receives the number of programs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc794-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc794-112">Return value</span></span>

<span data-ttu-id="cc794-113">El método devuelve un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="cc794-113">The method returns an HRESULT value.</span></span> <span data-ttu-id="cc794-114">Entre los valores posibles se incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cc794-114">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="cc794-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cc794-115">Return code</span></span>                                                                          | <span data-ttu-id="cc794-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc794-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="cc794-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="cc794-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cc794-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="cc794-118">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="cc794-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc794-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc794-120">**Interfaz IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="cc794-120">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="cc794-121">Ejemplo de filtro de analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="cc794-121">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




