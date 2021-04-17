---
description: El método ReleaseFormat libera la estructura asociada con el formato.
ms.assetid: 67181773-5a04-4e20-9814-b004d3b549f5
title: 'ITFormatControl:: ReleaseFormat (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b3eb2a84149054d7ff364cf05290946bca975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690534"
---
# <a name="itformatcontrolreleaseformat-method"></a><span data-ttu-id="ad4d0-103">ITFormatControl:: ReleaseFormat (método)</span><span class="sxs-lookup"><span data-stu-id="ad4d0-103">ITFormatControl::ReleaseFormat method</span></span>

<span data-ttu-id="ad4d0-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ad4d0-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ad4d0-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="ad4d0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ad4d0-106">El método **ReleaseFormat** libera la estructura asociada con el formato.</span><span class="sxs-lookup"><span data-stu-id="ad4d0-106">The **ReleaseFormat** method releases the structure associated with the format.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad4d0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad4d0-107">Syntax</span></span>


```C++
HRESULT ReleaseFormat(
  [in] AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="ad4d0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad4d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad4d0-109">*pMediaType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ad4d0-109">*pMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad4d0-110">Puntero a un descriptor de **\_ \_ tipo de medio am** del formato de terminal.</span><span class="sxs-lookup"><span data-stu-id="ad4d0-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="ad4d0-111">Para obtener más información sobre el **\_ \_ tipo de medio am**, consulte la documentación de DirectX.</span><span class="sxs-lookup"><span data-stu-id="ad4d0-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad4d0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad4d0-112">Return value</span></span>

<span data-ttu-id="ad4d0-113">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ad4d0-113">This method can return one of these values.</span></span>



| <span data-ttu-id="ad4d0-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ad4d0-114">Return code</span></span>                                                                                   | <span data-ttu-id="ad4d0-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad4d0-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ad4d0-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ad4d0-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ad4d0-117">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ad4d0-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ad4d0-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ad4d0-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ad4d0-119">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="ad4d0-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ad4d0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad4d0-120">Requirements</span></span>



| <span data-ttu-id="ad4d0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad4d0-121">Requirement</span></span> | <span data-ttu-id="ad4d0-122">Value</span><span class="sxs-lookup"><span data-stu-id="ad4d0-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ad4d0-123">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ad4d0-123">TAPI version</span></span><br/> | <span data-ttu-id="ad4d0-124">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="ad4d0-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="ad4d0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad4d0-125">Header</span></span><br/>       | <dl> <span data-ttu-id="ad4d0-126"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad4d0-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad4d0-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad4d0-127">Library</span></span><br/>      | <dl> <span data-ttu-id="ad4d0-128"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad4d0-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="ad4d0-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ad4d0-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="ad4d0-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad4d0-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad4d0-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad4d0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad4d0-132">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="ad4d0-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




