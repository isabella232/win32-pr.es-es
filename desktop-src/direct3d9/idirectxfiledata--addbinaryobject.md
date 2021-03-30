---
description: Crea un objeto binario y lo agrega como un objeto secundario. En desuso.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'IDirectXFileData:: AddBinaryObject (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 8373b9c4328a8683f32c1fe7ab979cb8d7636f87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280249"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a><span data-ttu-id="1604e-104">IDirectXFileData:: AddBinaryObject (método)</span><span class="sxs-lookup"><span data-stu-id="1604e-104">IDirectXFileData::AddBinaryObject method</span></span>

<span data-ttu-id="1604e-105">Crea un objeto binario y lo agrega como un objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="1604e-105">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="1604e-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="1604e-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="1604e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1604e-107">Syntax</span></span>


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="1604e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1604e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1604e-109">*szName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1604e-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1604e-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1604e-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1604e-111">Puntero al nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="1604e-111">Pointer to the name of the object.</span></span> <span data-ttu-id="1604e-112">Especifique **null** si el objeto no necesita un nombre.</span><span class="sxs-lookup"><span data-stu-id="1604e-112">Specify **NULL** if the object does not need a name.</span></span>

</dd> <dt>

<span data-ttu-id="1604e-113">*pguid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1604e-113">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1604e-114">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="1604e-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="1604e-115">Puntero al GUID que representa el objeto.</span><span class="sxs-lookup"><span data-stu-id="1604e-115">Pointer to the GUID representing the object.</span></span> <span data-ttu-id="1604e-116">Especifique **null** si el objeto no necesita un GUID.</span><span class="sxs-lookup"><span data-stu-id="1604e-116">Specify **NULL** if the object does not need a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="1604e-117">*szMimeType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1604e-117">*szMimeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1604e-118">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1604e-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1604e-119">Puntero al tipo MIME del objeto.</span><span class="sxs-lookup"><span data-stu-id="1604e-119">Pointer to the object's MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="1604e-120">*pvData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1604e-120">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1604e-121">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1604e-121">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1604e-122">Puntero a los datos del objeto.</span><span class="sxs-lookup"><span data-stu-id="1604e-122">Pointer to the object's data.</span></span>

</dd> <dt>

<span data-ttu-id="1604e-123">*cbSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1604e-123">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1604e-124">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1604e-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1604e-125">Tamaño del búfer al que apunta pvData, en bytes.</span><span class="sxs-lookup"><span data-stu-id="1604e-125">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1604e-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1604e-126">Return value</span></span>

<span data-ttu-id="1604e-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1604e-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1604e-128">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1604e-128">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="1604e-129">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="1604e-129">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="1604e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1604e-130">Requirements</span></span>



| <span data-ttu-id="1604e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1604e-131">Requirement</span></span> | <span data-ttu-id="1604e-132">Value</span><span class="sxs-lookup"><span data-stu-id="1604e-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1604e-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1604e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="1604e-134"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="1604e-134"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="1604e-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1604e-135">Library</span></span><br/> | <dl> <span data-ttu-id="1604e-136"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1604e-136"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1604e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1604e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1604e-138">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="1604e-138">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="1604e-139">**IDirectXFileBinary::GetMimeType**</span><span class="sxs-lookup"><span data-stu-id="1604e-139">**IDirectXFileBinary::GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
