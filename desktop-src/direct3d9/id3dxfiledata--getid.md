---
description: Recupera el GUID de este objeto de datos de archivo.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: 'ID3DXFileData:: GetId (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1dafb296541b1702e9163dcc6d460cf149b4007
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821218"
---
# <a name="id3dxfiledatagetid-method"></a><span data-ttu-id="ebfb4-103">ID3DXFileData:: GetId (método)</span><span class="sxs-lookup"><span data-stu-id="ebfb4-103">ID3DXFileData::GetId method</span></span>

<span data-ttu-id="ebfb4-104">Recupera el GUID de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-104">Retrieves the GUID of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebfb4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebfb4-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a><span data-ttu-id="ebfb4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebfb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebfb4-107">*pId* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ebfb4-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebfb4-108">Tipo: **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="ebfb4-108">Type: **LPGUID**</span></span>

<span data-ttu-id="ebfb4-109">Puntero a un GUID para recibir el identificador de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-109">Pointer to a GUID to receive the ID of this file data object.</span></span> <span data-ttu-id="ebfb4-110">Si el objeto de datos de archivo no tiene ningún identificador, el valor del parámetro devuelto será el GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-110">If the file data object has no ID, the returned parameter value will be GUID\_NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebfb4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ebfb4-111">Return value</span></span>

<span data-ttu-id="ebfb4-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ebfb4-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ebfb4-113">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ebfb4-114">Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="ebfb4-114">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebfb4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebfb4-115">Requirements</span></span>



| <span data-ttu-id="ebfb4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebfb4-116">Requirement</span></span> | <span data-ttu-id="ebfb4-117">Value</span><span class="sxs-lookup"><span data-stu-id="ebfb4-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebfb4-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebfb4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ebfb4-119"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebfb4-119"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="ebfb4-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ebfb4-120">Library</span></span><br/> | <dl> <span data-ttu-id="ebfb4-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebfb4-121"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ebfb4-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebfb4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebfb4-123">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="ebfb4-123">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 




