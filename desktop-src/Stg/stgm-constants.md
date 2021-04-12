---
title: Constantes STGM (ObjBase. h)
description: Marcas que indican las condiciones para crear y eliminar los modos de acceso y objeto del objeto.
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd283c2dfeddc48b6bd12f8317ec352cb62e4973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489371"
---
# <a name="stgm-constants"></a>Constantes de STGM

Las constantes STGM son marcas que indican las condiciones para crear y eliminar los modos de acceso y objeto del objeto. Las constantes STGM se incluyen en las interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)y [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y en las funciones [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)y [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) .

Estos elementos se combinan a menudo con un operador **or**. Se interpretan en grupos, tal y como se muestra en la tabla siguiente. No es válido usar más de un elemento de un solo grupo.

Use una marca del grupo de creación al crear un objeto, como con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).

Para obtener más información sobre la transacción, vea la sección Comentarios.



| Grupo                      | Marca                         | Value       |
|----------------------------|------------------------------|-------------|
| Access                     | **STGM \_ lectura**               | 0x00000000L |
|                            | **escritura de STGM \_**              | 0x00000001L |
|                            | **STGM \_ ReadWrite**          | 0x00000002L |
| Uso compartido                    | **STGM \_ recurso compartido \_ denegar \_ ninguno**  | 0x00000040L |
|                            | **STGM \_ recurso compartido de \_ lectura denegado \_**  | 0x00000030L |
|                            | **STGM \_ recurso compartido \_ denegar \_ escritura** | 0x00000020L |
|                            | **STGM \_ recurso compartido \_ exclusivo**   | 0x00000010L |
|                            | **prioridad de STGM \_**           | 0x00040000L |
| Creación                   | **\_crear STGM**             | 0x00001000L |
|                            | **STGM \_ convertir**            | 0x00020000L |
|                            | **STGM \_ FAILIFTHERE**        | 0x00000000L |
| Transaccional             | **STGM \_ directo**             | 0x00000000L |
|                            | **STGM \_ transacción**         | 0x00010000L |
| Rendimiento de la transacción | **STGM \_ NOscratch**          | 0x00100000L |
|                            | **STGM \_ NOsnapshot**         | 0x00200000L |
| Direct SWMR y simple     | **STGM \_ simple**             | 0x08000000L |
|                            | **STGM \_ Direct \_ SWMR**       | 0x00400000L |
| Eliminar en la versión          | **STGM \_ DELETEONRELEASE**    | 0x04000000L |



 

<dl> <dt>

<span id="STGM_READ"></span><span id="stgm_read"></span>**STGM \_ lectura**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Indica que el objeto es de solo lectura, lo que significa que no se pueden realizar modificaciones. Por ejemplo, si se abre un objeto de flujo con **STGM \_ Read**, se puede llamar al método [**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) , pero es posible que el método [**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) no lo sea. Del mismo modo, si se abre un objeto de almacenamiento con **STGM \_ Read**, se puede llamar a los métodos [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) y [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , pero los métodos [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) y [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) no pueden.


</dt> </dl> </dd> <dt>

<span id="STGM_WRITE"></span><span id="stgm_write"></span>**escritura de STGM \_**
</dt> <dd> <dl> <dt>

0x00000001L
</dt> <dt>



Permite guardar los cambios realizados en el objeto, pero no permite el acceso a sus datos. Las implementaciones proporcionadas de las interfaces [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) y [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) no admiten este modo de solo escritura.


</dt> </dl> </dd> <dt>

<span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM \_ ReadWrite**
</dt> <dd> <dl> <dt>

0x00000002L
</dt> <dt>



Habilita el acceso y la modificación de los datos de objeto. Por ejemplo, si se crea o se abre un objeto de flujo en este modo, es posible llamar a las dos [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) y **IStream:: Write**. Tenga en cuenta que esta constante no es un simple binario **u** operación de los elementos **STGM \_ Write** y **STGM \_ Read** .


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM \_ recurso compartido \_ denegar \_ ninguno**
</dt> <dd> <dl> <dt>

0x00000040L
</dt> <dt>



Especifica que no se deniega el acceso de lectura o escritura a las aperturas posteriores del objeto. Si no se especifica ninguna marca del grupo de uso compartido, se presupone esta marca.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM \_ recurso compartido de \_ lectura denegado \_**
</dt> <dd> <dl> <dt>

0x00000030L
</dt> <dt>



Evita que otros usuarios abran posteriormente el objeto en el modo de **\_ lectura STGM** . Normalmente se usa en un objeto de almacenamiento raíz.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM \_ recurso compartido \_ denegar \_ escritura**
</dt> <dd> <dl> <dt>

0x00000020L
</dt> <dt>



Evita que otros usuarios abran posteriormente el objeto para el acceso de **STGM \_ Write** o **STGM \_ ReadWrite** . En el modo de transacción, el uso compartido de **STGM \_ share \_ denegar \_ escritura** o el **\_ recurso compartido de STGM \_ exclusivo** puede mejorar significativamente el rendimiento porque no requieren instantáneas. Para obtener más información sobre la transacción, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM \_ recurso compartido \_ exclusivo**
</dt> <dd> <dl> <dt>

0x00000010L
</dt> <dt>



Evita que otros usuarios abran posteriormente el objeto en cualquier modo. Tenga en cuenta que este valor no es **una operación OR** bit a bit simple de los valores de lectura de los recursos compartidos **STGM \_ \_ \_ Read** y **STGM \_ share \_ Deny \_** . En el modo de transacción, el uso compartido de **STGM \_ share \_ denegar \_ escritura** o el **\_ recurso compartido de STGM \_ exclusivo** puede mejorar significativamente el rendimiento porque no requieren instantáneas. Para obtener más información sobre la transacción, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**prioridad de STGM \_**
</dt> <dd> <dl> <dt>

0x00040000L
</dt> <dt>



Abre el objeto de almacenamiento con acceso exclusivo a la versión confirmada más recientemente. Por lo tanto, otros usuarios no pueden confirmar los cambios en el objeto mientras está abierto en modo de prioridad. Obtiene ventajas de rendimiento para las operaciones de copia, pero impide que otros confirmen los cambios. Limite el tiempo que los objetos están abiertos en modo de prioridad. Debe especificar **STGM \_ Direct** y **STGM \_ Read** con el modo Priority y no puede especificar **STGM \_ DELETEONRELEASE**. **STGM \_ DELETEONRELEASE** solo es válido cuando se crea un objeto raíz, como con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). No es válido cuando se abre un objeto raíz existente, como con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex). Tampoco es válido al crear o abrir un subelemento, como con [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).


</dt> </dl> </dd> <dt>

<span id="STGM_CREATE"></span><span id="stgm_create"></span>**\_crear STGM**
</dt> <dd> <dl> <dt>

0x00001000L
</dt> <dt>



Indica que se debe quitar un objeto o secuencia de almacenamiento existente antes de que el nuevo objeto lo reemplace. Cuando se especifica este marcador, se crea un nuevo objeto solo si el objeto existente se ha quitado correctamente.

Esta marca se usa al intentar crear:

-   Un objeto de almacenamiento en un disco, pero existe un archivo con ese nombre.
-   Un objeto dentro de un objeto de almacenamiento, pero existe un objeto con el nombre especificado.
-   Objeto de matriz de bytes, pero existe uno con el nombre especificado.

Esta marca no se puede usar con operaciones de apertura, como [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) o [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).


</dt> </dl> </dd> <dt>

<span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ convertir**
</dt> <dd> <dl> <dt>

0x00020000L
</dt> <dt>



Crea el nuevo objeto conservando los datos existentes en una secuencia denominada "contents". En el caso de un objeto de almacenamiento o una matriz de bytes, se da formato a los datos antiguos en una secuencia, independientemente de si el archivo o la matriz de bytes existentes contiene actualmente un objeto de almacenamiento en capas. Esta marca solo se puede usar al crear un objeto de almacenamiento raíz. No se puede usar dentro de un objeto de almacenamiento. por ejemplo, en [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Tampoco es válido usar esta marca y la marca **STGM \_ DELETEONRELEASE** simultáneamente.


</dt> </dl> </dd> <dt>

<span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FAILIFTHERE**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Hace que se produzca un error en la operación de creación si existe un objeto con el nombre especificado. En este caso, se devuelve **STG \_ E \_ FILEALREADYEXISTS** . Este es el modo de creación predeterminado; es decir, si no se especifica ninguna otra marca Create, se implica **STGM \_ FAILIFTHERE** .


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ directo**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Indica que, en modo directo, cada cambio en un elemento de almacenamiento o de secuencia se escribe a medida que se produce. Este es el valor predeterminado si no se especifica **STGM \_ Direct** ni **STGM \_ transaccionad** .


</dt> </dl> </dd> <dt>

<span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ transacción**
</dt> <dd> <dl> <dt>

0x00010000L
</dt> <dt>



Indica que, en el modo de transacción, los cambios se almacenan en búfer y se escriben solo si se llama a una operación de confirmación explícita. Para omitir los cambios, llame al método [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) en la interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)o [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . La implementación de archivo compuesto COM de **IStorage** no admite secuencias de transacción, lo que significa que las secuencias solo se pueden abrir en modo directo, y no se pueden revertir los cambios en ellas, pero se admiten los almacenamientos de transacciones. Las implementaciones de archivos compuestos, independientes y del sistema de archivos NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) de forma similar no admiten conjuntos de propiedades con transacciones simples, ya que estos conjuntos de propiedades se almacenan en secuencias. Sin embargo, se admite la transacción de conjuntos de propiedades no simples, que se pueden crear especificando la marca **PROPSETFLAG \_ nonsimple** en el parámetro *grfFlags* de [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).


</dt> </dl> </dd> <dt>

<span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOscratch**
</dt> <dd> <dl> <dt>

0x00100000L
</dt> <dt>



Indica que, en el modo de transacción, normalmente se utiliza un archivo temporal temporal para guardar las modificaciones hasta que se llama al método **commit** . La especificación de **STGM \_ noscratch** permite que la parte no utilizada del archivo original se use como espacio de trabajo en lugar de crear un nuevo archivo para ese propósito. Esto no afecta a los datos del archivo original y, en algunos casos, puede mejorar el rendimiento. No es válido especificar esta marca sin especificar también **STGM \_ transacción**, y esta marca solo se puede usar en una raíz abierta. Para obtener más información sobre el modo noscratch, consulte la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOsnapshot**
</dt> <dd> <dl> <dt>

0x00200000L
</dt> <dt>



Esta marca se usa al abrir un objeto de almacenamiento con **STGM \_ transaccionad** y sin **STGM \_ share \_** or **STGM \_ share \_ Deny \_ Write**. En este caso, la especificación de **STGM \_ nosnapshot** evita que la implementación proporcionada por el sistema cree una copia de instantánea del archivo. En su lugar, los cambios realizados en el archivo se escriben al final del archivo. No se recupera el espacio no utilizado a menos que se realice la consolidación durante la confirmación, y solo hay un escritor actual en el archivo. Cuando el archivo se abre en modo sin instantánea, no se puede realizar otra operación de apertura sin especificar **STGM \_ nosnapshot**. Esta marca solo se puede usar en una operación de apertura raíz. Para obtener más información sobre el modo nosnapshot, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ simple**
</dt> <dd> <dl> <dt>

0x08000000L
</dt> <dt>



Proporciona una implementación más rápida de un archivo compuesto en un caso limitado, pero que se usa con frecuencia. Para obtener más información, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ Direct \_ SWMR**
</dt> <dd> <dl> <dt>

0x00400000L
</dt> <dt>



Admite el modo directo para las operaciones de archivo de un solo escritor. Para obtener más información, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ DELETEONRELEASE**
</dt> <dd> <dl> <dt>

0x04000000L
</dt> <dt>



Indica que el archivo subyacente se va a destruir automáticamente cuando se libere el objeto de almacenamiento raíz. Esta característica es muy útil para crear archivos temporales. Esta marca solo se puede usar al crear un objeto raíz, como con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). No es válido al abrir un objeto raíz, como con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), o al crear o abrir un subelemento, como con [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Tampoco es válido usar esta marca y la marca de conversión STGM \_ simultáneamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Puede combinar estas marcas, pero solo puede elegir una marca de cada grupo de marcas relacionadas. Normalmente se debe especificar una marca de cada uno de los grupos de acceso y uso compartido para todas las funciones y métodos que usan estas constantes. Las marcas de otros grupos son opcionales.

### <a name="transacted-mode"></a>Modo de transacción

Cuando se especifica la marca **STGM \_ Direct**, solo se puede especificar una de las siguientes combinaciones de marcas de los grupos de acceso y uso compartido.

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

Tenga en cuenta que el modo directo está implicado por la ausencia de **STGM \_ transacción**. Es decir, si no se especifica **STGM \_ Direct** ni **STGM \_ transaccionad** , se supone **STGM \_ Direct** .

Cuando se especifica la marca de **\_ transacción STGM** , los objetos se crean o se abren en modo de transacción. En este modo, los cambios realizados en un objeto no se conservan hasta que se confirman. Por ejemplo, los cambios en un objeto de almacenamiento con transacciones no se conservan hasta que se llama al método [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) . Los cambios en este tipo de objeto de almacenamiento se perderán si se libera el objeto de almacenamiento (versión final) antes de que se llame al método **commit** , o bien, si se llama al método [**IStorage:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) .

Cuando se crea o se abre un objeto en modo de transacción, la implementación debe conservar los datos originales y las actualizaciones de estos datos, de modo que las actualizaciones se puedan revertir si es necesario. Normalmente, esto se realiza mediante la escritura de cambios en un área de borrador hasta que se confirman, o bien mediante la creación de una copia, denominada instantánea, de los datos confirmados más recientemente.

Cuando se abre un objeto de almacenamiento raíz en modo de transacción, la ubicación y el comportamiento de los datos Scratch y las copias de instantáneas se pueden controlar para optimizar el rendimiento con las marcas **\_ noscratch** y **STGM \_ nosnapshot** de STGM. (Un objeto de almacenamiento raíz se obtiene de, por ejemplo, la función [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) ; un objeto de almacenamiento obtenido del método [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) es un objeto de subalmacenamiento). Normalmente, los datos y las instantáneas temporales se almacenan en archivos temporales, independientes del almacenamiento.

El efecto de estas marcas depende del número de lectores o escritores que tengan acceso al almacenamiento raíz.

En el caso de "un solo escritor", se abre un objeto de almacenamiento en modo de transacción para el acceso de escritura y no puede haber ningún otro acceso al archivo. Es decir, el archivo se abre con **STGM \_ transaccionad**, Access of **STGM \_ Write** o **STGM \_ ReadWrite** y el uso compartido de **STGM \_ share \_ Exclusive**. En este caso, los cambios en el objeto de almacenamiento se escriben en el área de borrado. Cuando estos cambios se confirman, se copian en el almacenamiento original. Por lo tanto, si no se realiza ningún cambio realmente en el objeto de almacenamiento, no habrá ninguna transferencia de datos innecesaria.

En el caso de "varios escritores", se abre un objeto de almacenamiento con transacciones para el acceso de escritura, pero se comparte en tal asway como para permitir otros escritores. Es decir, el objeto de almacenamiento se abre **con \_ STGM transaccionad**, Access of **STGM \_ Write** o **STGM \_ ReadWrite** y el uso compartido de **STGM \_ share \_ Deny \_ Read**. Si en su lugar se especifica el uso compartido del **\_ recurso compartido STGM \_ denegar \_ ninguno** , el caso sería "varios escritores, varios lectores". En estos casos, se realizará una instantánea de los datos originales durante la operación de apertura. Por lo tanto, incluso si no se realiza ningún cambio en el almacenamiento y/o no se abre realmente por otro escritor simultáneamente, la transferencia de datos sigue siendo necesaria durante la apertura. Como resultado, se puede obtener el mejor rendimiento en tiempo de ejecución abriendo el objeto de almacenamiento en los modos **STGM \_ share \_ Deny \_ Write** o **STGM \_ share \_** . Para obtener más información sobre cómo se confirman los cambios cuando hay varios escritores, vea [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).

En el caso de "un solo escritor, varios lectores", se abre un objeto de almacenamiento con transacciones para el acceso de escritura, pero se comparte con los lectores. Es decir, el escritor abre el objeto de almacenamiento con **STGM \_ transaccionad**, el acceso **de STGM \_ ReadWrite** o **STGM \_ Write** y el uso compartido de **STGM \_ share \_ Deny \_ Write**. Los lectores abren el almacenamiento con **\_ transacciones de STGM**, el acceso de **STGM \_ Read** y el uso compartido **del \_ recurso compartido STGM no \_ deniega \_ ninguno**. En este caso, el escritor usa el área de borrado para almacenar los cambios no confirmados. Como en los casos anteriores, el lector incurre en una penalización de rendimiento de tiempo abierto mientras se crea una copia de instantánea de los datos.

Normalmente, el área de borrado es un archivo temporal, independiente de los datos originales. Cuando los cambios se confirman en el archivo original, los datos se deben transferir desde el archivo temporal. Para evitar esta transferencia de datos, se puede especificar la marca **STGM \_ noscratch**. Cuando se especifica esta marca, se usan partes del archivo de objeto de almacenamiento para el área de borrado, en lugar de un archivo temporal independiente. Como resultado, la confirmación de los cambios puede realizarse rápidamente, ya que se requiere poca transferencia de datos. El inconveniente es que el archivo de almacenamiento puede ser mayor de lo que, en caso contrario, debe aumentarse para que sea lo suficientemente grande como para los datos originales y el área de borrado. Para consolidar los datos y quitar este área innecesaria, vuelva a abrir el almacenamiento raíz en modo de transacción, pero sin establecer la marca **STGM \_ noscratch** . A continuación, llame a [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) con el marcador de **STGC \_ ConsoliDate** establecido.

El área de instantáneas, como el área de borrador, también es, normalmente, un archivo temporal, y esto también puede verse afectado por una marca STGM. Al especificar la marca **STGM \_ nosnapshot** , no se crea un archivo de instantánea temporal independiente. En su lugar, los datos originales nunca se modifican, incluso si hay uno o más escritores por objeto. Cuando se confirman los cambios, se agregan al archivo, pero los datos originales permanecen intactos. Este modo aumenta la eficacia, ya que reduce el tiempo de ejecución eliminando el requisito de crear una instantánea durante la operación de apertura. Sin embargo, el uso de este modo puede dar lugar a un archivo de almacenamiento muy grande, ya que los datos del archivo no se pueden sobrescribir nunca. No es límite para el tamaño de los archivos abiertos en el modo nosnapshot.

### <a name="direct-single-writer-multiple-reader-mode"></a>Un solo escritor directo, modo de Multiple-Reader

Tal como se describe, es posible tener un solo escritor y varios lectores de un objeto de almacenamiento, si ese objeto está abierto en modo de transacción. También es posible lograr el caso de un solo escritor y MultiRead en modo directo, especificando la marca **STGM \_ Direct \_ SWMR** .

En el modo **STGM \_ Direct \_ SWMR** , es posible que un llamador abra un objeto para el acceso de lectura y escritura, mientras que otros llamadores tienen el archivo abierto al mismo tiempo para el acceso de solo lectura. No es válido usar esta marca en combinación con la marca de **\_ transacción STGM** . En este modo, el escritor abre el objeto con las marcas siguientes:

**STGM \_ Direct \_ SWMR** \| **STGM \_ ReadWrite** \| **STGM \_ recurso compartido \_ DENYWRITE**

y cada uno de los lectores abre el objeto con estas marcas:

**STGM \_ Direct \_ SWMR** \| **STGM \_ Read** \| **STGM \_ share \_ denegar \_ ninguno**

En este modo, para modificar el objeto de almacenamiento, el escritor debe obtener acceso exclusivo al objeto. Esto es posible cuando todos los lectores la han cerrado. El escritor usa la interfaz [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) para obtener este acceso exclusivo.

### <a name="simple-mode"></a>Modo simple

El modo simple (**STGM \_ simple**) es útil para las aplicaciones que realizan operaciones de guardado completas. Es eficaz, pero tiene las siguientes restricciones:

-   No existe compatibilidad para los subalmacenamientos.
-   No se pueden calcular las referencias del objeto de almacenamiento y de los objetos de secuencia obtenidos de él.
-   Cada flujo tiene un tamaño mínimo. Si se escriben menos bytes como mínimo en una secuencia cuando se libera la secuencia, la secuencia se extiende al tamaño mínimo. Por ejemplo, el tamaño mínimo de una implementación de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) determinada es de 4 KB. Se crea un flujo y se escribe 1 KB en él. En el lanzamiento final de esa **IStream**, el tamaño de la secuencia se extenderá automáticamente a 4 KB. Posteriormente, al abrir la secuencia y llamar al método [**IStream:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) , se mostrará un tamaño de 4 KB.
-   No todos los métodos de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) serán compatibles con la implementación de. Para obtener más información, vea [implementación de archivos compuestos de IStorage](istorage-compound-file-implementation.md)e [implementación de archivos compuestos de IStream](istream-compound-file-implementation.md).

El [cálculo de referencias](/windows/desktop/Midl/marshaling-ole-data-types) es el proceso de empaquetar, desempaquetar y enviar parámetros de método de interfaz a través de los límites de subprocesos o procesos dentro de una llamada a procedimiento remoto (RPC). Para obtener más información, vea Serialización de [detalles](../com/marshaling-details.md) y [serialización](../com/interface-marshaling.md)de la interfaz.

Cuando una operación de creación obtiene un objeto de almacenamiento en modo simple:

-   Los elementos de secuencia se pueden crear, pero no abrir.
-   Cuando se crea un elemento de secuencia mediante una llamada a [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), no es posible crear otro flujo hasta que se libere el objeto de secuencia.
-   Una vez que se escriben todas las secuencias, llame a [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) para vaciar los cambios.

Cuando una operación de apertura obtiene un objeto de almacenamiento en modo simple:

-   Es posible abrir un solo elemento de secuencia a la vez.
-   No es posible cambiar el tamaño de una secuencia llamando al método [**IStream:: setSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) o buscando o escribiendo más allá del final de la secuencia. Sin embargo, dado que todos los flujos tienen un tamaño mínimo, es posible usar el flujo hasta ese tamaño, aunque se hayan escrito menos datos en él. Para determinar el tamaño de una secuencia, use el método [**IStream:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) .

Tenga en cuenta que, si un objeto de almacenamiento modifica un elemento de almacenamiento que no está en modo simple, no será posible, de nuevo, abrir ese elemento de almacenamiento en modo simple.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>ObjBase. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[**StgOpenStorageOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

