---
description: Recupera un puntero al GUID que identifica un objeto de archivo de DirectX. En desuso.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: 'IDirectXFileObject:: GetId (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 336dbde487ecd1b3af7b32d3743f037c235952f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689876"
---
# <a name="idirectxfileobjectgetid-method"></a><span data-ttu-id="cceec-104">IDirectXFileObject:: GetId (método)</span><span class="sxs-lookup"><span data-stu-id="cceec-104">IDirectXFileObject::GetId method</span></span>

<span data-ttu-id="cceec-105">Recupera un puntero al GUID que identifica un objeto de archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="cceec-105">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="cceec-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="cceec-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="cceec-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cceec-107">Syntax</span></span>


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="cceec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cceec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cceec-109">*pGuid* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cceec-109">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cceec-110">Tipo: **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="cceec-110">Type: **LPGUID**</span></span>

<span data-ttu-id="cceec-111">Puntero a un GUID para recibir el identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="cceec-111">Pointer to a GUID to receive the object's ID.</span></span> <span data-ttu-id="cceec-112">Si el objeto no tiene un identificador, la función establecerá el GUID en un GUID **nulo** .</span><span class="sxs-lookup"><span data-stu-id="cceec-112">The function will set the GUID to a **NULL** GUID if the object does not have an ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cceec-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cceec-113">Return value</span></span>

<span data-ttu-id="cceec-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cceec-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cceec-115">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cceec-115">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="cceec-116">Si se produce un error en el método, el valor devuelto puede ser DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="cceec-116">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="cceec-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cceec-117">Requirements</span></span>



| <span data-ttu-id="cceec-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cceec-118">Requirement</span></span> | <span data-ttu-id="cceec-119">Value</span><span class="sxs-lookup"><span data-stu-id="cceec-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cceec-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cceec-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cceec-121"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="cceec-121"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="cceec-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cceec-122">Library</span></span><br/> | <dl> <span data-ttu-id="cceec-123"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cceec-123"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cceec-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="cceec-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cceec-125">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="cceec-125">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 




