---
description: Recupera un objeto secundario en este objeto de datos de archivo.
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: 'ID3DXFileEnumObject:: GetChild (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b5b8d535a9060e80318d4043af6362810023b9d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707970"
---
# <a name="id3dxfileenumobjectgetchild-method"></a><span data-ttu-id="85c40-103">ID3DXFileEnumObject:: GetChild (método)</span><span class="sxs-lookup"><span data-stu-id="85c40-103">ID3DXFileEnumObject::GetChild method</span></span>

<span data-ttu-id="85c40-104">Recupera un objeto secundario en este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="85c40-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="85c40-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85c40-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="85c40-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85c40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85c40-107">*ID.* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="85c40-107">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85c40-108">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85c40-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85c40-109">IDENTIFICADOR del objeto secundario que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="85c40-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="85c40-110">*ppObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="85c40-110">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85c40-111">Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="85c40-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="85c40-112">Dirección de un puntero para recibir el puntero de interfaz del objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="85c40-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85c40-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85c40-113">Return value</span></span>

<span data-ttu-id="85c40-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85c40-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85c40-115">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="85c40-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="85c40-116">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="85c40-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c40-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85c40-117">Requirements</span></span>



| <span data-ttu-id="85c40-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c40-118">Requirement</span></span> | <span data-ttu-id="85c40-119">Value</span><span class="sxs-lookup"><span data-stu-id="85c40-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85c40-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85c40-120">Header</span></span><br/>  | <dl> <span data-ttu-id="85c40-121"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="85c40-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="85c40-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85c40-122">Library</span></span><br/> | <dl> <span data-ttu-id="85c40-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85c40-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="85c40-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="85c40-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c40-125">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="85c40-125">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
