---
description: Recupera un puntero al nombre de un objeto de archivo de DirectX. En desuso.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'IDirectXFileObject:: GetName (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689875"
---
# <a name="idirectxfileobjectgetname-method"></a><span data-ttu-id="7f672-104">IDirectXFileObject:: GetName (método)</span><span class="sxs-lookup"><span data-stu-id="7f672-104">IDirectXFileObject::GetName method</span></span>

<span data-ttu-id="7f672-105">Recupera un puntero al nombre de un objeto de archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="7f672-105">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="7f672-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="7f672-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f672-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f672-107">Syntax</span></span>


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="7f672-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f672-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f672-109">*pstrNameBuf* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7f672-109">*pstrNameBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f672-110">Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f672-110">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f672-111">Puntero al búfer en el que se copiará el nombre del objeto de archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="7f672-111">Pointer to the buffer in which the DirectX file object's name will be copied.</span></span> <span data-ttu-id="7f672-112">Establezca en **null** si solo se necesita la longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="7f672-112">Set to **NULL** if only the buffer length is needed.</span></span>

</dd> <dt>

<span data-ttu-id="7f672-113">*pdwBufLen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7f672-113">*pdwBufLen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f672-114">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7f672-114">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7f672-115">Puntero a un valor DWORD que especifica la longitud del búfer al que apunta pstrNameBuf.</span><span class="sxs-lookup"><span data-stu-id="7f672-115">Pointer to a DWORD specifying the length of the buffer pointed to by pstrNameBuf.</span></span> <span data-ttu-id="7f672-116">El valor del parámetro pdwBufLen se modificará en la longitud del búfer necesaria para contener el nombre del objeto aunque pstrNameBuf sea **null**.</span><span class="sxs-lookup"><span data-stu-id="7f672-116">The pdwBufLen parameter value will be modified to the buffer length needed to hold the object's name even if pstrNameBuf is **NULL**.</span></span> <span data-ttu-id="7f672-117">En cualquier caso, la función devolverá DXFILEERR \_ BADVALUE si el valor original de pdwBufLen no es tan grande como o mayor que la longitud necesaria para contener el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="7f672-117">In either case, the function will return DXFILEERR\_BADVALUE if the original value of pdwBufLen is not as large as or larger than the length needed to hold the object's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f672-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f672-118">Return value</span></span>

<span data-ttu-id="7f672-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f672-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f672-120">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7f672-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="7f672-121">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="7f672-121">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="7f672-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f672-122">Requirements</span></span>



| <span data-ttu-id="7f672-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f672-123">Requirement</span></span> | <span data-ttu-id="7f672-124">Value</span><span class="sxs-lookup"><span data-stu-id="7f672-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f672-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f672-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7f672-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f672-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f672-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7f672-127">Library</span></span><br/> | <dl> <span data-ttu-id="7f672-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f672-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f672-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f672-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f672-130">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="7f672-130">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 
