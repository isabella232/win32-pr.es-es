---
description: Crea una instancia de un objeto DirectXFile. En desuso.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: Función DirectXFileCreate (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721441"
---
# <a name="directxfilecreate-function"></a><span data-ttu-id="b0e26-104">DirectXFileCreate función)</span><span class="sxs-lookup"><span data-stu-id="b0e26-104">DirectXFileCreate function</span></span>

<span data-ttu-id="b0e26-105">Crea una instancia de un objeto DirectXFile.</span><span class="sxs-lookup"><span data-stu-id="b0e26-105">Creates an instance of a DirectXFile object.</span></span> <span data-ttu-id="b0e26-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="b0e26-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e26-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0e26-107">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="b0e26-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0e26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e26-109">*lplpDirectXFile*</span><span class="sxs-lookup"><span data-stu-id="b0e26-109">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="b0e26-110">Tipo: **[ **LPDIRECTXFILE**](idirectxfile.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0e26-110">Type: **[**LPDIRECTXFILE**](idirectxfile.md)\***</span></span>

<span data-ttu-id="b0e26-111">Dirección de un puntero a una interfaz [**IDirectXFile**](idirectxfile.md) que representa el objeto DirectXFile creado.</span><span class="sxs-lookup"><span data-stu-id="b0e26-111">Address of a pointer to an [**IDirectXFile**](idirectxfile.md) interface, representing the created DirectXFile object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e26-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0e26-112">Return value</span></span>

<span data-ttu-id="b0e26-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0e26-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0e26-114">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b0e26-114">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b0e26-115">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="b0e26-115">If the function fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e26-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0e26-116">Remarks</span></span>

<span data-ttu-id="b0e26-117">Después de usar esta función, use [**RegisterTemplates**](idirectxfile--registertemplates.md) para registrar plantillas, [**CreateEnumObject**](idirectxfile--createenumobject.md) para crear un objeto de enumerador o [**CreateSaveObject**](idirectxfile--createsaveobject.md) para crear un objeto de guardado.</span><span class="sxs-lookup"><span data-stu-id="b0e26-117">After using this function, use [**RegisterTemplates**](idirectxfile--registertemplates.md) to register templates, [**CreateEnumObject**](idirectxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](idirectxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e26-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0e26-118">Requirements</span></span>



| <span data-ttu-id="b0e26-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0e26-119">Requirement</span></span> | <span data-ttu-id="b0e26-120">Value</span><span class="sxs-lookup"><span data-stu-id="b0e26-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e26-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0e26-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b0e26-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e26-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0e26-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0e26-123">Library</span></span><br/> | <dl> <span data-ttu-id="b0e26-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0e26-124"><dt>D3dxof.lib</dt></span></span> </dl> |
| <span data-ttu-id="b0e26-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0e26-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b0e26-126"><dt>D3dxof.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0e26-126"><dt>D3dxof.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0e26-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0e26-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0e26-128">Funciones de archivo X</span><span class="sxs-lookup"><span data-stu-id="b0e26-128">X File Functions</span></span>](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="b0e26-129">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="b0e26-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="b0e26-130">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="b0e26-130">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="b0e26-131">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="b0e26-131">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




