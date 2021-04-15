---
description: Recupera el tamaño de los datos binarios. En desuso.
ms.assetid: 99a74043-ce87-4545-961f-dade54e77735
title: 'IDirectXFileBinary:: (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetSize
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 664e2bf026df6d9e4b5bc07067ce1ce7fe7669db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548030"
---
# <a name="idirectxfilebinarygetsize-method"></a><span data-ttu-id="99fd3-104">IDirectXFileBinary:: (método)</span><span class="sxs-lookup"><span data-stu-id="99fd3-104">IDirectXFileBinary::GetSize method</span></span>

<span data-ttu-id="99fd3-105">Recupera el tamaño de los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="99fd3-105">Retrieves the size of the binary data.</span></span> <span data-ttu-id="99fd3-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="99fd3-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="99fd3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99fd3-107">Syntax</span></span>


```C++
HRESULT GetSize(
  [out] DWORD *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="99fd3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99fd3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99fd3-109">*PCB* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="99fd3-109">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99fd3-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="99fd3-110">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99fd3-111">Puntero al tamaño devuelto de los datos binarios, en bytes.</span><span class="sxs-lookup"><span data-stu-id="99fd3-111">Pointer to the returned size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99fd3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99fd3-112">Return value</span></span>

<span data-ttu-id="99fd3-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99fd3-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99fd3-114">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99fd3-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="99fd3-115">Si se produce un error en el método, el valor devuelto puede ser DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="99fd3-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="99fd3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99fd3-116">Requirements</span></span>



| <span data-ttu-id="99fd3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="99fd3-117">Requirement</span></span> | <span data-ttu-id="99fd3-118">Value</span><span class="sxs-lookup"><span data-stu-id="99fd3-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99fd3-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99fd3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="99fd3-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="99fd3-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="99fd3-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99fd3-121">Library</span></span><br/> | <dl> <span data-ttu-id="99fd3-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99fd3-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99fd3-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="99fd3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99fd3-124">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="99fd3-124">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
