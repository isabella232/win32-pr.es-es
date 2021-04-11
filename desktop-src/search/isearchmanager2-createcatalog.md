---
description: Crea un nuevo catálogo personalizado en el indizador de Windows Search y devuelve una referencia a él.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'ISearchManager2:: CreateCatalog (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 009e34a2d1eb4d18df1747ba01ea39c3360ec81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275256"
---
# <a name="isearchmanager2createcatalog-method"></a><span data-ttu-id="49ad2-103">ISearchManager2:: CreateCatalog (método)</span><span class="sxs-lookup"><span data-stu-id="49ad2-103">ISearchManager2::CreateCatalog method</span></span>

<span data-ttu-id="49ad2-104">Crea un nuevo catálogo personalizado en el indizador de Windows Search y devuelve una referencia a él.</span><span class="sxs-lookup"><span data-stu-id="49ad2-104">Creates a new custom catalog in the Windows Search indexer and returns a reference to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="49ad2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49ad2-105">Syntax</span></span>


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a><span data-ttu-id="49ad2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49ad2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ad2-107">*pszCatalog* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49ad2-107">*pszCatalog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ad2-108">Tipo: **[ **LPCWSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49ad2-108">Type: **[**LPCWSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49ad2-109">Nombre del catálogo que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="49ad2-109">Name of catalog to create.</span></span> <span data-ttu-id="49ad2-110">Puede ser cualquier nombre seleccionado por el autor de la llamada, solo debe contener caracteres alfanuméricos estándar y un carácter de subrayado.</span><span class="sxs-lookup"><span data-stu-id="49ad2-110">Can be any name selected by the caller, must contain only standard alphanumeric characters and underscore.</span></span>

</dd> <dt>

<span data-ttu-id="49ad2-111">*ppCatalogManager* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="49ad2-111">*ppCatalogManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49ad2-112">Tipo: **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span><span class="sxs-lookup"><span data-stu-id="49ad2-112">Type: **[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span></span>

<span data-ttu-id="49ad2-113">Si se ejecuta correctamente, se devuelve una referencia al catálogo creado como un puntero de interfaz [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .</span><span class="sxs-lookup"><span data-stu-id="49ad2-113">On success a reference to the created catalog is returned as an [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) interface pointer.</span></span> <span data-ttu-id="49ad2-114">Se debe llamar a la versión () en esta interfaz después de que la aplicación que realiza la llamada haya terminado de usarla.</span><span class="sxs-lookup"><span data-stu-id="49ad2-114">The Release() must be called on this interface after the calling application has finished using it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ad2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49ad2-115">Return value</span></span>

<span data-ttu-id="49ad2-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="49ad2-116">Type: **HRESULT**</span></span>

<span data-ttu-id="49ad2-117">HRESULT que indica el estado de la operación:</span><span class="sxs-lookup"><span data-stu-id="49ad2-117">HRESULT indicating status of operation:</span></span>



| <span data-ttu-id="49ad2-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="49ad2-118">Return code</span></span>                                                                             | <span data-ttu-id="49ad2-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="49ad2-119">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49ad2-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="49ad2-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="49ad2-121">El catálogo no existía anteriormente y se creó.</span><span class="sxs-lookup"><span data-stu-id="49ad2-121">Catalog did not previously exist and was created.</span></span> <span data-ttu-id="49ad2-122">Referencia al catálogo devuelta.</span><span class="sxs-lookup"><span data-stu-id="49ad2-122">Reference to catalog returned.</span></span><br/> |
| <dl> <span data-ttu-id="49ad2-123"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="49ad2-123"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="49ad2-124">El catálogo existía anteriormente, se devolvió una referencia al catálogo.</span><span class="sxs-lookup"><span data-stu-id="49ad2-124">Catalog previously existed, reference to catalog returned.</span></span><br/>                       |



 

<span data-ttu-id="49ad2-125">ERROR HRESULT: error al crear el catálogo o argumentos no válidos pasados.</span><span class="sxs-lookup"><span data-stu-id="49ad2-125">FAILED HRESULT: Failure creating catalog or invalid arguments passed.</span></span>

## <a name="remarks"></a><span data-ttu-id="49ad2-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49ad2-126">Remarks</span></span>

<span data-ttu-id="49ad2-127">Se llama para crear un nuevo catálogo en el indizador de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="49ad2-127">Called to create a new catalog in the Windows Search indexer.</span></span> <span data-ttu-id="49ad2-128">Después de la creación, se pueden usar los métodos del administrador de [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) devuelto para agregar ubicaciones que se van a indexar, supervisar el proceso de indexación y crear consultas para enviarlas al indexador y obtener los resultados.</span><span class="sxs-lookup"><span data-stu-id="49ad2-128">After creation, the methods on the returned [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) manager can be used to add locations to be indexed, monitor indexing process, and construct queries to send to the indexer and get results.</span></span> <span data-ttu-id="49ad2-129">Consulte la documentación sobre la administración del índice para obtener más información: https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="49ad2-129">See the “Managing the Index” documentation for more info: https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span></span>

## <a name="requirements"></a><span data-ttu-id="49ad2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49ad2-130">Requirements</span></span>



| <span data-ttu-id="49ad2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ad2-131">Requirement</span></span> | <span data-ttu-id="49ad2-132">Value</span><span class="sxs-lookup"><span data-stu-id="49ad2-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49ad2-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49ad2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="49ad2-134">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="49ad2-134">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="49ad2-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49ad2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="49ad2-136">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="49ad2-136">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49ad2-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="49ad2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ad2-138">**ISearchManager2**</span><span class="sxs-lookup"><span data-stu-id="49ad2-138">**ISearchManager2**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
