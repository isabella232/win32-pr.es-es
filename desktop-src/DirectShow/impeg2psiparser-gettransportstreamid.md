---
description: La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: 'IMpeg2PsiParser:: GetTransportStreamId (método)'
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
ms.openlocfilehash: 9615c50d8d16aa6d78e3e1b83a3ec0e356c6cb50
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677169"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a><span data-ttu-id="073bc-104">IMpeg2PsiParser:: GetTransportStreamId (método)</span><span class="sxs-lookup"><span data-stu-id="073bc-104">IMpeg2PsiParser::GetTransportStreamId method</span></span>

<span data-ttu-id="073bc-105">La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="073bc-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="073bc-106">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="073bc-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="073bc-107">El `GetTransportStreamId` método recupera el \_ \_ campo de identificador de flujo de transporte de la Pat.</span><span class="sxs-lookup"><span data-stu-id="073bc-107">The `GetTransportStreamId` method retrieves the transport\_stream\_id field from the PAT.</span></span> <span data-ttu-id="073bc-108">Este valor lo define el usuario y se puede usar para distinguir un flujo de transporte determinado de otras secuencias de la misma red.</span><span class="sxs-lookup"><span data-stu-id="073bc-108">This value is defined by the user, and can be used to distinguish a particular transport stream from other streams on the same network.</span></span> <span data-ttu-id="073bc-109">Un flujo de transporte contiene como máximo una PAT.</span><span class="sxs-lookup"><span data-stu-id="073bc-109">A transport stream contains at most one PAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="073bc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="073bc-110">Syntax</span></span>


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a><span data-ttu-id="073bc-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="073bc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="073bc-112">*pStreamId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="073bc-112">*pStreamId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="073bc-113">Puntero a una variable que recibe el campo de identificador de flujo de transporte \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="073bc-113">Pointer to a variable that receives the transport\_stream\_id field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="073bc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="073bc-114">Return value</span></span>

<span data-ttu-id="073bc-115">El método devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="073bc-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="073bc-116">Entre los valores posibles se incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="073bc-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="073bc-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="073bc-117">Return code</span></span>                                                                          | <span data-ttu-id="073bc-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="073bc-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="073bc-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="073bc-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="073bc-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="073bc-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="073bc-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="073bc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="073bc-122">**Interfaz IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="073bc-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="073bc-123">Ejemplo de filtro de analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="073bc-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




