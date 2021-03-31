---
description: Función de devolución de llamada que se usa para notificar al host la información de la tabla de objetos.
MS-HAID: vspixengine.IObjectTableCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IObjectTableCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAD02864-AE08-406B-A0E9-2228DC9A73E7
api_name:
- IObjectTableCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 66247dddbf0926b420faa998461393397a4717b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806697"
---
# <a name="span-idvspixengineiobjecttablecallback_resultcallback_dword_dword_dword_variant_arrspaniobjecttablecallbackresultcallback-method"></a><span data-ttu-id="d611b-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>IObjectTableCallback:: ResultCallback (método)</span><span class="sxs-lookup"><span data-stu-id="d611b-103"><span id="vspixengine.iobjecttablecallback_resultcallback_dword_dword_dword_variant_arr"></span>IObjectTableCallback::ResultCallback method</span></span>

<span data-ttu-id="d611b-104">Función de devolución de llamada que se usa para notificar al host la información de la tabla de objetos.</span><span class="sxs-lookup"><span data-stu-id="d611b-104">A callback function used to notify the host of object table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d611b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d611b-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count0_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="d611b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d611b-106">Parameters</span></span>

<span data-ttu-id="d611b-107">*numElements* </span><span class="sxs-lookup"><span data-stu-id="d611b-107">*numElements* </span></span>  
<span data-ttu-id="d611b-108">El número total de campos en todas las columnas de todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="d611b-108">The total number of fields in all columns of all objects.</span></span>

<span data-ttu-id="d611b-109">*numRows* </span><span class="sxs-lookup"><span data-stu-id="d611b-109">*numRows* </span></span>  
<span data-ttu-id="d611b-110">Número de objetos que se van a transferir.</span><span class="sxs-lookup"><span data-stu-id="d611b-110">The number of objects being transferred.</span></span>

<span data-ttu-id="d611b-111">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="d611b-111">*numColumns* </span></span>  
<span data-ttu-id="d611b-112">El número de columnas (campos) de la información que se transfiere para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="d611b-112">The number of columns (fields) of information being transferred for each object.</span></span>

<span data-ttu-id="d611b-113">*count0 \_ pRowData* </span><span class="sxs-lookup"><span data-stu-id="d611b-113">*count0\_pRowData* </span></span>  
<span data-ttu-id="d611b-114">Información sobre los objetos; un elemento para cada campo de cada objeto.</span><span class="sxs-lookup"><span data-stu-id="d611b-114">Information about the objects; one item for each field of each object.</span></span>

## <a name="return-value"></a><span data-ttu-id="d611b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d611b-115">Return value</span></span>

<span data-ttu-id="d611b-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d611b-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d611b-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d611b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d611b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d611b-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d611b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d611b-119">Header</span></span></p></td><td><span data-ttu-id="d611b-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d611b-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d611b-121"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="d611b-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d611b-122">**IObjectTableCallback**</span><span class="sxs-lookup"><span data-stu-id="d611b-122">**IObjectTableCallback**</span></span>](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
