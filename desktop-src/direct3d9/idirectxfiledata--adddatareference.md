---
description: Crea y agrega un objeto de referencia de datos como un objeto secundario. En desuso.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'IDirectXFileData:: AddDataReference (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717723"
---
# <a name="idirectxfiledataadddatareference-method"></a><span data-ttu-id="8aaa8-104">IDirectXFileData:: AddDataReference (método)</span><span class="sxs-lookup"><span data-stu-id="8aaa8-104">IDirectXFileData::AddDataReference method</span></span>

<span data-ttu-id="8aaa8-105">Crea y agrega un objeto de referencia de datos como un objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="8aaa8-105">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="8aaa8-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="8aaa8-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aaa8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8aaa8-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a><span data-ttu-id="8aaa8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8aaa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aaa8-109">*szRef* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8aaa8-109">*szRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8aaa8-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8aaa8-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8aaa8-111">Puntero al nombre del objeto de datos al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="8aaa8-111">Pointer to the name of the referenced data object.</span></span> <span data-ttu-id="8aaa8-112">Este parámetro puede ser **null** si pguidRef proporciona una referencia al GUID.</span><span class="sxs-lookup"><span data-stu-id="8aaa8-112">This parameter can be **NULL** if pguidRef provides a reference to the GUID.</span></span>

</dd> <dt>

<span data-ttu-id="8aaa8-113">*pguidRef* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8aaa8-113">*pguidRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8aaa8-114">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="8aaa8-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="8aaa8-115">Puntero al GUID que representa los datos.</span><span class="sxs-lookup"><span data-stu-id="8aaa8-115">Pointer to the GUID representing the data.</span></span> <span data-ttu-id="8aaa8-116">Este parámetro puede ser **null** si szRef proporciona una referencia al nombre.</span><span class="sxs-lookup"><span data-stu-id="8aaa8-116">This parameter can be **NULL** if szRef provides a reference to the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8aaa8-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8aaa8-117">Return value</span></span>

<span data-ttu-id="8aaa8-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8aaa8-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8aaa8-119">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8aaa8-119">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="8aaa8-120">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="8aaa8-120">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="8aaa8-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8aaa8-121">Remarks</span></span>

<span data-ttu-id="8aaa8-122">Para que este método se ejecute correctamente, el parámetro szRef o pguidRef no debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8aaa8-122">For this method to succeed, either the szRef or pguidRef parameter must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aaa8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aaa8-123">Requirements</span></span>



| <span data-ttu-id="8aaa8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aaa8-124">Requirement</span></span> | <span data-ttu-id="8aaa8-125">Value</span><span class="sxs-lookup"><span data-stu-id="8aaa8-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8aaa8-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8aaa8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8aaa8-127"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aaa8-127"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="8aaa8-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8aaa8-128">Library</span></span><br/> | <dl> <span data-ttu-id="8aaa8-129"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8aaa8-129"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aaa8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8aaa8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aaa8-131">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="8aaa8-131">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 
