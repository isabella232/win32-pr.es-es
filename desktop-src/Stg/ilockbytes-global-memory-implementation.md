---
title: 'ILockBytes: implementación de memoria global'
description: La implementación de memoria global de ILockBytes se implementa en un objeto de matriz de bytes subyacente a un objeto de almacenamiento de archivos compuestos COM y está diseñado para leer y escribir directamente en la memoria global.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd Stg, implementaciones, memoria global
- ILockBytes Strctd Stg , implementaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30f9786f29433bcc02e0b56f3ea9d45c949593f60962e80a650d80ed625da41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867456"
---
# <a name="ilockbytes---global-memory-implementation"></a>ILockBytes: implementación de memoria global

La implementación de memoria global de ILockBytes se implementa en un objeto de matriz de bytes subyacente a un objeto de almacenamiento de archivos compuestos COM y está diseñado para leer y escribir directamente en la memoria global.

## <a name="when-to-use"></a>Cuándo usar

Se llama a los métodos de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) desde las implementaciones de archivos compuestos de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en el objeto de almacenamiento de archivos compuesto creado a través de una llamada a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).

## <a name="remarks"></a>Comentarios

Estos son los métodos de la implementación de memoria global [**de ILockBytes.**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**
</dt> <dd>

Lee un bloque de bytes de un desplazamiento especificado al principio de la matriz de bytes.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**
</dt> <dd>

Escribe el bloque de bytes de un desplazamiento especificado al principio de la matriz de bytes.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**
</dt> <dd>

A diferencia de la implementación basada en archivos, llamar a este método en la implementación de memoria global no tiene ningún efecto.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**
</dt> <dd>

Establece el tamaño de la matriz de bytes.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**
</dt> <dd>

Esta implementación no admite el bloqueo, por lo *que dwLocksType* se establece en cero. El autor de la llamada debe asegurarse de que los accesos son válidos y mutuamente excluyentes.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**
</dt> <dd>

Esta implementación no admite el bloqueo.

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**
</dt> <dd>

La implementación de [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) proporcionada por COM llama al método [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) para recuperar datos sobre el objeto de matriz de bytes. Si no hay ningún nombre razonable para la matriz de bytes, el método **ILockBytes::Stat** proporcionado por COM devuelve **NULL** en el miembro **pwcsName** de la [**estructura STATSTG.**](/windows/win32/api/objidl/ns-objidl-statstg)

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




