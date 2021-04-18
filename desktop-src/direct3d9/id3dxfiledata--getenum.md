---
description: Recupera el objeto de enumeración en este objeto de datos de archivo.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: 'ID3DXFileData:: GetEnum (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7dd565f6f76d42159d77d8b83c638c75648f293b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718323"
---
# <a name="id3dxfiledatagetenum-method"></a><span data-ttu-id="e86ea-103">ID3DXFileData:: GetEnum (método)</span><span class="sxs-lookup"><span data-stu-id="e86ea-103">ID3DXFileData::GetEnum method</span></span>

<span data-ttu-id="e86ea-104">Recupera el objeto de enumeración en este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="e86ea-104">Retrieves the enumeration object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e86ea-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e86ea-105">Syntax</span></span>


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="e86ea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e86ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e86ea-107">*ppObj* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e86ea-107">*ppObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e86ea-108">Tipo: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e86ea-108">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="e86ea-109">Dirección de un puntero para recibir el objeto de enumeración en este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="e86ea-109">Address of a pointer to receive the enumeration object in this file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e86ea-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e86ea-110">Return value</span></span>

<span data-ttu-id="e86ea-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e86ea-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e86ea-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e86ea-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e86ea-113">Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="e86ea-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e86ea-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e86ea-114">Requirements</span></span>



| <span data-ttu-id="e86ea-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e86ea-115">Requirement</span></span> | <span data-ttu-id="e86ea-116">Value</span><span class="sxs-lookup"><span data-stu-id="e86ea-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e86ea-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e86ea-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e86ea-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e86ea-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e86ea-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e86ea-119">Library</span></span><br/> | <dl> <span data-ttu-id="e86ea-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e86ea-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e86ea-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e86ea-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86ea-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="e86ea-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




