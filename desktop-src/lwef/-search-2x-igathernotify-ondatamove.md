---
title: IGatherNotify OnDataMove (deprecated) (método)
description: Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API ISearchPersistentItemsChangedSink de Windows Search en el Windows SDK. | IGatherNotify OnDataMove (deprecated) (método)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- OnDataMove (obsoleto) características de entorno de Windows heredado
- OnDataMove (obsoleto) características de entorno heredado de Windows, interfaz IGatherNotify
- Interfaz IGatherNotify características del entorno heredado de Windows, OnDataMove (en desuso) (método)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362200"
---
# <a name="igathernotifyondatamove-deprecated-method"></a><span data-ttu-id="58c54-107">IGatherNotify:: OnDataMove (deprecated) (método)</span><span class="sxs-lookup"><span data-stu-id="58c54-107">IGatherNotify::OnDataMove (Deprecated) method</span></span>

<span data-ttu-id="58c54-108">\[**OnDataMove** puede modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto.\]</span><span class="sxs-lookup"><span data-stu-id="58c54-108">\[**OnDataMove** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="58c54-109">Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de Windows Search en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="58c54-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="58c54-110">Este método notifica al indizador de los datos que se han despasado.</span><span class="sxs-lookup"><span data-stu-id="58c54-110">This method notifies the indexer of data that has been moved.</span></span> <span data-ttu-id="58c54-111">Cuando envía la notificación al indexador, incluye la dirección anterior, la nueva dirección y la dirección lógica.</span><span class="sxs-lookup"><span data-stu-id="58c54-111">When it sends the notification to the indexer, it includes the old address, new address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c54-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58c54-112">Syntax</span></span>


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="58c54-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58c54-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58c54-114">*eChangeAdviseSemantics* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58c54-114">*eChangeAdviseSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c54-115">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="58c54-115">Type: **long**</span></span>

<span data-ttu-id="58c54-116">Parámetro enumerado que describe el tipo de movimiento que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="58c54-116">An enumerated parameter that describes the type of move that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="58c54-117">*bstrOldAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58c54-117">*bstrOldAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c54-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="58c54-118">Type: **BSTR**</span></span>

<span data-ttu-id="58c54-119">Dirección antigua del elemento que se ha desplace.</span><span class="sxs-lookup"><span data-stu-id="58c54-119">The old address of the item that moved.</span></span> <span data-ttu-id="58c54-120">En el caso de los archivos normales,*eChangeAdviseSematics* es **null**.</span><span class="sxs-lookup"><span data-stu-id="58c54-120">For normal files,*eChangeAdviseSematics* is **NULL**.</span></span> <span data-ttu-id="58c54-121">En el caso de una carpeta o directorio, establezca *eChangeAdviseSematics* en el \_ directorio GTHR CA \_ Semantics \_ .</span><span class="sxs-lookup"><span data-stu-id="58c54-121">For a folder or directory, set *eChangeAdviseSematics* to GTHR\_CA\_SEMANTICS\_DIRECTORY.</span></span>

</dd> <dt>

<span data-ttu-id="58c54-122">*bstrNewAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58c54-122">*bstrNewAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c54-123">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="58c54-123">Type: **BSTR**</span></span>

<span data-ttu-id="58c54-124">Nueva dirección del elemento que se ha despasado.</span><span class="sxs-lookup"><span data-stu-id="58c54-124">The new address of the item that moved.</span></span>

</dd> <dt>

<span data-ttu-id="58c54-125">*bstrLogicalAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="58c54-125">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c54-126">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="58c54-126">Type: **BSTR**</span></span>

<span data-ttu-id="58c54-127">Dirección lógica del elemento que se ha despasado.</span><span class="sxs-lookup"><span data-stu-id="58c54-127">The logical address of the item that moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58c54-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58c54-128">Return value</span></span>

<span data-ttu-id="58c54-129">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="58c54-129">This method does not return a value.</span></span>

 

 
