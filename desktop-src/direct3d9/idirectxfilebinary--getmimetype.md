---
description: Recupera el tipo de extensiones multipropósito de correo Internet (MIME) para los datos binarios. En desuso.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'IDirectXFileBinary:: GetMimeType (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003802"
---
# <a name="idirectxfilebinarygetmimetype-method"></a><span data-ttu-id="d047d-104">IDirectXFileBinary:: GetMimeType (método)</span><span class="sxs-lookup"><span data-stu-id="d047d-104">IDirectXFileBinary::GetMimeType method</span></span>

<span data-ttu-id="d047d-105">Recupera el tipo de extensiones multipropósito de correo Internet (MIME) para los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="d047d-105">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="d047d-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="d047d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d047d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d047d-107">Syntax</span></span>


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a><span data-ttu-id="d047d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d047d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d047d-109">*pszMimeType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d047d-109">*pszMimeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d047d-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d047d-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d047d-111">Dirección de un puntero para recibir la cadena de tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="d047d-111">Address of a pointer to receive the MIME type string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d047d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d047d-112">Return value</span></span>

<span data-ttu-id="d047d-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d047d-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d047d-114">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d047d-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="d047d-115">Si se produce un error en el método, el valor devuelto puede ser DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="d047d-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="d047d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d047d-116">Remarks</span></span>

<span data-ttu-id="d047d-117">Cuando no hay ningún tipo MIME especificado en un archivo de DirectX para un objeto binario, la función establece pszMimeType en **null**.</span><span class="sxs-lookup"><span data-stu-id="d047d-117">When there is no MIME type specified in a DirectX file for a binary object, the function will set pszMimeType to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d047d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d047d-118">Requirements</span></span>



| <span data-ttu-id="d047d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d047d-119">Requirement</span></span> | <span data-ttu-id="d047d-120">Value</span><span class="sxs-lookup"><span data-stu-id="d047d-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d047d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d047d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d047d-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="d047d-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="d047d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d047d-123">Library</span></span><br/> | <dl> <span data-ttu-id="d047d-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d047d-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d047d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d047d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d047d-126">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="d047d-126">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
