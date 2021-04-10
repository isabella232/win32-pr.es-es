---
description: Recupera el PROPVARIANT y la cadena de entrada que representa un fragmento de datos. Llamar a este método es igual que llamar a GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'IRichChunk:: RemoteGetData (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153940"
---
# <a name="irichchunkremotegetdata-method"></a><span data-ttu-id="693a3-104">IRichChunk:: RemoteGetData (método)</span><span class="sxs-lookup"><span data-stu-id="693a3-104">IRichChunk::RemoteGetData method</span></span>

<span data-ttu-id="693a3-105">Recupera el [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) y la cadena de entrada que representa un fragmento de datos.</span><span class="sxs-lookup"><span data-stu-id="693a3-105">Retrieves the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) and input string that represents a chunk of data.</span></span> <span data-ttu-id="693a3-106">Llamar a este método es igual que llamar a [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span><span class="sxs-lookup"><span data-stu-id="693a3-106">Calling this method is the same as calling [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span></span>

## <a name="syntax"></a><span data-ttu-id="693a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="693a3-107">Syntax</span></span>


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="693a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="693a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="693a3-109">*pFirstPos* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="693a3-109">*pFirstPos* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="693a3-110">Recibe la posición inicial de base cero del intervalo.</span><span class="sxs-lookup"><span data-stu-id="693a3-110">Receives the zero-based starting position of the range.</span></span> <span data-ttu-id="693a3-111">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="693a3-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="693a3-112">*plength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="693a3-112">*pLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="693a3-113">Recibe la longitud del intervalo.</span><span class="sxs-lookup"><span data-stu-id="693a3-113">Receives the length of the range.</span></span> <span data-ttu-id="693a3-114">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="693a3-114">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="693a3-115">*ppsz* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="693a3-115">*ppsz* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="693a3-116">Recibe el valor de cadena Unicode asociado o **null** si no está disponible.</span><span class="sxs-lookup"><span data-stu-id="693a3-116">Receives the associated Unicode string value, or **NULL** if not available.</span></span>

</dd> <dt>

<span data-ttu-id="693a3-117">*pValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="693a3-117">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="693a3-118">Recibe el valor de [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) asociado o **VT \_ vacío** si no está disponible.</span><span class="sxs-lookup"><span data-stu-id="693a3-118">Receives the associated [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value, or **VT\_EMPTY** if not available.</span></span> <span data-ttu-id="693a3-119">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="693a3-119">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="693a3-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="693a3-120">Return value</span></span>

<span data-ttu-id="693a3-121">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="693a3-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="693a3-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="693a3-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="693a3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="693a3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="693a3-124">**IRichChunk**</span><span class="sxs-lookup"><span data-stu-id="693a3-124">**IRichChunk**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
