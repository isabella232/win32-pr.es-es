---
description: Agrega un objeto de datos como elemento secundario del objeto ID3DXFileSaveData.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'ID3DXFileSaveObject:: AddDataObject (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d1586035a0d8a81c2210009bad903aac5197bcf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717750"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a><span data-ttu-id="26b75-103">ID3DXFileSaveObject:: AddDataObject (método)</span><span class="sxs-lookup"><span data-stu-id="26b75-103">ID3DXFileSaveObject::AddDataObject method</span></span>

<span data-ttu-id="26b75-104">Agrega un objeto de datos como elemento secundario del objeto [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="26b75-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b75-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26b75-105">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="26b75-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26b75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26b75-107">*rguidTemplate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26b75-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b75-108">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="26b75-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="26b75-109">GUID que representa la plantilla del objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="26b75-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="26b75-110">*szName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26b75-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b75-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26b75-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26b75-112">Puntero al nombre del objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="26b75-112">Pointer to the name of the data object.</span></span> <span data-ttu-id="26b75-113">Especifique **null** si el objeto no tiene nombre.</span><span class="sxs-lookup"><span data-stu-id="26b75-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="26b75-114">*pId* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="26b75-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b75-115">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="26b75-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="26b75-116">Puntero a un GUID que representa el objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="26b75-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="26b75-117">Especifique **null** si el objeto no tiene un GUID.</span><span class="sxs-lookup"><span data-stu-id="26b75-117">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="26b75-118">*cbSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26b75-118">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b75-119">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26b75-119">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26b75-120">Tamaño del objeto de datos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="26b75-120">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="26b75-121">*pvData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26b75-121">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b75-122">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26b75-122">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26b75-123">Puntero a un búfer que contiene todos los datos necesarios en el objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="26b75-123">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="26b75-124">*ppObj* \[ in, retval\]</span><span class="sxs-lookup"><span data-stu-id="26b75-124">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="26b75-125">Tipo: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="26b75-125">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="26b75-126">Dirección de un puntero a una interfaz [**ID3DXFileSaveData**](id3dxfilesavedata.md) que representa el nodo de datos de archivo al que se agregará el objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="26b75-126">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26b75-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26b75-127">Return value</span></span>

<span data-ttu-id="26b75-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26b75-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26b75-129">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="26b75-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="26b75-130">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADOBJECT, DXFILEERR \_ BADVALUE, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="26b75-130">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, DXFILEERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="26b75-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26b75-131">Remarks</span></span>

<span data-ttu-id="26b75-132">Si un objeto de referencia de datos hará referencia al objeto de datos, el parámetro szName o el parámetro pId no deben ser **null**.</span><span class="sxs-lookup"><span data-stu-id="26b75-132">If a data reference object will reference the data object, either the szName or pId parameter must be non-**NULL**.</span></span>

<span data-ttu-id="26b75-133">Guarde los datos creados en el disco mediante el método [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md) .</span><span class="sxs-lookup"><span data-stu-id="26b75-133">Save the created data to disk by using the [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="26b75-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26b75-134">Requirements</span></span>



| <span data-ttu-id="26b75-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="26b75-135">Requirement</span></span> | <span data-ttu-id="26b75-136">Value</span><span class="sxs-lookup"><span data-stu-id="26b75-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26b75-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26b75-137">Header</span></span><br/>  | <dl> <span data-ttu-id="26b75-138"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="26b75-138"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="26b75-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26b75-139">Library</span></span><br/> | <dl> <span data-ttu-id="26b75-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26b75-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="26b75-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="26b75-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b75-142">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="26b75-142">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
