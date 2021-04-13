---
description: Crea un objeto de datos. En desuso.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'IDirectXFileSaveObject:: CreateDataObject (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362534"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a><span data-ttu-id="a0fd6-104">IDirectXFileSaveObject:: CreateDataObject (método)</span><span class="sxs-lookup"><span data-stu-id="a0fd6-104">IDirectXFileSaveObject::CreateDataObject method</span></span>

<span data-ttu-id="a0fd6-105">Crea un objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-105">Creates a data object.</span></span> <span data-ttu-id="a0fd6-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0fd6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0fd6-107">Syntax</span></span>


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="a0fd6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0fd6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0fd6-109">*rguidTemplate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0fd6-109">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd6-110">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="a0fd6-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="a0fd6-111">GUID que representa la plantilla del objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-111">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd6-112">*szName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0fd6-112">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd6-113">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0fd6-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0fd6-114">Puntero al nombre del objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-114">Pointer to the name of the data object.</span></span> <span data-ttu-id="a0fd6-115">Especifique **null** si el objeto no tiene nombre.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-115">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd6-116">*pguid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0fd6-116">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd6-117">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="a0fd6-117">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="a0fd6-118">Puntero a un GUID que representa el objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-118">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="a0fd6-119">Especifique **null** si el objeto no tiene un GUID.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-119">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd6-120">*cbSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0fd6-120">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd6-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0fd6-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0fd6-122">Tamaño del objeto de datos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-122">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd6-123">*pvData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0fd6-123">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd6-124">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0fd6-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0fd6-125">Puntero a un búfer que contiene todos los datos de miembro necesarios.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-125">Pointer to a buffer containing all required member's data.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd6-126">*ppDataObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a0fd6-126">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd6-127">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0fd6-127">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="a0fd6-128">Dirección de un puntero a una interfaz [**IDirectXFileData**](idirectxfiledata.md) que representa el objeto de datos de archivo creado.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-128">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the created file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0fd6-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0fd6-129">Return value</span></span>

<span data-ttu-id="a0fd6-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0fd6-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0fd6-131">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-131">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="a0fd6-132">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="a0fd6-132">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="a0fd6-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0fd6-133">Remarks</span></span>

<span data-ttu-id="a0fd6-134">Si un objeto de referencia de datos hará referencia al objeto de datos, el parámetro szName o pguid no debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-134">If a data reference object will reference the data object, either the szName or pguid parameter must be non-**NULL**.</span></span>

<span data-ttu-id="a0fd6-135">Guarde las plantillas mediante el método [**IDirectXFileSaveObject:: SaveTemplates**](idirectxfilesaveobject--savetemplates.md) antes de guardar los datos creados por este método.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-135">Save any templates by using the [**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) method before saving the data created by this method.</span></span> <span data-ttu-id="a0fd6-136">Guarde los datos creados mediante el método [**IDirectXFileSaveObject:: savedata**](idirectxfilesaveobject--savedata.md) .</span><span class="sxs-lookup"><span data-stu-id="a0fd6-136">Save the created data by using the [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) method.</span></span>

<span data-ttu-id="a0fd6-137">Si necesita guardar datos opcionales, use el método [**IDirectXFileData:: AddDataObject**](idirectxfiledata--adddataobject.md) después de usar este método y antes de usar [**IDirectXFileSaveObject:: savedata**](idirectxfilesaveobject--savedata.md).</span><span class="sxs-lookup"><span data-stu-id="a0fd6-137">If you need to save optional data, use the [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) method after using this method and before using [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md).</span></span> <span data-ttu-id="a0fd6-138">Si el objeto tiene objetos secundarios, agréguelos antes de llamar a **IDirectXFileSaveObject:: savedata**.</span><span class="sxs-lookup"><span data-stu-id="a0fd6-138">If the object has child objects, add them before calling **IDirectXFileSaveObject::SaveData**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0fd6-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0fd6-139">Requirements</span></span>



| <span data-ttu-id="a0fd6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0fd6-140">Requirement</span></span> | <span data-ttu-id="a0fd6-141">Value</span><span class="sxs-lookup"><span data-stu-id="a0fd6-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fd6-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0fd6-142">Header</span></span><br/>  | <dl> <span data-ttu-id="a0fd6-143"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0fd6-143"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0fd6-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0fd6-144">Library</span></span><br/> | <dl> <span data-ttu-id="a0fd6-145"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0fd6-145"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0fd6-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0fd6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0fd6-147">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="a0fd6-147">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="a0fd6-148">**IDirectXFileData::AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="a0fd6-148">**IDirectXFileData::AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)
</dt> <dt>

[<span data-ttu-id="a0fd6-149">**IDirectXFileSaveObject:: SaveData**</span><span class="sxs-lookup"><span data-stu-id="a0fd6-149">**IDirectXFileSaveObject::SaveData**</span></span>](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[<span data-ttu-id="a0fd6-150">**IDirectXFileSaveObject::SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="a0fd6-150">**IDirectXFileSaveObject::SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 
