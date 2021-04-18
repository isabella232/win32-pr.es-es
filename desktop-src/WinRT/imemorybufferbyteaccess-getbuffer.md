---
description: Obtiene un IMemoryBuffer como una matriz de bytes.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'IMemoryBufferByteAccess:: GetBuffer (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715153"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a><span data-ttu-id="ab920-103">IMemoryBufferByteAccess:: GetBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="ab920-103">IMemoryBufferByteAccess::GetBuffer method</span></span>

<span data-ttu-id="ab920-104">Obtiene un [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) como una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="ab920-104">Gets an [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) as an array of bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab920-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab920-105">Syntax</span></span>


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a><span data-ttu-id="ab920-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab920-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab920-107">*valor* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab920-107">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab920-108">Puntero a una matriz de bytes que contiene los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="ab920-108">A pointer to a byte array containing the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="ab920-109">*capacidad* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab920-109">*capacity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab920-110">Número de bytes de la matriz devuelta</span><span class="sxs-lookup"><span data-stu-id="ab920-110">The number of bytes in the returned array</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab920-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab920-111">Return value</span></span>

<span data-ttu-id="ab920-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ab920-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab920-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab920-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab920-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab920-114">Remarks</span></span>

<span data-ttu-id="ab920-115">Cuando se llama a [**MemoryBuffer:: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) , el código que usa este búfer debe establecer el puntero de *valor* en NULL.</span><span class="sxs-lookup"><span data-stu-id="ab920-115">When [**MemoryBuffer::Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) is called, the code using this buffer should set the *value* pointer to null.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab920-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab920-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab920-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab920-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span></span>
</dt> </dl>

 

 
