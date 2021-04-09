---
description: Recupera el objeto ID3DXFile.
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: 'ID3DXFileEnumObject:: GetFile (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d3b5d672ca9b462e08c75a6f3352b01b07ead43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003872"
---
# <a name="id3dxfileenumobjectgetfile-method"></a><span data-ttu-id="b4622-103">ID3DXFileEnumObject:: GetFile (método)</span><span class="sxs-lookup"><span data-stu-id="b4622-103">ID3DXFileEnumObject::GetFile method</span></span>

<span data-ttu-id="b4622-104">Recupera el objeto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="b4622-104">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4622-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4622-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="b4622-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4622-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4622-107">*ppFile* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b4622-107">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4622-108">Tipo: **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b4622-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="b4622-109">Dirección de un puntero a una interfaz [**ID3DXFile**](id3dxfile.md) que representa el objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="b4622-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the returned object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4622-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4622-110">Return value</span></span>

<span data-ttu-id="b4622-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4622-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4622-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b4622-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b4622-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="b4622-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4622-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4622-114">Requirements</span></span>



| <span data-ttu-id="b4622-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4622-115">Requirement</span></span> | <span data-ttu-id="b4622-116">Value</span><span class="sxs-lookup"><span data-stu-id="b4622-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4622-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4622-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b4622-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4622-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="b4622-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4622-119">Library</span></span><br/> | <dl> <span data-ttu-id="b4622-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4622-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b4622-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4622-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4622-122">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="b4622-122">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 




