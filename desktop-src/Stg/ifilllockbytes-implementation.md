---
title: 'IFillLockBytes: implementación'
description: El sistema proporciona una implementación de IFillLockBytes como parte de la implementación de archivos compuestos.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd Stg , implementación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c095d32bf9a932062b527cd486ee518e099d8de0f0d859caf2f1143e68237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663025"
---
# <a name="ifilllockbytes---implementation"></a>IFillLockBytes: implementación

El sistema proporciona una [**implementación de IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) como parte de la implementación de archivos compuestos.

La descarga de código puede crear una instancia de un objeto de archivo compuesto asincrónico llamando a [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes). La descarga de código también puede crear una instancia de un objeto contenedor de matriz de bytes asincrónico en un archivo existente o una matriz de bytes llamando a la función [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) o a la función [**StgGetIFillLockBytesOnILockBytes.**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes)

## <a name="when-to-use"></a>Cuándo usar

Actualmente, los monikers de url son los únicos usuarios de la implementación de almacenamiento asincrónico COM.

## <a name="remarks"></a>Comentarios

Estos son los cuatro métodos de la [**implementación de IFillLockBytes.**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)

<dl> <dt>

<span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**
</dt> <dd>

Escribe un nuevo bloque de bytes al final de una matriz de bytes. El tamaño del bloque se especifica como un parámetro para [**FillAppend.**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend)

</dd> <dt>

<span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**
</dt> <dd>

Escribe un nuevo bloque de datos en una ubicación especificada de la matriz de bytes.

</dd> <dt>

<span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**
</dt> <dd>

Establece el tamaño de la matriz de bytes. Devuelve E \_ FAIL de las llamadas a [**ILockBytes::ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) que intentan acceder a los datos más allá del límite superior especificado por el método .

</dd> <dt>

<span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes::Terminate**
</dt> <dd>

Informa a la matriz de bytes de que se ha finalizado una descarga, ya sea correcta o incorrectamente.

</dd> </dl>

 

 




