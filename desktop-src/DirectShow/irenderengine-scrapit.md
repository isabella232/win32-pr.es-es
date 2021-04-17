---
description: El método ScrapIt descarta el gráfico de filtro del motor de representación y todos los objetos asociados.
ms.assetid: b7470947-a661-4c08-8786-9298e5322e58
title: 'IRenderEngine:: ScrapIt (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ScrapIt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f9febbe20cfd5ab9a6577a6e00989c7d6fc4145
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681071"
---
# <a name="irenderenginescrapit-method"></a><span data-ttu-id="e9753-103">IRenderEngine:: ScrapIt (método)</span><span class="sxs-lookup"><span data-stu-id="e9753-103">IRenderEngine::ScrapIt method</span></span>

> [!Note]  
> <span data-ttu-id="e9753-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e9753-104">\[Deprecated.</span></span> <span data-ttu-id="e9753-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e9753-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e9753-106">El `ScrapIt` método descarta el gráfico de filtro del motor de representación y todos los objetos asociados.</span><span class="sxs-lookup"><span data-stu-id="e9753-106">The `ScrapIt` method discards the render engine's filter graph and all associated objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9753-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9753-107">Syntax</span></span>


```C++
HRESULT ScrapIt();
```



## <a name="parameters"></a><span data-ttu-id="e9753-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9753-108">Parameters</span></span>

<span data-ttu-id="e9753-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e9753-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9753-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9753-110">Return value</span></span>

<span data-ttu-id="e9753-111">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="e9753-111">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e9753-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e9753-112">Return code</span></span>                                                                                            | <span data-ttu-id="e9753-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9753-113">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="e9753-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e9753-114"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="e9753-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e9753-115">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="e9753-116"><dt>**E \_ debe \_ inicializar el \_ representador**</dt></span><span class="sxs-lookup"><span data-stu-id="e9753-116"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="e9753-117">No se pudo inicializar el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="e9753-117">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e9753-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9753-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e9753-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e9753-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e9753-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e9753-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e9753-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e9753-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e9753-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9753-122">Requirements</span></span>



| <span data-ttu-id="e9753-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9753-123">Requirement</span></span> | <span data-ttu-id="e9753-124">Value</span><span class="sxs-lookup"><span data-stu-id="e9753-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9753-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9753-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e9753-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9753-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e9753-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9753-127">Library</span></span><br/> | <dl> <span data-ttu-id="e9753-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9753-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9753-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9753-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9753-130">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="e9753-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="e9753-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="e9753-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




