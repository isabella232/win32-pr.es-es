---
description: Estas funciones proporcionan compatibilidad para implementar la interfaz IUnknown en DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Funciones auxiliares de COM (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681187"
---
# <a name="com-helper-functions"></a><span data-ttu-id="05d76-103">Funciones auxiliares de COM</span><span class="sxs-lookup"><span data-stu-id="05d76-103">COM Helper Functions</span></span>

<span data-ttu-id="05d76-104">Estas funciones proporcionan compatibilidad para implementar la interfaz **IUnknown** en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="05d76-104">These functions provide support for implementing the **IUnknown** interface in DirectShow.</span></span>



| <span data-ttu-id="05d76-105">Función</span><span class="sxs-lookup"><span data-stu-id="05d76-105">Function</span></span>                                               | <span data-ttu-id="05d76-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="05d76-106">Description</span></span>                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="05d76-107">**DECLARAR \_ IUNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="05d76-107">**DECLARE\_IUNKNOWN**</span></span>](declare-iunknown.md)          | <span data-ttu-id="05d76-108">Declara los tres métodos de la interfaz base para una nueva interfaz.</span><span class="sxs-lookup"><span data-stu-id="05d76-108">Declares the three methods of the base interface for a new interface.</span></span> |
| [<span data-ttu-id="05d76-109">**GetInterface**</span><span class="sxs-lookup"><span data-stu-id="05d76-109">**GetInterface**</span></span>](getinterface.md)                   | <span data-ttu-id="05d76-110">Recupera un puntero de interfaz al cliente solicitado.</span><span class="sxs-lookup"><span data-stu-id="05d76-110">Retrieves an interface pointer to the requested client.</span></span>               |
| [<span data-ttu-id="05d76-111">**INonDelegatingUnknown**</span><span class="sxs-lookup"><span data-stu-id="05d76-111">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md) | <span data-ttu-id="05d76-112">Versión no delegada de la interfaz **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="05d76-112">Nondelegating version of the **IUnknown** interface.</span></span>                  |
| [<span data-ttu-id="05d76-113">**LoadOLEAut32**</span><span class="sxs-lookup"><span data-stu-id="05d76-113">**LoadOLEAut32**</span></span>](loadoleaut32.md)                   | <span data-ttu-id="05d76-114">Carga el archivo DLL de automatización (OleAut32.dll).</span><span class="sxs-lookup"><span data-stu-id="05d76-114">Loads the Automation DLL (OleAut32.dll).</span></span>                              |



 

## <a name="requirements"></a><span data-ttu-id="05d76-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05d76-115">Requirements</span></span>



| <span data-ttu-id="05d76-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="05d76-116">Requirement</span></span> | <span data-ttu-id="05d76-117">Value</span><span class="sxs-lookup"><span data-stu-id="05d76-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05d76-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05d76-118">Header</span></span><br/>  | <dl> <span data-ttu-id="05d76-119"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05d76-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="05d76-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05d76-120">Library</span></span><br/> | <dl> <span data-ttu-id="05d76-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="05d76-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05d76-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="05d76-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d76-123">Funciones de la utilidad</span><span class="sxs-lookup"><span data-stu-id="05d76-123">Utility Functions</span></span>](utility-functions.md)
</dt> </dl>

 

 




