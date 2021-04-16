---
description: La interfaz IAMTimelineSplittable divide un objeto Timeline en los servicios de edición de DirectShow (DES). Los orígenes, los efectos, las transiciones y las pistas implementan esta interfaz.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Interfaz IAMTimelineSplittable (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689968"
---
# <a name="iamtimelinesplittable-interface"></a><span data-ttu-id="4a132-104">Interfaz IAMTimelineSplittable</span><span class="sxs-lookup"><span data-stu-id="4a132-104">IAMTimelineSplittable interface</span></span>

> [!Note]  
> <span data-ttu-id="4a132-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4a132-105">\[Deprecated.</span></span> <span data-ttu-id="4a132-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a132-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a132-107">La `IAMTimelineSplittable` interfaz divide un objeto Timeline en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="4a132-107">The `IAMTimelineSplittable` interface splits a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="4a132-108">Los orígenes, los efectos, las transiciones y las pistas implementan esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="4a132-108">Sources, effects, transitions, and tracks implement this interface.</span></span>

## <a name="members"></a><span data-ttu-id="4a132-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4a132-109">Members</span></span>

<span data-ttu-id="4a132-110">La interfaz **IAMTimelineSplittable** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4a132-110">The **IAMTimelineSplittable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4a132-111">**IAMTimelineSplittable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4a132-111">**IAMTimelineSplittable** also has these types of members:</span></span>

-   [<span data-ttu-id="4a132-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a132-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4a132-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a132-113">Methods</span></span>

<span data-ttu-id="4a132-114">La interfaz **IAMTimelineSplittable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4a132-114">The **IAMTimelineSplittable** interface has these methods.</span></span>



| <span data-ttu-id="4a132-115">Método</span><span class="sxs-lookup"><span data-stu-id="4a132-115">Method</span></span>                                             | <span data-ttu-id="4a132-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a132-116">Description</span></span>                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a132-117">**SplitAt**</span><span class="sxs-lookup"><span data-stu-id="4a132-117">**SplitAt**</span></span>](iamtimelinesplittable-splitat.md)   | <span data-ttu-id="4a132-118">Divide el objeto en el momento especificado.</span><span class="sxs-lookup"><span data-stu-id="4a132-118">Splits the object at the specified time.</span></span><br/>                                                  |
| [<span data-ttu-id="4a132-119">**SplitAt2**</span><span class="sxs-lookup"><span data-stu-id="4a132-119">**SplitAt2**</span></span>](iamtimelinesplittable-splitat2.md) | <span data-ttu-id="4a132-120">Divide el objeto en el momento especificado, especificado como un valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="4a132-120">Splits the object at the specified time, specified as a [**REFTIME**](reftime.md) value.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a132-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a132-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a132-122">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4a132-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a132-123">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a132-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a132-124">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4a132-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a132-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a132-125">Requirements</span></span>



| <span data-ttu-id="4a132-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a132-126">Requirement</span></span> | <span data-ttu-id="4a132-127">Value</span><span class="sxs-lookup"><span data-stu-id="4a132-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a132-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a132-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4a132-129"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a132-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a132-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a132-130">Library</span></span><br/> | <dl> <span data-ttu-id="4a132-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a132-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
