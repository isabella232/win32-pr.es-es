---
description: El método GetGroupCount recupera el número de grupos contenidos en la escala de tiempo.
ms.assetid: 24351e03-3132-4363-8171-eae517fb770a
title: 'IAMTimeline:: GetGroupCount (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroupCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4d16cf44839b05f39bc747cb89eda77842caa04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653831"
---
# <a name="iamtimelinegetgroupcount-method"></a><span data-ttu-id="3f2c2-103">IAMTimeline:: GetGroupCount (método)</span><span class="sxs-lookup"><span data-stu-id="3f2c2-103">IAMTimeline::GetGroupCount method</span></span>

> [!Note]  
> <span data-ttu-id="3f2c2-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3f2c2-104">\[Deprecated.</span></span> <span data-ttu-id="3f2c2-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3f2c2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3f2c2-106">El `GetGroupCount` método recupera el número de grupos contenidos en la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3f2c2-106">The `GetGroupCount` method retrieves the number of groups that are contained in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f2c2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f2c2-107">Syntax</span></span>


```C++
HRESULT GetGroupCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="3f2c2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f2c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f2c2-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="3f2c2-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="3f2c2-110">Recibe el número de grupos de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="3f2c2-110">Receives the number of groups in the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f2c2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f2c2-111">Return value</span></span>

<span data-ttu-id="3f2c2-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3f2c2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f2c2-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f2c2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f2c2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f2c2-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3f2c2-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="3f2c2-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3f2c2-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f2c2-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3f2c2-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3f2c2-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f2c2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f2c2-118">Requirements</span></span>



| <span data-ttu-id="3f2c2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f2c2-119">Requirement</span></span> | <span data-ttu-id="3f2c2-120">Value</span><span class="sxs-lookup"><span data-stu-id="3f2c2-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f2c2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f2c2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3f2c2-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f2c2-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3f2c2-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f2c2-123">Library</span></span><br/> | <dl> <span data-ttu-id="3f2c2-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f2c2-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f2c2-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f2c2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f2c2-126">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="3f2c2-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="3f2c2-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="3f2c2-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




