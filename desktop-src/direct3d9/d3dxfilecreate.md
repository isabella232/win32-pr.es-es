---
description: Crea una instancia de un objeto ID3DXFile.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: Función D3DXFileCreate (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157188"
---
# <a name="d3dxfilecreate-function"></a><span data-ttu-id="290ae-103">D3DXFileCreate función)</span><span class="sxs-lookup"><span data-stu-id="290ae-103">D3DXFileCreate function</span></span>

<span data-ttu-id="290ae-104">Crea una instancia de un objeto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="290ae-104">Creates an instance of an [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="290ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="290ae-105">Syntax</span></span>


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a><span data-ttu-id="290ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="290ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="290ae-107">*lplpDirectXFile*</span><span class="sxs-lookup"><span data-stu-id="290ae-107">*lplpDirectXFile*</span></span> 
</dt> <dd>

<span data-ttu-id="290ae-108">Tipo: **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="290ae-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="290ae-109">Dirección de un puntero a una interfaz [**ID3DXFile**](id3dxfile.md) que representa el objeto de archivo. x creado.</span><span class="sxs-lookup"><span data-stu-id="290ae-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the created .x file object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="290ae-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="290ae-110">Return value</span></span>

<span data-ttu-id="290ae-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="290ae-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="290ae-112">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="290ae-112">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="290ae-113">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: E \_ \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="290ae-113">If the function fails, the return value can be one of the following: E\_POINTER, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="290ae-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="290ae-114">Remarks</span></span>

<span data-ttu-id="290ae-115">Después de usar esta función, use [**RegisterTemplates**](id3dxfile--registertemplates.md) o [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) para registrar plantillas, [**CreateEnumObject**](id3dxfile--createenumobject.md) para crear un objeto de enumerador o [**CreateSaveObject**](id3dxfile--createsaveobject.md) para crear un objeto de guardado.</span><span class="sxs-lookup"><span data-stu-id="290ae-115">After using this function, use [**RegisterTemplates**](id3dxfile--registertemplates.md) or [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) to register templates, [**CreateEnumObject**](id3dxfile--createenumobject.md) to create an enumerator object, or [**CreateSaveObject**](id3dxfile--createsaveobject.md) to create a save object.</span></span>

## <a name="requirements"></a><span data-ttu-id="290ae-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="290ae-116">Requirements</span></span>



| <span data-ttu-id="290ae-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="290ae-117">Requirement</span></span> | <span data-ttu-id="290ae-118">Value</span><span class="sxs-lookup"><span data-stu-id="290ae-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="290ae-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="290ae-119">Header</span></span><br/>  | <dl> <span data-ttu-id="290ae-120"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="290ae-120"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="290ae-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="290ae-121">Library</span></span><br/> | <dl> <span data-ttu-id="290ae-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="290ae-122"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="290ae-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="290ae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="290ae-124">Funciones de archivo de D3DX X</span><span class="sxs-lookup"><span data-stu-id="290ae-124">D3DX X File Functions</span></span>](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[<span data-ttu-id="290ae-125">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="290ae-125">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="290ae-126">**CreateSaveObject**</span><span class="sxs-lookup"><span data-stu-id="290ae-126">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)
</dt> <dt>

[<span data-ttu-id="290ae-127">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="290ae-127">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[<span data-ttu-id="290ae-128">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="290ae-128">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




