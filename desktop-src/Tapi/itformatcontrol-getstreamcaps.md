---
description: El método GetStreamCaps recupera las capacidades asociadas a un índice de formato determinado.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'ITFormatControl:: GetStreamCaps (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ccaf825912e53eafb5112f14ed369f999959a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690535"
---
# <a name="itformatcontrolgetstreamcaps-method"></a><span data-ttu-id="07b06-103">ITFormatControl:: GetStreamCaps (método)</span><span class="sxs-lookup"><span data-stu-id="07b06-103">ITFormatControl::GetStreamCaps method</span></span>

<span data-ttu-id="07b06-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="07b06-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="07b06-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="07b06-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="07b06-106">El método **GetStreamCaps** recupera las capacidades asociadas a un índice de formato determinado.</span><span class="sxs-lookup"><span data-stu-id="07b06-106">The **GetStreamCaps** method retrieves the capabilities associated with a given format index.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b06-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07b06-107">Syntax</span></span>


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="07b06-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07b06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07b06-109">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="07b06-109">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07b06-110">Índice del formato que se va a sondear.</span><span class="sxs-lookup"><span data-stu-id="07b06-110">Index of the format being probed.</span></span>

</dd> <dt>

<span data-ttu-id="07b06-111">*ppMediaType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="07b06-111">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07b06-112">Puntero a un descriptor de **\_ \_ tipo de medio am** del formato de terminal.</span><span class="sxs-lookup"><span data-stu-id="07b06-112">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="07b06-113">Para obtener más información sobre el **\_ \_ tipo de medio am**, consulte la documentación de DirectX.</span><span class="sxs-lookup"><span data-stu-id="07b06-113">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> <dt>

<span data-ttu-id="07b06-114">*pStreamConfigCaps* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="07b06-114">*pStreamConfigCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07b06-115">Una estructura de [**configuración de secuencia de TAPI \_ \_ \_ Cap**](tapi-stream-config-caps.md) que proporciona información detallada sobre las capacidades de streaming.</span><span class="sxs-lookup"><span data-stu-id="07b06-115">A [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure that gives detailed information concerning stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="07b06-116">*pfEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="07b06-116">*pfEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07b06-117">Indica si el formato asociado al índice actual está habilitado.</span><span class="sxs-lookup"><span data-stu-id="07b06-117">Indicates whether the format associated with the current index is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07b06-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07b06-118">Return value</span></span>

<span data-ttu-id="07b06-119">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="07b06-119">This method can return one of these values.</span></span>



| <span data-ttu-id="07b06-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="07b06-120">Return code</span></span>                                                                                   | <span data-ttu-id="07b06-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="07b06-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="07b06-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="07b06-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="07b06-123">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="07b06-123">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="07b06-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="07b06-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="07b06-125">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="07b06-125">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="07b06-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07b06-126">Requirements</span></span>



| <span data-ttu-id="07b06-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b06-127">Requirement</span></span> | <span data-ttu-id="07b06-128">Value</span><span class="sxs-lookup"><span data-stu-id="07b06-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="07b06-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="07b06-129">TAPI version</span></span><br/> | <span data-ttu-id="07b06-130">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="07b06-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="07b06-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07b06-131">Header</span></span><br/>       | <dl> <span data-ttu-id="07b06-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="07b06-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="07b06-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07b06-133">Library</span></span><br/>      | <dl> <span data-ttu-id="07b06-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07b06-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="07b06-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="07b06-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="07b06-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07b06-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07b06-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="07b06-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b06-138">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="07b06-138">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="07b06-139">**\_Cap de \_ configuración de secuencia TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="07b06-139">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




