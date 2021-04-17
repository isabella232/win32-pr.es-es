---
description: Recupera el GUID de este nodo de datos del archivo ID3DXFileSaveData.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: 'ID3DXFileSaveData:: GetId (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b03322e03d1bedc10f9deec82c60418b5ad846b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698320"
---
# <a name="id3dxfilesavedatagetid-method"></a><span data-ttu-id="70d7f-103">ID3DXFileSaveData:: GetId (método)</span><span class="sxs-lookup"><span data-stu-id="70d7f-103">ID3DXFileSaveData::GetId method</span></span>

<span data-ttu-id="70d7f-104">Recupera el GUID de este nodo de datos del archivo [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="70d7f-104">Retrieves the GUID of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d7f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70d7f-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="70d7f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70d7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70d7f-107">*pId* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="70d7f-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70d7f-108">Tipo: **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="70d7f-108">Type: **LPGUID**</span></span>

<span data-ttu-id="70d7f-109">Puntero a un GUID para recibir el identificador de este nodo de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="70d7f-109">Pointer to a GUID to receive the ID of this file data node.</span></span> <span data-ttu-id="70d7f-110">Si el objeto no tiene ningún identificador, el valor del parámetro devuelto será el GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="70d7f-110">If the object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70d7f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70d7f-111">Return value</span></span>

<span data-ttu-id="70d7f-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="70d7f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="70d7f-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="70d7f-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="70d7f-114">Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="70d7f-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="70d7f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70d7f-115">Requirements</span></span>



| <span data-ttu-id="70d7f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="70d7f-116">Requirement</span></span> | <span data-ttu-id="70d7f-117">Value</span><span class="sxs-lookup"><span data-stu-id="70d7f-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70d7f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70d7f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="70d7f-119"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="70d7f-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="70d7f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70d7f-120">Library</span></span><br/> | <dl> <span data-ttu-id="70d7f-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70d7f-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="70d7f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="70d7f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70d7f-123">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="70d7f-123">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




