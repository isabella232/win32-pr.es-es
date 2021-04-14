---
description: Registra plantillas personalizadas, dado un objeto de enumeración ID3DXFileEnumObject.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'ID3DXFile:: RegisterEnumTemplates (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424447"
---
# <a name="id3dxfileregisterenumtemplates-method"></a><span data-ttu-id="d5016-103">ID3DXFile:: RegisterEnumTemplates (método)</span><span class="sxs-lookup"><span data-stu-id="d5016-103">ID3DXFile::RegisterEnumTemplates method</span></span>

<span data-ttu-id="d5016-104">Registra plantillas personalizadas, dado un objeto de enumeración [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="d5016-104">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5016-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5016-105">Syntax</span></span>


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="d5016-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5016-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5016-107">*pEnum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5016-107">*pEnum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5016-108">Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="d5016-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\***</span></span>

<span data-ttu-id="d5016-109">Puntero a un objeto de enumeración [**ID3DXFileEnumObject**](id3dxfileenumobject.md) que contiene plantillas.</span><span class="sxs-lookup"><span data-stu-id="d5016-109">Pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object that contains templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5016-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5016-110">Return value</span></span>

<span data-ttu-id="d5016-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5016-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5016-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5016-112">If the method succeeds, the return value is S\_OK .</span></span>

<span data-ttu-id="d5016-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="d5016-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5016-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5016-114">Remarks</span></span>

<span data-ttu-id="d5016-115">Cuando se llama a este método, copia las plantillas almacenadas con ID3DXFileEnumObject, que representan el archivo, en el almacén de plantillas local del objeto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="d5016-115">When this method is called, it copies templates stored with the ID3DXFileEnumObject, representing the file, to the local template store of the [**ID3DXFile**](id3dxfile.md) object.</span></span>

<span data-ttu-id="d5016-116">Si no está disponible un puntero [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , llame al método [**RegisterTemplates**](id3dxfile--registertemplates.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d5016-116">If an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) pointer is not available, call the [**RegisterTemplates**](id3dxfile--registertemplates.md) method instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5016-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5016-117">Requirements</span></span>



| <span data-ttu-id="d5016-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5016-118">Requirement</span></span> | <span data-ttu-id="d5016-119">Value</span><span class="sxs-lookup"><span data-stu-id="d5016-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5016-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5016-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d5016-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5016-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d5016-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5016-122">Library</span></span><br/> | <dl> <span data-ttu-id="d5016-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5016-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d5016-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5016-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5016-125">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="d5016-125">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="d5016-126">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="d5016-126">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




