---
description: El método GetOutputBuffering recupera el número de fotogramas representados de antemano durante la vista previa.
ms.assetid: 93cb8d18-f1b7-48f9-af41-97f010304b05
title: 'IAMTimelineGroup:: GetOutputBuffering (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8213be882ca445775137a946d9064487b25f48af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691075"
---
# <a name="iamtimelinegroupgetoutputbuffering-method"></a><span data-ttu-id="eebd0-103">IAMTimelineGroup:: GetOutputBuffering (método)</span><span class="sxs-lookup"><span data-stu-id="eebd0-103">IAMTimelineGroup::GetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="eebd0-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="eebd0-104">\[Deprecated.</span></span> <span data-ttu-id="eebd0-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eebd0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eebd0-106">El `GetOutputBuffering` método recupera el número de fotogramas representados de antemano durante la vista previa.</span><span class="sxs-lookup"><span data-stu-id="eebd0-106">The `GetOutputBuffering` method retrieves the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="eebd0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eebd0-107">Syntax</span></span>


```C++
HRESULT GetOutputBuffering(
  [out] int *pnBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="eebd0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eebd0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eebd0-109">*pnBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="eebd0-109">*pnBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eebd0-110">Recibe el número de Marcos almacenados en búfer.</span><span class="sxs-lookup"><span data-stu-id="eebd0-110">Receives the number of buffered frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eebd0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eebd0-111">Return value</span></span>

<span data-ttu-id="eebd0-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="eebd0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eebd0-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eebd0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eebd0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eebd0-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eebd0-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="eebd0-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eebd0-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="eebd0-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eebd0-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="eebd0-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eebd0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eebd0-118">Requirements</span></span>



| <span data-ttu-id="eebd0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eebd0-119">Requirement</span></span> | <span data-ttu-id="eebd0-120">Value</span><span class="sxs-lookup"><span data-stu-id="eebd0-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eebd0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eebd0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="eebd0-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="eebd0-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eebd0-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eebd0-123">Library</span></span><br/> | <dl> <span data-ttu-id="eebd0-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eebd0-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eebd0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="eebd0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eebd0-126">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="eebd0-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="eebd0-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="eebd0-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




