---
description: Inicializa la \_ biblioteca klib de AUX.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Función AuxKlibInitialize (AUX \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650104"
---
# <a name="auxklibinitialize-function"></a><span data-ttu-id="c9d30-103">AuxKlibInitialize función)</span><span class="sxs-lookup"><span data-stu-id="c9d30-103">AuxKlibInitialize function</span></span>

<span data-ttu-id="c9d30-104">Inicializa la \_ biblioteca klib de AUX.</span><span class="sxs-lookup"><span data-stu-id="c9d30-104">Initializes the Aux\_klib library.</span></span> <span data-ttu-id="c9d30-105">Se debe llamar a esta función antes de que se pueda llamar a cualquier otra función de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c9d30-105">This function must be called before any other function in the library can be called.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d30-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9d30-106">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="c9d30-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9d30-107">Parameters</span></span>

<span data-ttu-id="c9d30-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c9d30-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9d30-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9d30-109">Return value</span></span>

<span data-ttu-id="c9d30-110">Si la función se ejecuta correctamente, el valor devuelto es STATUs \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c9d30-110">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="c9d30-111">Si se produce un error en la función, el valor devuelto puede ser uno de los códigos de estado definidos en NTSTATUS. h, que está disponible en el WDK.</span><span class="sxs-lookup"><span data-stu-id="c9d30-111">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9d30-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9d30-112">Remarks</span></span>

<span data-ttu-id="c9d30-113">La biblioteca de objetos que implementa esta API se puede descargar desde [aquí](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="c9d30-113">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d30-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9d30-114">Requirements</span></span>



| <span data-ttu-id="c9d30-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9d30-115">Requirement</span></span> | <span data-ttu-id="c9d30-116">Value</span><span class="sxs-lookup"><span data-stu-id="c9d30-116">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d30-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c9d30-117">Redistributable</span></span><br/> | <span data-ttu-id="c9d30-118">Biblioteca de API auxiliar de Windows versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c9d30-118">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="c9d30-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9d30-119">Header</span></span><br/>          | <dl> <span data-ttu-id="c9d30-120"><dt>AUX \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9d30-120"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9d30-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9d30-121">Library</span></span><br/>         | <dl> <span data-ttu-id="c9d30-122"><dt>AUX \_ klib. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9d30-122"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d30-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9d30-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d30-124">**AuxKlibQueryModuleInformation**</span><span class="sxs-lookup"><span data-stu-id="c9d30-124">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




