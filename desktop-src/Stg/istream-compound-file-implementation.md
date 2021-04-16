---
title: Implementación de archivos compuestos de IStream
description: La interfaz IStream permite leer y escribir datos en objetos de secuencia. En un objeto de almacenamiento estructurado, los objetos Stream contienen los datos y los almacenamientos proporcionan la estructura.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd STG, implementación de archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105670045"
---
# <a name="istream---compound-file-implementation"></a>Implementación de archivos compuestos de IStream

La interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) permite leer y escribir datos en objetos de secuencia. En un objeto de almacenamiento estructurado, los objetos Stream contienen los datos y los almacenamientos proporcionan la estructura. Los datos simples se pueden escribir directamente en una secuencia, pero con más frecuencia, las secuencias son elementos anidados dentro de un objeto de almacenamiento. Son similares a los archivos estándar.

La especificación de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) define más funcionalidad de la que admite la implementación de com. Por ejemplo, la interfaz **IStream** define las secuencias hasta 2 ⁶ ⁴ bytes de longitud que requieren un puntero de búsqueda de 64 bits. Sin embargo, la implementación COM solo admite secuencias de hasta 2 ³ ² bytes de longitud (4 GB) y las operaciones de lectura y escritura siempre están limitadas a 2 ³ ² bytes a la vez. La implementación COM tampoco admite el bloqueo de la transacción o de la región.

Para crear una secuencia simple basada en la memoria global, obtenga un puntero [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) llamando a la función de API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal). Para obtener un puntero **IStream** dentro de un objeto de archivo compuesto, llame a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage). Estas funciones recuperan un puntero [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , con el que se puede llamar a [**CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) o [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) para un puntero **IStream** . En cualquier caso, se usa el mismo código de implementación de **IStream** .

> [!Note]  
> La implementación de archivos compuestos de almacenamiento estructurado no se realiza correctamente en un método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), pero incluye los métodos de [**lectura**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) y [**escritura**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) a través del puntero de interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .

 

## <a name="when-to-use"></a>Cuándo usar

Llame a los métodos de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para leer y escribir datos en una secuencia.

Dado que los objetos de secuencia se pueden serializar en otros procesos, las aplicaciones pueden compartir los datos de los objetos de almacenamiento sin tener que usar la memoria global. En la implementación de archivo compuesto COM de objetos de secuencia, las funciones personalizadas de serialización en COM crean una versión remota del objeto original en el nuevo proceso cuando los dos procesos tienen acceso de memoria compartida. Por lo tanto, la versión remota no necesita comunicarse con el proceso original para llevar a cabo sus funciones.

La versión remota del objeto de secuencia comparte el mismo puntero de búsqueda que la secuencia original. Si no desea compartir el puntero de búsqueda, use el método [**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) para proporcionar una copia del objeto de secuencia para el proceso remoto.

> [!Note]
> Si se crea un objeto de secuencia que es mayor que el montón en la memoria del equipo y se utiliza un identificador **HGLOBAL** para un objeto de memoria global, el objeto de secuencia llama al método [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) internamente al requiere más memoria. Dado que **GlobalRealloc** siempre copia los datos del origen en el destino, el aumento de un objeto de secuencia de 20 MB a 25 MB, por ejemplo, requiere una gran cantidad de tiempo. Esto se debe al tamaño de los incrementos copiados y se empeora si hay menos de 45 MB de memoria en el equipo debido al intercambio de disco.
>
> La solución preferida consiste en implementar un método [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) que use la memoria asignada por [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) en lugar de [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc). Esto puede reservar un gran fragmento de espacio de direcciones virtuales y, a continuación, confirmar la memoria dentro de ese espacio de direcciones según sea necesario. No se realiza la copia de datos y la memoria se confirma solo cuando es necesario.
>
> Una alternativa a [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) es llamar al método [**IStream:: setSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) en el objeto de secuencia para aumentar la asignación de memoria de antemano. Sin embargo, esto no es tan eficaz como el uso de [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), como se describió anteriormente.

 

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dd>

Lee un número especificado de bytes del objeto de flujo en la memoria, empezando en el puntero de búsqueda actual. Esta implementación devuelve \_ si se alcanzó el final de la secuencia durante la lectura. (Esto es lo mismo que el comportamiento de "fin de archivo" que se encuentra en el sistema de archivos FAT de MS-DOS).

</dd> <dt>

<span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)
</dt> <dd>

Escribe un número especificado de bytes en el objeto de flujo, empezando en el puntero de búsqueda actual. En esta implementación, los objetos de secuencia no son dispersos. Los bytes de relleno se asignan finalmente en el disco y se asignan a la secuencia.

</dd> <dt>

<span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream:: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)
</dt> <dd>

Cambia el puntero de búsqueda a una nueva ubicación respecto al principio del flujo, al final del flujo o al puntero de búsqueda actual.

</dd> <dt>

<span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream:: setSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)
</dt> <dd>

Cambia el tamaño del objeto de secuencia. En esta implementación, no hay ninguna garantía de que el espacio asignado sea contiguo.

</dd> <dt>

<span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
</dt> <dd>

Copia un número especificado de bytes del puntero de búsqueda actual del flujo en el puntero de búsqueda actual de otro flujo.

</dd> <dt>

<span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream:: commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)
</dt> <dd>

La implementación de archivo compuesto de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) admite la apertura de secuencias solo en modo directo, no en modo de transacción. Por lo tanto, el método no tiene ningún efecto cuando se llama a otro para vaciar todos los búferes de memoria en el siguiente nivel de almacenamiento.

En esta implementación, no importa si confirma los cambios en los flujos, solo necesita confirmar los cambios de los objetos de almacenamiento.

</dd> <dt>

<span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream:: revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)
</dt> <dd>

Esta implementación no admite secuencias de transacción, por lo que una llamada a este método no tiene ningún efecto.

</dd> <dt>

<span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)
</dt> <dd>

Esta implementación no admite el bloqueo de intervalo, por lo que una llamada a este método no tiene ningún efecto.

</dd> <dt>

<span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream:: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)
</dt> <dd>

Quita la restricción de acceso de un intervalo de bytes previamente restringido con [**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).

</dd> <dt>

<span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)
</dt> <dd>

Recupera la estructura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) para esta secuencia.

</dd> <dt>

<span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)
</dt> <dd>

Crea un nuevo objeto de flujo con su propio puntero de búsqueda que hace referencia a los mismos bytes que el flujo original.

</dd> </dl>

Una [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) de modo simple está sujeta a las siguientes restricciones.

-   Una secuencia es un modo simple si se ha creado o abierto desde un almacenamiento de modo simple. Un almacenamiento es un modo sencillo si se crea o se abre con la \_ marca de STGM simple establecida en el parámetro *grfMode* .
-   No se admiten los métodos [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) y [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) .
-   Se admite el método [**STAT**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) , pero \_ se debe especificar el valor Noname de STATFLAG.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 