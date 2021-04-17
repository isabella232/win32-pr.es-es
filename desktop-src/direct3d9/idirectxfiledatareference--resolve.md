---
description: Resuelve referencias de datos. En desuso.
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'IDirectXFileDataReference:: Resolve (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1b047245e3f89a618cde83e5c18a323f9364f3ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718385"
---
# <a name="idirectxfiledatareferenceresolve-method"></a><span data-ttu-id="af81d-104">IDirectXFileDataReference:: Resolve (método)</span><span class="sxs-lookup"><span data-stu-id="af81d-104">IDirectXFileDataReference::Resolve method</span></span>

<span data-ttu-id="af81d-105">Resuelve referencias de datos.</span><span class="sxs-lookup"><span data-stu-id="af81d-105">Resolves data references.</span></span> <span data-ttu-id="af81d-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="af81d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="af81d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af81d-107">Syntax</span></span>


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="af81d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af81d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af81d-109">*ppDataObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="af81d-109">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="af81d-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="af81d-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="af81d-111">Dirección de un puntero a una interfaz [**IDirectXFileData**](idirectxfiledata.md) que representa el objeto de datos de archivo devuelto.</span><span class="sxs-lookup"><span data-stu-id="af81d-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af81d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af81d-112">Return value</span></span>

<span data-ttu-id="af81d-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af81d-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af81d-114">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af81d-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="af81d-115">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="af81d-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="af81d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af81d-116">Requirements</span></span>



| <span data-ttu-id="af81d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="af81d-117">Requirement</span></span> | <span data-ttu-id="af81d-118">Value</span><span class="sxs-lookup"><span data-stu-id="af81d-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af81d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af81d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="af81d-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="af81d-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="af81d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af81d-121">Library</span></span><br/> | <dl> <span data-ttu-id="af81d-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af81d-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af81d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="af81d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af81d-124">IDirectXFileDataReference</span><span class="sxs-lookup"><span data-stu-id="af81d-124">IDirectXFileDataReference</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 




