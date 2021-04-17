---
title: IGatherNotify OnDataChange (deprecated) (método)
description: Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API ISearchPersistentItemsChangedSink de Windows Search en el Windows SDK. | IGatherNotify OnDataChange (deprecated) (método)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- OnDataChange (obsoleto) características de entorno de Windows heredado
- OnDataChange (obsoleto) características de entorno heredado de Windows, interfaz IGatherNotify
- Interfaz IGatherNotify características del entorno heredado de Windows, OnDataChange (en desuso) (método)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698114"
---
# <a name="igathernotifyondatachange-deprecated-method"></a><span data-ttu-id="99c97-107">IGatherNotify:: OnDataChange (deprecated) (método)</span><span class="sxs-lookup"><span data-stu-id="99c97-107">IGatherNotify::OnDataChange (Deprecated) method</span></span>

<span data-ttu-id="99c97-108">\[**OnDataChange** puede modificarse o no estar disponible en versiones posteriores del sistema operativo o del producto.\]</span><span class="sxs-lookup"><span data-stu-id="99c97-108">\[**OnDataChange** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="99c97-109">Este tema de la interfaz de búsqueda en el escritorio de Windows está en desuso y se ha sustituido por la API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de Windows Search en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="99c97-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="99c97-110">Este método notifica al indizador de los datos que han cambiado.</span><span class="sxs-lookup"><span data-stu-id="99c97-110">This method notifies the indexer of data that has changed.</span></span> <span data-ttu-id="99c97-111">Cuando envía la notificación al indexador, incluye el tipo de cambio, la dirección física y la dirección lógica.</span><span class="sxs-lookup"><span data-stu-id="99c97-111">When it sends the notification to the indexer, it includes the type of change, physical address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c97-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99c97-112">Syntax</span></span>


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="99c97-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99c97-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99c97-114">*eChangeAdvise* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c97-114">*eChangeAdvise* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c97-115">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="99c97-115">Type: **long**</span></span>

<span data-ttu-id="99c97-116">Valor enumerado que especifica el tipo de cambio.</span><span class="sxs-lookup"><span data-stu-id="99c97-116">An enumerated value that specifies the type of change.</span></span>

</dd> <dt>

<span data-ttu-id="99c97-117">*bstrPhysicalAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c97-117">*bstrPhysicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c97-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="99c97-118">Type: **BSTR**</span></span>

<span data-ttu-id="99c97-119">Dirección física del elemento que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="99c97-119">The physical address of the item that changed.</span></span>

</dd> <dt>

<span data-ttu-id="99c97-120">*bstrLogicalAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="99c97-120">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c97-121">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="99c97-121">Type: **BSTR**</span></span>

<span data-ttu-id="99c97-122">Dirección lógica del elemento que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="99c97-122">The logical address of the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99c97-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99c97-123">Return value</span></span>

<span data-ttu-id="99c97-124">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="99c97-124">This method does not return a value.</span></span>

 

 
