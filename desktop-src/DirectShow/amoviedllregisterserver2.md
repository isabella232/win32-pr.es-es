---
description: La función AMovieDllRegisterServer2 registra y anula el registro de filtros.
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: Función AMovieDllRegisterServer2 (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec36290b7cad66b2b5f27633d30ae76c3331eba9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661117"
---
# <a name="amoviedllregisterserver2-function"></a><span data-ttu-id="3a8db-103">AMovieDllRegisterServer2 función)</span><span class="sxs-lookup"><span data-stu-id="3a8db-103">AMovieDllRegisterServer2 function</span></span>

<span data-ttu-id="3a8db-104">La función **AMovieDllRegisterServer2** registra y anula el registro de filtros.</span><span class="sxs-lookup"><span data-stu-id="3a8db-104">The **AMovieDllRegisterServer2** function registers and unregisters filters.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a8db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a8db-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="3a8db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a8db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a8db-107">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="3a8db-107">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="3a8db-108">**True** indica que se registra el filtro; **false** indica que se anula el registro.</span><span class="sxs-lookup"><span data-stu-id="3a8db-108">**TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a8db-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a8db-109">Return value</span></span>

<span data-ttu-id="3a8db-110">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3a8db-110">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a8db-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a8db-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a8db-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a8db-112">Remarks</span></span>

<span data-ttu-id="3a8db-113">Utilice esta función para configurar los filtros.</span><span class="sxs-lookup"><span data-stu-id="3a8db-113">Use this function to set up your filters.</span></span> <span data-ttu-id="3a8db-114">Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="3a8db-114">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a8db-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a8db-115">Requirements</span></span>



| <span data-ttu-id="3a8db-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a8db-116">Requirement</span></span> | <span data-ttu-id="3a8db-117">Value</span><span class="sxs-lookup"><span data-stu-id="3a8db-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a8db-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a8db-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3a8db-119"><dt>Dllsetup. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a8db-119"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3a8db-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a8db-120">Library</span></span><br/> | <dl> <span data-ttu-id="3a8db-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3a8db-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a8db-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a8db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a8db-123">**Funciones de instalación de DLL**</span><span class="sxs-lookup"><span data-stu-id="3a8db-123">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




