---
title: 'ILockBytes: File-Based implementación'
description: Se implementa en un objeto de matriz de bytes subyacente a un objeto de almacenamiento de archivos compuestos COM y está diseñado para leer y escribir directamente en un archivo de disco.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Strctd Stg, implementaciones, basadas en archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3dcfd11562f6a023d1f77af44b51ff7016cb61afdb16f2e4d72f81114fc132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961814"
---
# <a name="ilockbytes---file-based-implementation"></a>ILockBytes: File-Based implementación

Se implementa en un objeto de matriz de bytes subyacente a un objeto de almacenamiento de archivos compuestos COM y está diseñado para leer y escribir directamente en un archivo de disco.

## <a name="when-to-use"></a>Cuándo usar

Se llama a los métodos de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) desde las implementaciones de archivos compuestos de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en el objeto de almacenamiento de archivos compuesto creado a través de una llamada a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), por lo que no es necesario llamarlos directamente.

## <a name="remarks"></a>Comentarios

Estos son los métodos de la implementación de [**File-Based ILockBytes.**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**
</dt> <dd>

Lee un bloque de bytes de un desplazamiento especificado al principio de la matriz de bytes.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**
</dt> <dd>

Escribe un bloque de bytes de un desplazamiento especificado al principio de la matriz de bytes.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**
</dt> <dd>

Garantiza que los búferes internos mantenidos por la implementación [**de ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) se escriben en el almacenamiento físico subyacente.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**
</dt> <dd>

Establece el tamaño de la matriz de bytes.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**
</dt> <dd>

El *parámetro dwLockTypes* se establece en LOCK ONLYONCE o LOCK EXCLUSIVE, lo que permitirá o restringirá el acceso \_ a las \_ regiones bloqueadas.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**
</dt> <dd>

Este método desbloquea la región bloqueada por [**ILockBytes::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**
</dt> <dd>

La implementación de [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) proporcionada por COM llama al método [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) para recuperar información sobre el objeto de matriz de bytes. Si no hay ningún nombre razonable para la matriz de bytes, el método **ILockBytes::Stat** proporcionado por COM devuelve **NULL** en el miembro **pwcsName** de la [**estructura STATSTG.**](/windows/win32/api/objidl/ns-objidl-statstg)

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




