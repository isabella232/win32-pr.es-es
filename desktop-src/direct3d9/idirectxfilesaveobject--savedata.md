---
description: Guarda un objeto de datos y sus elementos secundarios en un archivo de DirectX. En desuso.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'IDirectXFileSaveObject:: SaveData (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: cb901bd984e1fcd923d0ea172fb5f387b3a9302a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717720"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a><span data-ttu-id="be95f-104">IDirectXFileSaveObject:: SaveData (método)</span><span class="sxs-lookup"><span data-stu-id="be95f-104">IDirectXFileSaveObject::SaveData method</span></span>

<span data-ttu-id="be95f-105">Guarda un objeto de datos y sus elementos secundarios en un archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="be95f-105">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="be95f-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="be95f-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="be95f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be95f-107">Syntax</span></span>


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="be95f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be95f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be95f-109">*pDataObj* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="be95f-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be95f-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="be95f-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="be95f-111">Puntero a una interfaz [**IDirectXFileData**](idirectxfiledata.md) que representa el objeto de datos de archivo que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="be95f-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be95f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be95f-112">Return value</span></span>

<span data-ttu-id="be95f-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be95f-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be95f-114">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be95f-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="be95f-115">Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="be95f-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="be95f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be95f-116">Requirements</span></span>



| <span data-ttu-id="be95f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="be95f-117">Requirement</span></span> | <span data-ttu-id="be95f-118">Value</span><span class="sxs-lookup"><span data-stu-id="be95f-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be95f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be95f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="be95f-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="be95f-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="be95f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be95f-121">Library</span></span><br/> | <dl> <span data-ttu-id="be95f-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be95f-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be95f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="be95f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be95f-124">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="be95f-124">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 




