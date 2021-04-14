---
description: Guarda un objeto de datos y sus elementos secundarios en un archivo. x en el disco.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'ID3DXFileSaveObject:: Save (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424392"
---
# <a name="id3dxfilesaveobjectsave-method"></a><span data-ttu-id="26884-103">ID3DXFileSaveObject:: Save (método)</span><span class="sxs-lookup"><span data-stu-id="26884-103">ID3DXFileSaveObject::Save method</span></span>

<span data-ttu-id="26884-104">Guarda un objeto de datos y sus elementos secundarios en un archivo. x en el disco.</span><span class="sxs-lookup"><span data-stu-id="26884-104">Saves a data object and its children to a .x file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="26884-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26884-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="26884-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26884-106">Parameters</span></span>

<span data-ttu-id="26884-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="26884-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26884-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26884-108">Return value</span></span>

<span data-ttu-id="26884-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26884-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26884-110">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="26884-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="26884-111">Si se produce un error en el método, el valor devuelto puede ser el siguiente: D3DXFERR \_ BADOBJECT.</span><span class="sxs-lookup"><span data-stu-id="26884-111">If the method fails, the return value can be the following: D3DXFERR\_BADOBJECT.</span></span>

## <a name="remarks"></a><span data-ttu-id="26884-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26884-112">Remarks</span></span>

<span data-ttu-id="26884-113">Una vez que este método se realiza correctamente, ya no se puede llamar a [**ID3DXFileSaveObject:: AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData:: AddDataObject**](id3dxfilesavedata--adddataobject.md) y [**ID3DXFileSaveData:: AddDataReference**](id3dxfilesavedata--adddatareference.md) hasta que se crea un nuevo objeto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="26884-113">After this method succeeds, [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) and [**ID3DXFileSaveData::AddDataReference**](id3dxfilesavedata--adddatareference.md) can no longer be called until a new [**ID3DXFile**](id3dxfile.md) object is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="26884-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26884-114">Requirements</span></span>



| <span data-ttu-id="26884-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="26884-115">Requirement</span></span> | <span data-ttu-id="26884-116">Value</span><span class="sxs-lookup"><span data-stu-id="26884-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26884-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26884-117">Header</span></span><br/>  | <dl> <span data-ttu-id="26884-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="26884-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="26884-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26884-119">Library</span></span><br/> | <dl> <span data-ttu-id="26884-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26884-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="26884-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="26884-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26884-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="26884-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




