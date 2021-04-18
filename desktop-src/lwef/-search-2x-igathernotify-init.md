---
title: IGatherNotify init (deprecated) (método)
description: Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API ISearchPersistentItemsChangedSink de Windows Search en el Windows SDK. | IGatherNotify init (deprecated) (método)
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Init (obsoleto) características del entorno de Windows heredado
- Init (obsoleto) características del entorno heredado de Windows, interfaz IGatherNotify
- Interfaz IGatherNotify características del entorno heredado de Windows, método init (obsoleto)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698115"
---
# <a name="igathernotifyinit-deprecated-method"></a><span data-ttu-id="a773c-107">IGatherNotify:: init (deprecated) (método)</span><span class="sxs-lookup"><span data-stu-id="a773c-107">IGatherNotify::Init (Deprecated) method</span></span>

<span data-ttu-id="a773c-108">\[**Init** puede modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto.\]</span><span class="sxs-lookup"><span data-stu-id="a773c-108">\[**Init** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="a773c-109">Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de Windows Search en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a773c-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="a773c-110">Inicializa la interfaz del recopilador.</span><span class="sxs-lookup"><span data-stu-id="a773c-110">Initializes the Gatherer interface.</span></span> <span data-ttu-id="a773c-111">También especifica el índice al que se va a notificar y el almacén de aplicaciones que se va a supervisar.</span><span class="sxs-lookup"><span data-stu-id="a773c-111">Also specifies the index to notify and the application store to monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="a773c-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a773c-112">Syntax</span></span>


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a><span data-ttu-id="a773c-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a773c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a773c-114">*bstrApplication* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a773c-114">*bstrApplication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a773c-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a773c-115">Type: **BSTR**</span></span>

<span data-ttu-id="a773c-116">Cadena que especifica la aplicación de destino.</span><span class="sxs-lookup"><span data-stu-id="a773c-116">A string that specifies the target application.</span></span>

</dd> <dt>

<span data-ttu-id="a773c-117">*bstrProject* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a773c-117">*bstrProject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a773c-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a773c-118">Type: **BSTR**</span></span>

<span data-ttu-id="a773c-119">Cadena que especifica el nombre del indizador al que se va a pasar la información del recopilador.</span><span class="sxs-lookup"><span data-stu-id="a773c-119">A string that specifies the name of the indexer to pass gatherer information to.</span></span>

</dd> <dt>

<span data-ttu-id="a773c-120">*varScopesBstrArray* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a773c-120">*varScopesBstrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a773c-121">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="a773c-121">Type: **variant**</span></span>

<span data-ttu-id="a773c-122">Parámetro opcional, que permite pasar una matriz de ámbitos que se van a inicializar.</span><span class="sxs-lookup"><span data-stu-id="a773c-122">Optional parameter, that enables you to pass an array of scopes to be initialized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a773c-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a773c-123">Return value</span></span>

<span data-ttu-id="a773c-124">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a773c-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a773c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a773c-125">Remarks</span></span>

<span data-ttu-id="a773c-126">Inicialice con Application = "RSApp", Project = "alindex".</span><span class="sxs-lookup"><span data-stu-id="a773c-126">Initialize with application="RSApp", Project="MyIndex".</span></span>

 

 
