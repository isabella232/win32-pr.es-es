---
description: Crea un objeto enumerador que leerá un archivo. x.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'ID3DXFile:: CreateEnumObject (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718326"
---
# <a name="id3dxfilecreateenumobject-method"></a><span data-ttu-id="099a1-103">ID3DXFile:: CreateEnumObject (método)</span><span class="sxs-lookup"><span data-stu-id="099a1-103">ID3DXFile::CreateEnumObject method</span></span>

<span data-ttu-id="099a1-104">Crea un objeto enumerador que leerá un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="099a1-104">Creates an enumerator object that will read a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="099a1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="099a1-105">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="099a1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="099a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="099a1-107">*pvSource* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="099a1-107">*pvSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="099a1-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="099a1-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="099a1-109">El origen de datos.</span><span class="sxs-lookup"><span data-stu-id="099a1-109">The data source.</span></span> <span data-ttu-id="099a1-110">Tener instaladas localmente una de las siguientes:</span><span class="sxs-lookup"><span data-stu-id="099a1-110">Either:</span></span>

-   <span data-ttu-id="099a1-111">Un nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="099a1-111">A file name</span></span>
-   <span data-ttu-id="099a1-112">Una estructura [**D3DXF \_ FILELOADMEMORY**](d3dxf-fileloadmemory.md)</span><span class="sxs-lookup"><span data-stu-id="099a1-112">A [**D3DXF\_FILELOADMEMORY**](d3dxf-fileloadmemory.md) structure</span></span>
-   <span data-ttu-id="099a1-113">Una estructura [**D3DXF \_ FILELOADRESOURCE**](d3dxf-fileloadresource.md)</span><span class="sxs-lookup"><span data-stu-id="099a1-113">A [**D3DXF\_FILELOADRESOURCE**](d3dxf-fileloadresource.md) structure</span></span>

<span data-ttu-id="099a1-114">Dependiendo del valor de loadflags.</span><span class="sxs-lookup"><span data-stu-id="099a1-114">Depending on the value of loadflags.</span></span>

</dd> <dt>

<span data-ttu-id="099a1-115">*loadflags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="099a1-115">*loadflags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="099a1-116">Tipo: **[D3DXF \_ FILELOADOPTIONS](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="099a1-116">Type: **[D3DXF\_FILELOADOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="099a1-117">Valor que especifica el origen de los datos.</span><span class="sxs-lookup"><span data-stu-id="099a1-117">Value that specifies the source of the data.</span></span> <span data-ttu-id="099a1-118">Este valor puede ser una de las marcas [D3DXF \_ FILELOADOPTIONS](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="099a1-118">This value can be one of the [D3DXF\_FILELOADOPTIONS](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="099a1-119">*ppEnumObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="099a1-119">*ppEnumObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="099a1-120">Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="099a1-120">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="099a1-121">Dirección de un puntero a una interfaz [**ID3DXFileEnumObject**](id3dxfileenumobject.md) que representa el objeto de enumerador creado.</span><span class="sxs-lookup"><span data-stu-id="099a1-121">Address of a pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="099a1-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="099a1-122">Return value</span></span>

<span data-ttu-id="099a1-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="099a1-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="099a1-124">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="099a1-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="099a1-125">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADVALUE, D3DXFERR \_ Nº.</span><span class="sxs-lookup"><span data-stu-id="099a1-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="099a1-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="099a1-126">Remarks</span></span>

<span data-ttu-id="099a1-127">Después de usar este método, use uno de los métodos [**ID3DXFileEnumObject**](id3dxfileenumobject.md) para recuperar un objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="099a1-127">After using this method, use one of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="099a1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="099a1-128">Requirements</span></span>



| <span data-ttu-id="099a1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="099a1-129">Requirement</span></span> | <span data-ttu-id="099a1-130">Value</span><span class="sxs-lookup"><span data-stu-id="099a1-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="099a1-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="099a1-131">Header</span></span><br/>  | <dl> <span data-ttu-id="099a1-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="099a1-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="099a1-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="099a1-133">Library</span></span><br/> | <dl> <span data-ttu-id="099a1-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="099a1-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="099a1-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="099a1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099a1-136">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="099a1-136">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="099a1-137">**ID3DXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="099a1-137">**ID3DXFileEnumObject**</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
