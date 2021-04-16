---
title: DownloadItem. tipo
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad Type recupera el tipo de la descarga.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem. Escriba Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cdcf21ce7443d7730d4a75518fb4749af0b9e52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699423"
---
# <a name="downloaditemtype"></a><span data-ttu-id="90758-106">DownloadItem. tipo</span><span class="sxs-lookup"><span data-stu-id="90758-106">DownloadItem.type</span></span>

> [!Note]  
> <span data-ttu-id="90758-107">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="90758-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="90758-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="90758-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="90758-109">La propiedad **Type** recupera el tipo de la descarga.</span><span class="sxs-lookup"><span data-stu-id="90758-109">The **type** property retrieves the type of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="90758-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90758-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a><span data-ttu-id="90758-111">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="90758-111">Possible Values</span></span>

<span data-ttu-id="90758-112">Esta propiedad es una **cadena** de solo lectura que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="90758-112">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="90758-113">Value</span><span class="sxs-lookup"><span data-stu-id="90758-113">Value</span></span>      | <span data-ttu-id="90758-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="90758-114">Description</span></span>                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90758-115">background</span><span class="sxs-lookup"><span data-stu-id="90758-115">background</span></span> | <span data-ttu-id="90758-116">(Solo Windows XP). La descarga se produce como un proceso en segundo plano a medida que el tiempo de procesador está disponible.</span><span class="sxs-lookup"><span data-stu-id="90758-116">(Windows XP only.) The download occurs as a background process as processor time becomes available.</span></span> <span data-ttu-id="90758-117">Los Estados de descarga se conservan incluso cuando se apaga Windows Media Player o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="90758-117">Download states persist even when Windows Media Player or Windows XP is shut down.</span></span> |
| <span data-ttu-id="90758-118">en tiempo real</span><span class="sxs-lookup"><span data-stu-id="90758-118">real time</span></span>  | <span data-ttu-id="90758-119">(Todos los sistemas operativos compatibles). La descarga se produce a la vez.</span><span class="sxs-lookup"><span data-stu-id="90758-119">(All supported operating systems.) The download occurs all at once.</span></span> <span data-ttu-id="90758-120">No se conservan los Estados de descarga entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="90758-120">No download states persist between sessions.</span></span>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="90758-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90758-121">Remarks</span></span>

<span data-ttu-id="90758-122">Cada tipo de descarga tiene ventajas y desventajas.</span><span class="sxs-lookup"><span data-stu-id="90758-122">Each type of download has advantages and disadvantages.</span></span> <span data-ttu-id="90758-123">La descarga en segundo plano permite al usuario continuar con otras tareas e incluso reiniciar Windows sin cancelar la descarga, pero tarda más tiempo en completarse para completar la descarga y solo es compatible con Windows XP.</span><span class="sxs-lookup"><span data-stu-id="90758-123">Background downloading allows the user to proceed to other tasks and even restart Windows without cancelling the download, but takes more time overall to complete the download and is only supported for Windows XP.</span></span> <span data-ttu-id="90758-124">La descarga en tiempo real tarda menos tiempo en completarse, pero requiere que el usuario finalice la descarga antes de cerrar Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="90758-124">Real-time downloading takes less time to complete, but requires the user to finish all downloading before closing Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="90758-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90758-125">Requirements</span></span>



| <span data-ttu-id="90758-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="90758-126">Requirement</span></span> | <span data-ttu-id="90758-127">Value</span><span class="sxs-lookup"><span data-stu-id="90758-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90758-128">Versión</span><span class="sxs-lookup"><span data-stu-id="90758-128">Version</span></span><br/> | <span data-ttu-id="90758-129">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="90758-129">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="90758-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="90758-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="90758-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90758-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90758-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="90758-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90758-133">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="90758-133">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





