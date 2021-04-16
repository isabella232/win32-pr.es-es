---
description: El método CloseModule del objeto Merge cierra el módulo de combinación de Windows Installer abierto actualmente.
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
title: Método Merge. CloseModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseModule
- IMsmMerge.CloseModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8688ae06cedca1e3b75290f7831f7d3539e3ec21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670309"
---
# <a name="mergeclosemodule-method"></a><span data-ttu-id="92a3d-103">Merge. CloseModule (método)</span><span class="sxs-lookup"><span data-stu-id="92a3d-103">Merge.CloseModule method</span></span>

<span data-ttu-id="92a3d-104">El método **CloseModule** del objeto [**Merge**](merge-object.md) cierra el módulo de combinación de Windows Installer abierto actualmente.</span><span class="sxs-lookup"><span data-stu-id="92a3d-104">The **CloseModule** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer merge module.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a3d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92a3d-105">Syntax</span></span>


```JScript
Merge.CloseModule()
```



## <a name="parameters"></a><span data-ttu-id="92a3d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92a3d-106">Parameters</span></span>

<span data-ttu-id="92a3d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="92a3d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92a3d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92a3d-108">Return value</span></span>

<span data-ttu-id="92a3d-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="92a3d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a3d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92a3d-110">Remarks</span></span>

<span data-ttu-id="92a3d-111">El cierre de un módulo de combinación no afectará a los errores que no se hayan recuperado.</span><span class="sxs-lookup"><span data-stu-id="92a3d-111">Closing a merge module will not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="92a3d-112">C++</span><span class="sxs-lookup"><span data-stu-id="92a3d-112">C++</span></span>

<span data-ttu-id="92a3d-113">Consulte función [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) .</span><span class="sxs-lookup"><span data-stu-id="92a3d-113">See [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="92a3d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92a3d-114">Requirements</span></span>



| <span data-ttu-id="92a3d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="92a3d-115">Requirement</span></span> | <span data-ttu-id="92a3d-116">Value</span><span class="sxs-lookup"><span data-stu-id="92a3d-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92a3d-117">Versión</span><span class="sxs-lookup"><span data-stu-id="92a3d-117">Version</span></span><br/> | <span data-ttu-id="92a3d-118">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="92a3d-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="92a3d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92a3d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="92a3d-120"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="92a3d-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="92a3d-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92a3d-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="92a3d-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a3d-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
