---
description: Agrega un objeto de datos como un objeto secundario. En desuso.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'IDirectXFileData:: AddDataObject (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 393526bb249b0337964bee0af5be1b55b8dd513e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362679"
---
# <a name="idirectxfiledataadddataobject-method"></a><span data-ttu-id="a1a9c-104">IDirectXFileData:: AddDataObject (método)</span><span class="sxs-lookup"><span data-stu-id="a1a9c-104">IDirectXFileData::AddDataObject method</span></span>

<span data-ttu-id="a1a9c-105">Agrega un objeto de datos como un objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="a1a9c-105">Adds a data object as a child object.</span></span> <span data-ttu-id="a1a9c-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="a1a9c-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a9c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1a9c-107">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="a1a9c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1a9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1a9c-109">*pDataObj* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a1a9c-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a9c-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="a1a9c-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="a1a9c-111">Puntero a una interfaz [**IDirectXFileData**](idirectxfiledata.md) que representa el objeto de datos de archivo que se va a agregar como un objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="a1a9c-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to add as a child object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1a9c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1a9c-112">Return value</span></span>

<span data-ttu-id="a1a9c-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1a9c-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1a9c-114">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a1a9c-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="a1a9c-115">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="a1a9c-115">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="a1a9c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1a9c-116">Remarks</span></span>

<span data-ttu-id="a1a9c-117">Use el método [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para crear el objeto [**IDirectXFileData**](idirectxfiledata.md) antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="a1a9c-117">Use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create the [**IDirectXFileData**](idirectxfiledata.md) object before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1a9c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1a9c-118">Requirements</span></span>



| <span data-ttu-id="a1a9c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1a9c-119">Requirement</span></span> | <span data-ttu-id="a1a9c-120">Value</span><span class="sxs-lookup"><span data-stu-id="a1a9c-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a9c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1a9c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a1a9c-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1a9c-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1a9c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1a9c-123">Library</span></span><br/> | <dl> <span data-ttu-id="a1a9c-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1a9c-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1a9c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1a9c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a9c-126">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="a1a9c-126">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="a1a9c-127">**IDirectXFileSaveObject::CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="a1a9c-127">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




