---
description: Lee los datos binarios. En desuso.
ms.assetid: 530552c5-bf05-4e86-836d-d25161832c6d
title: 'IDirectXFileBinary:: Read (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.Read
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 60548640fbbb0e67909eab1fed2df24a3465bf95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083774"
---
# <a name="idirectxfilebinaryread-method"></a><span data-ttu-id="217d6-104">IDirectXFileBinary:: Read (método)</span><span class="sxs-lookup"><span data-stu-id="217d6-104">IDirectXFileBinary::Read method</span></span>

<span data-ttu-id="217d6-105">Lee los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="217d6-105">Reads the binary data.</span></span> <span data-ttu-id="217d6-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="217d6-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="217d6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="217d6-107">Syntax</span></span>


```C++
HRESULT Read(
  [out] LPVOID  pvData,
  [in]  DWORD   cbSize,
  [out] LPDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="217d6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="217d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="217d6-109">*pvData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="217d6-109">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="217d6-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="217d6-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="217d6-111">Puntero al búfer que recibe los datos que se han leído.</span><span class="sxs-lookup"><span data-stu-id="217d6-111">Pointer to the buffer that receives the data that has been read.</span></span>

</dd> <dt>

<span data-ttu-id="217d6-112">*cbSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="217d6-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="217d6-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="217d6-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="217d6-114">Tamaño del búfer al que apunta pvData, en bytes.</span><span class="sxs-lookup"><span data-stu-id="217d6-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="217d6-115">*pcbRead* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="217d6-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="217d6-116">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="217d6-116">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="217d6-117">Puntero al número de bytes leídos realmente.</span><span class="sxs-lookup"><span data-stu-id="217d6-117">Pointer to the number of bytes actually read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="217d6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="217d6-118">Return value</span></span>

<span data-ttu-id="217d6-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="217d6-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="217d6-120">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="217d6-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="217d6-121">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREDATA.</span><span class="sxs-lookup"><span data-stu-id="217d6-121">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="217d6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="217d6-122">Requirements</span></span>



| <span data-ttu-id="217d6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="217d6-123">Requirement</span></span> | <span data-ttu-id="217d6-124">Value</span><span class="sxs-lookup"><span data-stu-id="217d6-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="217d6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="217d6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="217d6-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="217d6-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="217d6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="217d6-127">Library</span></span><br/> | <dl> <span data-ttu-id="217d6-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="217d6-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="217d6-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="217d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="217d6-130">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="217d6-130">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
