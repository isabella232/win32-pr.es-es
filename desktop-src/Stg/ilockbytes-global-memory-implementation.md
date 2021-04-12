---
title: 'ILockBytes: implementación de memoria global'
description: La implementación de memoria global ILockBytes se implementa en un objeto de matriz de bytes subyacente de un objeto de almacenamiento de archivos compuesto COM y está diseñado para leer y escribir directamente en la memoria global.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd STG, implementaciones, memoria global
- ILockBytes Strctd STG, implementaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d7cae82c1503fcb53d2cfd8fee39095eb60801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356819"
---
# <a name="ilockbytes---global-memory-implementation"></a>ILockBytes: implementación de memoria global

La implementación de memoria global ILockBytes se implementa en un objeto de matriz de bytes subyacente de un objeto de almacenamiento de archivos compuesto COM y está diseñado para leer y escribir directamente en la memoria global.

## <a name="when-to-use"></a>Cuándo usar

Se llama a los métodos de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) desde las implementaciones de archivos compuestos de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) y [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en el objeto de almacenamiento de archivos compuesto creado a través de una llamada a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).

## <a name="remarks"></a>Observaciones

A continuación se muestran los métodos de la implementación de memoria global [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: readatum**
</dt> <dd>

Lee un bloque de bytes de un desplazamiento especificado al principio de la matriz de bytes.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: WriteAt**
</dt> <dd>

Escribe el bloque de bytes desde un desplazamiento especificado al principio de la matriz de bytes.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**
</dt> <dd>

A diferencia de la implementación basada en archivo, llamar a este método en la implementación de memoria global no tiene ningún efecto.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: setSize**
</dt> <dd>

Establece el tamaño de la matriz de bytes.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**
</dt> <dd>

Esta implementación no admite el bloqueo, por lo que *dwLocksType* se establece en cero. El autor de la llamada debe asegurarse de que los accesos son válidos y mutuamente excluyentes.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**
</dt> <dd>

Esta implementación no admite el bloqueo.

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: Stat**
</dt> <dd>

La implementación [**IStorage:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) proporcionada por com llama al método [**ILockBytes:: Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) para recuperar datos sobre el objeto de matriz de bytes. Si no hay un nombre razonable para la matriz de bytes, el método **ILockBytes:: Stat** proporcionado por com devuelve **null** en el miembro **pwcsName** de la estructura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




