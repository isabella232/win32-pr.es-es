---
title: DownloadCollection.id
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. La propiedad ID recupera el identificador de la colección de descargas.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.id Windows Media Player
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9edcca4f56c485951ca907ae228dfec7a958b308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700350"
---
# <a name="downloadcollectionid"></a><span data-ttu-id="07170-106">DownloadCollection.id</span><span class="sxs-lookup"><span data-stu-id="07170-106">DownloadCollection.id</span></span>

> [!Note]  
> <span data-ttu-id="07170-107">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="07170-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="07170-108">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="07170-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="07170-109">La propiedad **ID** recupera el identificador de la colección de descargas.</span><span class="sxs-lookup"><span data-stu-id="07170-109">The **id** property retrieves the ID of the download collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="07170-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07170-110">Syntax</span></span>

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a><span data-ttu-id="07170-111">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="07170-111">Possible Values</span></span>

<span data-ttu-id="07170-112">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="07170-112">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="07170-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07170-113">Remarks</span></span>

<span data-ttu-id="07170-114">Cuando el administrador de descargas crea una nueva colección de descargas, asigna un número de identificador a la colección.</span><span class="sxs-lookup"><span data-stu-id="07170-114">When the Download Manager creates a new download collection, it assigns the collection an ID number.</span></span> <span data-ttu-id="07170-115">Los números de ID. se conservan entre las sesiones de Windows Media Player y las sesiones del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="07170-115">ID numbers persist between Windows Media Player sessions and operating system sessions.</span></span>

<span data-ttu-id="07170-116">Los números de ID. no son únicos.</span><span class="sxs-lookup"><span data-stu-id="07170-116">ID numbers are not unique.</span></span> <span data-ttu-id="07170-117">Sin embargo, hay suficientes números de identificador disponibles en el valor de 32 bits, por lo que es muy poco probable que un número de ID. existente se sobrescriba en uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="07170-117">However, there are enough ID numbers available in the 32-bit value that it is extremely unlikely that an existing ID number will ever be overwritten by a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="07170-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07170-118">Requirements</span></span>



| <span data-ttu-id="07170-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="07170-119">Requirement</span></span> | <span data-ttu-id="07170-120">Value</span><span class="sxs-lookup"><span data-stu-id="07170-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="07170-121">Versión</span><span class="sxs-lookup"><span data-stu-id="07170-121">Version</span></span><br/> | <span data-ttu-id="07170-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="07170-122">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="07170-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="07170-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="07170-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07170-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07170-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="07170-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07170-126">**Objeto DownloadCollection**</span><span class="sxs-lookup"><span data-stu-id="07170-126">**DownloadCollection Object**</span></span>](downloadcollection-object.md)
</dt> </dl>

 

 





