---
description: Guarda las plantillas en un archivo de DirectX. En desuso.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'IDirectXFileSaveObject:: SaveTemplates (método) (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362533"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a><span data-ttu-id="79145-104">IDirectXFileSaveObject:: SaveTemplates (método)</span><span class="sxs-lookup"><span data-stu-id="79145-104">IDirectXFileSaveObject::SaveTemplates method</span></span>

<span data-ttu-id="79145-105">Guarda las plantillas en un archivo de DirectX.</span><span class="sxs-lookup"><span data-stu-id="79145-105">Saves templates to a DirectX file.</span></span> <span data-ttu-id="79145-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="79145-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="79145-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79145-107">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a><span data-ttu-id="79145-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79145-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79145-109">*cTemplates* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79145-109">*cTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79145-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79145-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79145-111">Número total de plantillas que se van a guardar.</span><span class="sxs-lookup"><span data-stu-id="79145-111">Total number of templates to save.</span></span>

</dd> <dt>

<span data-ttu-id="79145-112">*ppguidTemplates* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="79145-112">*ppguidTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79145-113">Tipo: **[**GUID**](guid.md) \* \* const**</span><span class="sxs-lookup"><span data-stu-id="79145-113">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="79145-114">Dirección de un puntero a una matriz de los GUID de todas las plantillas que se van a guardar.</span><span class="sxs-lookup"><span data-stu-id="79145-114">Address of a pointer to an array of the GUIDs for all templates to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79145-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79145-115">Return value</span></span>

<span data-ttu-id="79145-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79145-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79145-117">Si el método se ejecuta correctamente, el valor devuelto es DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="79145-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="79145-118">Si se produce un error en el método, el valor devuelto puede ser DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="79145-118">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="79145-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79145-119">Remarks</span></span>

<span data-ttu-id="79145-120">El siguiente fragmento de código proporciona una llamada de ejemplo a **IDirectXFileSaveObject:: SaveTemplates** y el contenido de ejemplo de la matriz a la que apunta ppguidTemplates.</span><span class="sxs-lookup"><span data-stu-id="79145-120">The following code fragment provides an example call to **IDirectXFileSaveObject::SaveTemplates** and example contents for the array to which ppguidTemplates points.</span></span>


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



<span data-ttu-id="79145-121">Después de usar este método para guardar las plantillas, use el método [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para crear un objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="79145-121">After using this method to save the templates, use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="79145-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79145-122">Requirements</span></span>



| <span data-ttu-id="79145-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="79145-123">Requirement</span></span> | <span data-ttu-id="79145-124">Value</span><span class="sxs-lookup"><span data-stu-id="79145-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79145-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79145-125">Header</span></span><br/>  | <dl> <span data-ttu-id="79145-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="79145-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="79145-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79145-127">Library</span></span><br/> | <dl> <span data-ttu-id="79145-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79145-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79145-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="79145-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79145-130">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="79145-130">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="79145-131">**IDirectXFileSaveObject::CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="79145-131">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
