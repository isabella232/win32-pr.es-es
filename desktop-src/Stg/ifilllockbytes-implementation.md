---
title: 'IFillLockBytes: implementación'
description: El sistema proporciona una implementación de IFillLockBytes como parte de la implementación de archivos compuestos.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd STG, implementación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58737d02e3e6bc2511670178825aef8cbe2dcc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994197"
---
# <a name="ifilllockbytes---implementation"></a><span data-ttu-id="7b16b-104">IFillLockBytes: implementación</span><span class="sxs-lookup"><span data-stu-id="7b16b-104">IFillLockBytes - Implementation</span></span>

<span data-ttu-id="7b16b-105">El sistema proporciona una implementación de [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) como parte de la implementación de archivos compuestos.</span><span class="sxs-lookup"><span data-stu-id="7b16b-105">The system provides an [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation as part of the Compound Files implementation.</span></span>

<span data-ttu-id="7b16b-106">La descarga de código puede crear una instancia de un objeto de archivo compuesto asincrónico llamando a [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span><span class="sxs-lookup"><span data-stu-id="7b16b-106">Downloading code can create an instance of an asynchronous Compound File object by calling [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span></span> <span data-ttu-id="7b16b-107">La descarga del código también puede crear una instancia de un objeto contenedor de matriz de bytes asincrónico en un archivo o una matriz de bytes existente llamando a la función [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) o a la función [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="7b16b-107">Downloading code can also create an instance of an asynchronous byte array wrapper object on an existing file or byte array by calling either the [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) function or the [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) function.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="7b16b-108">Cuándo usar</span><span class="sxs-lookup"><span data-stu-id="7b16b-108">When to Use</span></span>

<span data-ttu-id="7b16b-109">Actualmente, los monikers de dirección URL son los únicos usuarios de la implementación de almacenamiento asincrónico COM.</span><span class="sxs-lookup"><span data-stu-id="7b16b-109">Currently, URL monikers are the only users of the COM asynchronous storage implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b16b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b16b-110">Remarks</span></span>

<span data-ttu-id="7b16b-111">A continuación se muestran los cuatro métodos de la implementación de [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) .</span><span class="sxs-lookup"><span data-stu-id="7b16b-111">The following are the four methods of the [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation.</span></span>

<dl> <dt>

<span data-ttu-id="7b16b-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**</span><span class="sxs-lookup"><span data-stu-id="7b16b-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**</span></span>
</dt> <dd>

<span data-ttu-id="7b16b-113">Escribe un nuevo bloque de bytes en el final de una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="7b16b-113">Writes a new block of bytes to the end of a byte array.</span></span> <span data-ttu-id="7b16b-114">El tamaño del bloque se especifica como un parámetro de [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span><span class="sxs-lookup"><span data-stu-id="7b16b-114">The size of the block is specified as a parameter to [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span></span>

</dd> <dt>

<span data-ttu-id="7b16b-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**</span><span class="sxs-lookup"><span data-stu-id="7b16b-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**</span></span>
</dt> <dd>

<span data-ttu-id="7b16b-116">Escribe un nuevo bloque de datos en una ubicación especificada de la matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="7b16b-116">Writes a new block of data to a specified location in the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="7b16b-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**</span><span class="sxs-lookup"><span data-stu-id="7b16b-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**</span></span>
</dt> <dd>

<span data-ttu-id="7b16b-118">Establece el tamaño de la matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="7b16b-118">Sets the size of the byte array.</span></span> <span data-ttu-id="7b16b-119">Devuelve E \_ FAIL from llama a [**ILockBytes:: readatum**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) que intentan obtener acceso a los datos más allá del límite superior especificado por el método.</span><span class="sxs-lookup"><span data-stu-id="7b16b-119">Returns E\_FAIL from calls to [**ILockBytes::ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) that attempt to access data beyond the upper limit specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="7b16b-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes:: Terminate**</span><span class="sxs-lookup"><span data-stu-id="7b16b-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes::Terminate**</span></span>
</dt> <dd>

<span data-ttu-id="7b16b-121">Informa a la matriz de bytes de que se ha finalizado una descarga, ya sea correcta o incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="7b16b-121">Informs the byte array that a download has been terminated, either successfully or unsuccessfully.</span></span>

</dd> </dl>

 

 




