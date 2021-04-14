---
description: Obtiene la interfaz ID3DXFile del objeto que creó este objeto ID3DXFileSaveObject.
ms.assetid: 79249d17-cae3-43d9-9ccb-fa804b02a353
title: 'ID3DXFileSaveObject:: GetFile (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 137f8245b94bb0ebd14e81d5f73a7ba9622a4933
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424443"
---
# <a name="id3dxfilesaveobjectgetfile-method"></a><span data-ttu-id="94022-103">ID3DXFileSaveObject:: GetFile (método)</span><span class="sxs-lookup"><span data-stu-id="94022-103">ID3DXFileSaveObject::GetFile method</span></span>

<span data-ttu-id="94022-104">Obtiene la interfaz [**ID3DXFile**](id3dxfile.md) del objeto que creó este objeto [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="94022-104">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="94022-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94022-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [in] ID3DXFile ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="94022-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94022-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94022-107">*ppFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="94022-107">*ppFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94022-108">Tipo: **[ **ID3DXFile**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="94022-108">Type: **[**ID3DXFile**](id3dxfile.md)**</span></span>

<span data-ttu-id="94022-109">Dirección de un puntero a un objeto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="94022-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94022-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94022-110">Return value</span></span>

<span data-ttu-id="94022-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="94022-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="94022-112">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="94022-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="94022-113">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DXFERR \_ BADVALUE, e \_ nointerface, e \_ Pointer.</span><span class="sxs-lookup"><span data-stu-id="94022-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, E\_NOINTERFACE, E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="94022-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94022-114">Requirements</span></span>



| <span data-ttu-id="94022-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="94022-115">Requirement</span></span> | <span data-ttu-id="94022-116">Value</span><span class="sxs-lookup"><span data-stu-id="94022-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94022-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94022-117">Header</span></span><br/>  | <dl> <span data-ttu-id="94022-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="94022-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="94022-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94022-119">Library</span></span><br/> | <dl> <span data-ttu-id="94022-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94022-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="94022-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="94022-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94022-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="94022-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




