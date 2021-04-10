---
description: Recupera un puntero a este nodo de datos del archivo ID3DXFileSaveObject.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'ID3DXFileSaveData:: GetSave (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e23296ad0a866a0ad289a9a587c433411ef9bb8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280497"
---
# <a name="id3dxfilesavedatagetsave-method"></a><span data-ttu-id="f311e-103">ID3DXFileSaveData:: GetSave (método)</span><span class="sxs-lookup"><span data-stu-id="f311e-103">ID3DXFileSaveData::GetSave method</span></span>

<span data-ttu-id="f311e-104">Recupera un puntero a este nodo de datos del archivo [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="f311e-104">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="f311e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f311e-105">Syntax</span></span>


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="f311e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f311e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f311e-107">*ppObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f311e-107">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f311e-108">Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f311e-108">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="f311e-109">Dirección de un puntero a una interfaz [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) que representa este nodo de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f311e-109">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface representing this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f311e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f311e-110">Return value</span></span>

<span data-ttu-id="f311e-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f311e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f311e-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f311e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f311e-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="f311e-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="f311e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f311e-114">Requirements</span></span>



| <span data-ttu-id="f311e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f311e-115">Requirement</span></span> | <span data-ttu-id="f311e-116">Value</span><span class="sxs-lookup"><span data-stu-id="f311e-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f311e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f311e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f311e-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="f311e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f311e-119">Library</span></span><br/> | <dl> <span data-ttu-id="f311e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f311e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f311e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f311e-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="f311e-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




