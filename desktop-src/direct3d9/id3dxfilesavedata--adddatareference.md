---
description: Agrega una referencia de datos como un elemento secundario de este nodo de datos de archivo ID3DXFileSaveData. La referencia de datos apunta a un objeto de datos de archivo.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'ID3DXFileSaveData:: AddDataReference (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f4aabf5601ef73f4e1062b1db1a28c1f0deae5fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003870"
---
# <a name="id3dxfilesavedataadddatareference-method"></a><span data-ttu-id="15ca0-104">ID3DXFileSaveData:: AddDataReference (método)</span><span class="sxs-lookup"><span data-stu-id="15ca0-104">ID3DXFileSaveData::AddDataReference method</span></span>

<span data-ttu-id="15ca0-105">Agrega una referencia de datos como un elemento secundario de este nodo de datos de archivo [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="15ca0-105">Adds a data reference as a child of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span> <span data-ttu-id="15ca0-106">La referencia de datos apunta a un objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="15ca0-106">The data reference points to a file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ca0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15ca0-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a><span data-ttu-id="15ca0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15ca0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15ca0-109">*szName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="15ca0-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15ca0-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15ca0-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15ca0-111">Puntero al nombre del objeto de datos que se va a agregar por referencia.</span><span class="sxs-lookup"><span data-stu-id="15ca0-111">Pointer to the name of the data object to add by reference.</span></span> <span data-ttu-id="15ca0-112">Especifique **null** si el objeto de datos no tiene nombre.</span><span class="sxs-lookup"><span data-stu-id="15ca0-112">Specify **NULL** if the data object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="15ca0-113">*pId* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="15ca0-113">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15ca0-114">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="15ca0-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="15ca0-115">Puntero a un GUID que representa el objeto de datos que se va a agregar por referencia.</span><span class="sxs-lookup"><span data-stu-id="15ca0-115">Pointer to a GUID representing the data object to add by reference.</span></span> <span data-ttu-id="15ca0-116">Si **es null**, se agregará una referencia que señala al objeto de datos con el nombre dado por szName.</span><span class="sxs-lookup"><span data-stu-id="15ca0-116">If **NULL**, a reference will be added that points to the data object with the name given by szName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15ca0-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15ca0-117">Return value</span></span>

<span data-ttu-id="15ca0-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15ca0-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15ca0-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="15ca0-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="15ca0-120">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="15ca0-120">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="15ca0-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15ca0-121">Remarks</span></span>

<span data-ttu-id="15ca0-122">El objeto de datos de archivo al que se hace referencia debe tener un nombre o un GUID.</span><span class="sxs-lookup"><span data-stu-id="15ca0-122">The file data object being referenced must have either a name or a GUID.</span></span> <span data-ttu-id="15ca0-123">El objeto de datos de archivo también se debe derivar de un objeto [**ID3DXFileSaveData**](id3dxfilesavedata.md) primario diferente.</span><span class="sxs-lookup"><span data-stu-id="15ca0-123">The file data object must also derive from a different parent [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="15ca0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15ca0-124">Requirements</span></span>



| <span data-ttu-id="15ca0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="15ca0-125">Requirement</span></span> | <span data-ttu-id="15ca0-126">Value</span><span class="sxs-lookup"><span data-stu-id="15ca0-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15ca0-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15ca0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="15ca0-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="15ca0-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="15ca0-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15ca0-129">Library</span></span><br/> | <dl> <span data-ttu-id="15ca0-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15ca0-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="15ca0-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="15ca0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ca0-132">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="15ca0-132">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
