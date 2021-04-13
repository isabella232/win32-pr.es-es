---
description: Agrega un objeto de datos como elemento secundario del nodo de datos del archivo ID3DXFileSaveData.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'ID3DXFileSaveData:: AddDataObject (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b097e63792b32bc1688ce93c8ce32ffaedeae6ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362643"
---
# <a name="id3dxfilesavedataadddataobject-method"></a><span data-ttu-id="1fcd6-103">ID3DXFileSaveData:: AddDataObject (método)</span><span class="sxs-lookup"><span data-stu-id="1fcd6-103">ID3DXFileSaveData::AddDataObject method</span></span>

<span data-ttu-id="1fcd6-104">Agrega un objeto de datos como elemento secundario del nodo de datos del archivo [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="1fcd6-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fcd6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fcd6-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1fcd6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1fcd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fcd6-107">*rguidTemplate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1fcd6-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fcd6-108">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="1fcd6-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="1fcd6-109">GUID que representa la plantilla del objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="1fcd6-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="1fcd6-110">*szName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1fcd6-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fcd6-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fcd6-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fcd6-112">Puntero al nombre del objeto de datos que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="1fcd6-112">Pointer to the name of the data object to add.</span></span> <span data-ttu-id="1fcd6-113">Especifique **null** si el objeto no tiene nombre.</span><span class="sxs-lookup"><span data-stu-id="1fcd6-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="1fcd6-114">*pId* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1fcd6-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fcd6-115">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="1fcd6-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="1fcd6-116">Puntero a un GUID que representa el objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="1fcd6-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="1fcd6-117">El objeto de datos se debe haber registrado con [**ID3DXFile:: RegisterTemplates**](id3dxfile--registertemplates.md) o [**ID3DXFile:: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md).</span><span class="sxs-lookup"><span data-stu-id="1fcd6-117">The data object must have been registered with [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) or [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md).</span></span> <span data-ttu-id="1fcd6-118">Especifique **null** si el objeto no tiene un GUID.</span><span class="sxs-lookup"><span data-stu-id="1fcd6-118">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="1fcd6-119">*cbSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1fcd6-119">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fcd6-120">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fcd6-120">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fcd6-121">Tamaño del objeto de datos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="1fcd6-121">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1fcd6-122">*pvData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1fcd6-122">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fcd6-123">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fcd6-123">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fcd6-124">Puntero a un búfer que contiene todos los datos necesarios en el objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="1fcd6-124">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="1fcd6-125">*ppObj* \[ in, retval\]</span><span class="sxs-lookup"><span data-stu-id="1fcd6-125">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1fcd6-126">Tipo: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1fcd6-126">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="1fcd6-127">Dirección de un puntero a una interfaz [**ID3DXFileSaveData**](id3dxfilesavedata.md) que representa el nodo de datos de archivo al que se agregará el objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="1fcd6-127">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fcd6-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1fcd6-128">Return value</span></span>

<span data-ttu-id="1fcd6-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fcd6-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fcd6-130">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1fcd6-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1fcd6-131">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1fcd6-131">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fcd6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fcd6-132">Requirements</span></span>



| <span data-ttu-id="1fcd6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fcd6-133">Requirement</span></span> | <span data-ttu-id="1fcd6-134">Value</span><span class="sxs-lookup"><span data-stu-id="1fcd6-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fcd6-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fcd6-135">Header</span></span><br/>  | <dl> <span data-ttu-id="1fcd6-136"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fcd6-136"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="1fcd6-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fcd6-137">Library</span></span><br/> | <dl> <span data-ttu-id="1fcd6-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fcd6-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1fcd6-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fcd6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fcd6-140">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="1fcd6-140">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
