---
description: 'Método IMpeg2PsiParser::GetPatVersionNumber: la implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.'
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: IMpeg2PsiParser::GetPatVersionNumber (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 978da4c7076bcf8ffe91bc2b9a4b2077d9d3d48a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089153"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a><span data-ttu-id="679fd-104">IMpeg2PsiParser::GetPatVersionNumber (método)</span><span class="sxs-lookup"><span data-stu-id="679fd-104">IMpeg2PsiParser::GetPatVersionNumber method</span></span>

<span data-ttu-id="679fd-105">La implementación de este método se proporciona como código de ejemplo con el SDK de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="679fd-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="679fd-106">No es una API de DirectShow compatible.</span><span class="sxs-lookup"><span data-stu-id="679fd-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="679fd-107">El `GetPatVersionNumber` método recupera el campo de número de versión del \_ PAT.</span><span class="sxs-lookup"><span data-stu-id="679fd-107">The `GetPatVersionNumber` method retrieves the version\_number field from the PAT.</span></span> <span data-ttu-id="679fd-108">Una secuencia de transporte contiene como máximo un PAT.</span><span class="sxs-lookup"><span data-stu-id="679fd-108">A transport stream contains at most one PAT.</span></span> <span data-ttu-id="679fd-109">El número de versión se incrementa cada vez que cambia la información de la tabla.</span><span class="sxs-lookup"><span data-stu-id="679fd-109">The version number is incremented whenever the information in the table changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="679fd-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="679fd-110">Syntax</span></span>


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a><span data-ttu-id="679fd-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="679fd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="679fd-112">*pPatVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="679fd-112">*pPatVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="679fd-113">Puntero a una variable que recibe el campo de \_ número de versión.</span><span class="sxs-lookup"><span data-stu-id="679fd-113">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="679fd-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="679fd-114">Return value</span></span>

<span data-ttu-id="679fd-115">El método devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="679fd-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="679fd-116">Los valores posibles incluyen, entre otros, los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="679fd-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="679fd-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="679fd-117">Return code</span></span>                                                                          | <span data-ttu-id="679fd-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="679fd-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="679fd-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="679fd-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="679fd-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="679fd-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="679fd-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="679fd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="679fd-122">**IMpeg2PsiParser (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="679fd-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="679fd-123">Ejemplo de filtro del analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="679fd-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




