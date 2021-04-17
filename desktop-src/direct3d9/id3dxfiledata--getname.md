---
description: Recupera el nombre de este objeto de datos de archivo.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: 'ID3DXFileData:: GetName (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718322"
---
# <a name="id3dxfiledatagetname-method"></a><span data-ttu-id="d90ab-103">ID3DXFileData:: GetName (método)</span><span class="sxs-lookup"><span data-stu-id="d90ab-103">ID3DXFileData::GetName method</span></span>

<span data-ttu-id="d90ab-104">Recupera el nombre de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="d90ab-104">Retrieves the name of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d90ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d90ab-105">Syntax</span></span>


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a><span data-ttu-id="d90ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d90ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d90ab-107">*szName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d90ab-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d90ab-108">Tipo: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d90ab-108">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d90ab-109">Dirección de un puntero para recibir el nombre de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="d90ab-109">Address of a pointer to receive the name of this file data object.</span></span> <span data-ttu-id="d90ab-110">Si este parámetro es **null**, puiSize devolverá el tamaño de la cadena.</span><span class="sxs-lookup"><span data-stu-id="d90ab-110">If this parameter is **NULL**, then puiSize will return the size of the string.</span></span> <span data-ttu-id="d90ab-111">Si szName apunta a la memoria válida, el nombre de este objeto de datos de archivo se copiará en szName hasta el número de caracteres proporcionado por puiSize.</span><span class="sxs-lookup"><span data-stu-id="d90ab-111">If szName points to valid memory, the name of this file data object will be copied into szName up to the number of characters given by puiSize.</span></span>

</dd> <dt>

<span data-ttu-id="d90ab-112">*puiSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d90ab-112">*puiSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d90ab-113">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d90ab-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d90ab-114">Puntero al tamaño de la cadena que representa el nombre de este objeto de datos de archivo.</span><span class="sxs-lookup"><span data-stu-id="d90ab-114">Pointer to the size of the string that represents the name of this file data object.</span></span> <span data-ttu-id="d90ab-115">Este parámetro puede ser **null** si szName proporciona una referencia al nombre.</span><span class="sxs-lookup"><span data-stu-id="d90ab-115">This parameter can be **NULL** if szName provides a reference to the name.</span></span> <span data-ttu-id="d90ab-116">Este parámetro devolverá el tamaño de la cadena si szName es **null**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-116">This parameter will return the size of the string if szName is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d90ab-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d90ab-117">Return value</span></span>

<span data-ttu-id="d90ab-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d90ab-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d90ab-119">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d90ab-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d90ab-120">Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="d90ab-120">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="d90ab-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d90ab-121">Remarks</span></span>

<span data-ttu-id="d90ab-122">Para que este método se ejecute correctamente, szName o *puiSize* no deben ser **null**.</span><span class="sxs-lookup"><span data-stu-id="d90ab-122">For this method to succeed, either szName or *puiSize* must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d90ab-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d90ab-123">Requirements</span></span>



| <span data-ttu-id="d90ab-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d90ab-124">Requirement</span></span> | <span data-ttu-id="d90ab-125">Value</span><span class="sxs-lookup"><span data-stu-id="d90ab-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d90ab-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d90ab-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d90ab-127"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d90ab-127"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d90ab-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d90ab-128">Library</span></span><br/> | <dl> <span data-ttu-id="d90ab-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d90ab-129"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d90ab-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d90ab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d90ab-131">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="d90ab-131">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
