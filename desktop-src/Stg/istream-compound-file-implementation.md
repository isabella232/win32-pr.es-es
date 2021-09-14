---
title: 'IStream: implementación de archivos compuestos'
description: La interfaz IStream admite la lectura y escritura de datos para transmitir objetos. En un objeto de almacenamiento estructurado, los objetos de secuencia contienen los datos y los almacenamientos proporcionan la estructura .
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd Stg , implementación de archivos compuestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068918"
---
# <a name="istream---compound-file-implementation"></a>IStream: implementación de archivos compuestos

La [**interfaz IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) admite la lectura y escritura de datos para transmitir objetos. En un objeto de almacenamiento estructurado, los objetos de secuencia contienen los datos y los almacenamientos proporcionan la estructura . Los datos simples se pueden escribir directamente en una secuencia, pero con más frecuencia, las secuencias son elementos anidados dentro de un objeto de almacenamiento. Son similares a los archivos estándar.

La especificación [**de IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) define más funcionalidad de la que admite la implementación com. Por ejemplo, la **interfaz IStream** define secuencias de hasta 2⁶⁴ bytes de longitud que requieren un puntero de búsqueda de 64 bits. Sin embargo, la implementación com solo admite secuencias de hasta 2 bytes de longitud (4 GB) y las operaciones de lectura y escritura siempre están limitadas a 2 bytes a la vez. La implementación com tampoco admite transacciones de flujos ni bloqueos de regiones.

Para crear una secuencia simple basada en memoria global, obtenga un puntero [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) llamando a la función de API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal). Para obtener un **puntero IStream** dentro de un objeto de archivo compuesto, llame a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage). Estas funciones recuperan un [**puntero IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) con el que puede llamar a [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) o [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) para un **puntero IStream.** En cualquier caso, se usa el mismo código de implementación de **IStream.**

> [!Note]  
> La implementación de archivos compuestos del almacenamiento estructurado no se realiza correctamente [](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) en [](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) un método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), pero incluye los métodos de lectura y escritura a través del puntero de interfaz [**IStream.**](/windows/desktop/api/Objidl/nn-objidl-istream)

 

## <a name="when-to-use"></a>Cuándo usar

Llame a los métodos [**de IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para leer y escribir datos en una secuencia.

Dado que los objetos de secuencia se pueden serializar a otros procesos, las aplicaciones pueden compartir los datos en objetos de almacenamiento sin tener que usar memoria global. En la implementación de archivos compuestos COM de objetos de secuencia, las instalaciones de serialización personalizadas de COM crean una versión remota del objeto original en el nuevo proceso cuando los dos procesos tienen acceso a memoria compartida. Por lo tanto, la versión remota no necesita comunicarse con el proceso original para llevar a cabo sus funciones.

La versión remota del objeto de secuencia comparte el mismo puntero de búsqueda que la secuencia original. Si no desea compartir el puntero de búsqueda, use el método [**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) para proporcionar una copia del objeto de secuencia para el proceso remoto.

> [!Note]
> Si crea un objeto de secuencia mayor que el montón en la memoria del equipo y usa un identificador **HGLOBAL** para un objeto de memoria global, el objeto de secuencia llama al método [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) internamente para que requiera más memoria. Dado **que GlobalRealloc** siempre copia datos del origen al destino, aumentar un objeto de secuencia de 20 MB a 25 MB, por ejemplo, requiere grandes cantidades de tiempo. Esto se debe al tamaño de los incrementos copiados y se aqueda si hay menos de 45 MB de memoria en el equipo debido al intercambio de disco.
>
> La solución preferida es implementar un [**método IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) que use la memoria asignada por [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) en lugar de [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc). Esto puede reservar un gran fragmento de espacio de direcciones virtuales y, a continuación, confirmar la memoria dentro de ese espacio de direcciones según sea necesario. No se produce ninguna copia de datos y la memoria solo se confirma cuando es necesaria.
>
> Una alternativa a [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) es llamar al método [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) en el objeto de secuencia para aumentar la asignación de memoria de antemano. Sin embargo, esto no es tan eficaz como usar [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), como se ha descrito anteriormente.

 

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dd>

Lee un número especificado de bytes del objeto de flujo en la memoria, empezando en el puntero de búsqueda actual. Esta implementación devuelve S \_ OK si se alcanzó el final de la secuencia durante la lectura. (Esto es lo mismo que el comportamiento de "fin de archivo" que se encuentra en el sistema de archivos FAT de MS-DOS).

</dd> <dt>

<span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)
</dt> <dd>

Escribe un número especificado de bytes en el objeto de secuencia a partir del puntero de búsqueda actual. En esta implementación, los objetos de secuencia no son dispersos. Los bytes de relleno se asignan finalmente en el disco y se asignan a la secuencia.

</dd> <dt>

<span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream::Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)
</dt> <dd>

Cambia el puntero de búsqueda a una nueva ubicación respecto al principio del flujo, al final del flujo o al puntero de búsqueda actual.

</dd> <dt>

<span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)
</dt> <dd>

Cambia el tamaño del objeto de secuencia. En esta implementación, no hay ninguna garantía de que el espacio asignado será contiguo.

</dd> <dt>

<span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
</dt> <dd>

Copia un número especificado de bytes del puntero de búsqueda actual del flujo en el puntero de búsqueda actual de otro flujo.

</dd> <dt>

<span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream::Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)
</dt> <dd>

La implementación de archivo compuesto [**de IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) admite la apertura de secuencias solo en modo directo, no en modo de transacción. Por lo tanto, el método no tiene ningún efecto cuando se llama a que no sea vaciar todos los búferes de memoria en el siguiente nivel de almacenamiento.

En esta implementación, no importa si confirma cambios en secuencias, solo necesita confirmar los cambios para los objetos de almacenamiento.

</dd> <dt>

<span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream::Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)
</dt> <dd>

Esta implementación no admite secuencias con transacciones, por lo que una llamada a este método no tiene ningún efecto.

</dd> <dt>

<span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)
</dt> <dd>

Esta implementación no admite el bloqueo de intervalos, por lo que una llamada a este método no tiene ningún efecto.

</dd> <dt>

<span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream::UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)
</dt> <dd>

Quita la restricción de acceso en un intervalo de bytes previamente restringido con [**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).

</dd> <dt>

<span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)
</dt> <dd>

Recupera la estructura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) para esta secuencia.

</dd> <dt>

<span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)
</dt> <dd>

Crea un nuevo objeto de flujo con su propio puntero de búsqueda que hace referencia a los mismos bytes que el flujo original.

</dd> </dl>

Un [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en modo simple está sujeto a las restricciones siguientes.

-   Una secuencia es un modo simple si se creó o abrió desde un almacenamiento en modo simple. Un almacenamiento es un modo simple si se crea o abre con la marca SIMPLE de STGM \_ establecida en el parámetro *grfMode.*
-   No [**se admiten**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) los métodos Clone y [**CopyTo.**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
-   Se admite el método [**Stat,**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) pero se debe especificar el valor \_ STATFLAG NONAME.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 