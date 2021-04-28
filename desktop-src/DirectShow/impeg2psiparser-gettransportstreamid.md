---
description: 'Método IMpeg2PsiParser::GetTransportStreamId: la implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.'
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: IMpeg2PsiParser::GetTransportStreamId (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: a24253b021abacf398a3a169b63bbb2f01ec2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084573"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a><span data-ttu-id="6f297-104">IMpeg2PsiParser::GetTransportStreamId (método)</span><span class="sxs-lookup"><span data-stu-id="6f297-104">IMpeg2PsiParser::GetTransportStreamId method</span></span>

<span data-ttu-id="6f297-105">La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6f297-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="6f297-106">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="6f297-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="6f297-107">El `GetTransportStreamId` método recupera el campo de identificador de flujo de transporte del \_ \_ PAT.</span><span class="sxs-lookup"><span data-stu-id="6f297-107">The `GetTransportStreamId` method retrieves the transport\_stream\_id field from the PAT.</span></span> <span data-ttu-id="6f297-108">El usuario define este valor y se puede usar para distinguir una secuencia de transporte determinada de otras secuencias de la misma red.</span><span class="sxs-lookup"><span data-stu-id="6f297-108">This value is defined by the user, and can be used to distinguish a particular transport stream from other streams on the same network.</span></span> <span data-ttu-id="6f297-109">Una secuencia de transporte contiene como máximo un PAT.</span><span class="sxs-lookup"><span data-stu-id="6f297-109">A transport stream contains at most one PAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f297-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f297-110">Syntax</span></span>


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a><span data-ttu-id="6f297-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f297-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f297-112">*pStreamId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6f297-112">*pStreamId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f297-113">Puntero a una variable que recibe el campo de identificador \_ de flujo \_ de transporte.</span><span class="sxs-lookup"><span data-stu-id="6f297-113">Pointer to a variable that receives the transport\_stream\_id field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f297-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f297-114">Return value</span></span>

<span data-ttu-id="6f297-115">El método devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="6f297-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="6f297-116">Los valores posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6f297-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="6f297-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6f297-117">Return code</span></span>                                                                          | <span data-ttu-id="6f297-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f297-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="6f297-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6f297-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6f297-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6f297-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6f297-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6f297-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f297-122">**IMpeg2PsiParser (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="6f297-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="6f297-123">Ejemplo de filtro del analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="6f297-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




