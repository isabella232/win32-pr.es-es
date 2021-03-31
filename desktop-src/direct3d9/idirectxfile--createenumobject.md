---
description: Crea un objeto de enumerador. En desuso.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'IDirectXFile:: CreateEnumObject (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d15738b78299441fe08333a41f0652f1b4224d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821354"
---
# <a name="idirectxfilecreateenumobject-method"></a><span data-ttu-id="45c92-104">IDirectXFile:: CreateEnumObject (método)</span><span class="sxs-lookup"><span data-stu-id="45c92-104">IDirectXFile::CreateEnumObject method</span></span>

<span data-ttu-id="45c92-105">Crea un objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="45c92-105">Creates an enumerator object.</span></span> <span data-ttu-id="45c92-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="45c92-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="45c92-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45c92-107">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="45c92-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45c92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45c92-109">*pvSource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45c92-109">*pvSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45c92-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45c92-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45c92-111">Puntero a los datos cuyo contenido depende del valor de dwLoadOptions</span><span class="sxs-lookup"><span data-stu-id="45c92-111">Pointer to data whose contents depend on the value of dwLoadOptions</span></span>

</dd> <dt>

<span data-ttu-id="45c92-112">*dwLoadOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45c92-112">*dwLoadOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45c92-113">Tipo: **[ **DXFILELOADOPTIONS**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="45c92-113">Type: **[**DXFILELOADOPTIONS**](dxfile.md)**</span></span>

<span data-ttu-id="45c92-114">Valor que especifica el origen de los datos.</span><span class="sxs-lookup"><span data-stu-id="45c92-114">Value that specifies the source of the data.</span></span> <span data-ttu-id="45c92-115">Este valor puede ser una de las \_ marcas DXFILELOAD XXX en las [constantes DXFILE](dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="45c92-115">This value can be one of the DXFILELOAD\_xxx flags in [DXFILE Constants](dxfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="45c92-116">*ppEnumObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="45c92-116">*ppEnumObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="45c92-117">Tipo: **[ **LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="45c92-117">Type: **[**LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span></span>

<span data-ttu-id="45c92-118">Dirección de un puntero a una interfaz [**IDirectXFileEnumObject**](idirectxfileenumobject.md) que representa el objeto de enumerador creado.</span><span class="sxs-lookup"><span data-stu-id="45c92-118">Address of a pointer to an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45c92-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45c92-119">Return value</span></span>

<span data-ttu-id="45c92-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="45c92-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="45c92-121">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="45c92-121">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="45c92-122">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR \_ BADRESOURCE, DXFILEERR \_ BADVALUE, DXFILEERR \_ FILENOTFOUND, DXFILEERR \_ RESOURCENOTFOUND, DXFILEERR \_ URLNOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="45c92-122">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADRESOURCE, DXFILEERR\_BADVALUE, DXFILEERR\_FILENOTFOUND, DXFILEERR\_RESOURCENOTFOUND, DXFILEERR\_URLNOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="45c92-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45c92-123">Remarks</span></span>

<span data-ttu-id="45c92-124">Después de usar este método, use uno de los métodos IDirectXFileEnumObject para recuperar un objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="45c92-124">After using this method, use one of the IDirectXFileEnumObject methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="45c92-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45c92-125">Requirements</span></span>



| <span data-ttu-id="45c92-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="45c92-126">Requirement</span></span> | <span data-ttu-id="45c92-127">Value</span><span class="sxs-lookup"><span data-stu-id="45c92-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45c92-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45c92-128">Header</span></span><br/>  | <dl> <span data-ttu-id="45c92-129"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="45c92-129"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="45c92-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45c92-130">Library</span></span><br/> | <dl> <span data-ttu-id="45c92-131"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45c92-131"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45c92-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="45c92-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45c92-133">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="45c92-133">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
