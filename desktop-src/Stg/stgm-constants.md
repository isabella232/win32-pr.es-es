---
title: Constantes STGM (ObjBase.h)
description: Marcas que indican las condiciones para crear y eliminar el objeto y los modos de acceso para el objeto.
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
ms.openlocfilehash: 18248e862c3d5981e9c34b29522b1cd75d2b61cf78a52613b3d28a1d2c98b4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661975"
---
# <a name="stgm-constants"></a>Constantes STGM

Las constantes STGM son marcas que indican condiciones para crear y eliminar el objeto y los modos de acceso para el objeto. Las constantes STGM se incluyen en las interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) y en las funciones [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) [**StgCreateDocfileOnILockBytes,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes) [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)y [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)

Estos elementos se combinan a menudo mediante un **operador OR.** Se interpretan en grupos como se muestra en la tabla siguiente. No es válido usar más de un elemento de un único grupo.

Use una marca del grupo de creación al crear un objeto, como [**con StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).

Para obtener más información sobre las transacciones, vea la sección Comentarios.



| Grupo                      | Marca                         | Value       |
|----------------------------|------------------------------|-------------|
| Acceso                     | **STGM \_ READ**               | 0x00000000L |
|                            | **STGM \_ WRITE**              | 0x00000001L |
|                            | **STGM \_ READWRITE**          | 0x00000002L |
| Uso compartido                    | **STGM \_ SHARE \_ DENY \_ NONE**  | 0x00000040L |
|                            | **STGM \_ SHARE \_ DENY \_ READ**  | 0x00000030L |
|                            | **ESCRITURA DE \_ DENEGACIÓN DE \_ RECURSO COMPARTIDO STGM \_** | 0x00000020L |
|                            | **STGM \_ SHARE \_ EXCLUSIVE**   | 0x00000010L |
|                            | **STGM \_ PRIORITY**           | 0x00040000L |
| Creación                   | **STGM \_ CREATE**             | 0x00001000L |
|                            | **STGM \_ CONVERT**            | 0x00020000L |
|                            | **STGM \_ FAILIFTHERE**        | 0x00000000L |
| Transacciones             | **STGM \_ DIRECT**             | 0x00000000L |
|                            | **STGM \_ TRANSACTED**         | 0x00010000L |
| Rendimiento de transacciones | **STGM \_ NOSCRATCH**          | 0x00100000L |
|                            | **STGM \_ NOSNAPSHOT**         | 0x00200000L |
| SWMR directo y simple     | **STGM \_ SIMPLE**             | 0x08000000L |
|                            | **STGM \_ DIRECT \_ SWMR**       | 0x00400000L |
| Eliminar en la versión          | **STGM \_ DELETEONRELEASE**    | 0x04000000L |



 

<dl> <dt>

<span id="STGM_READ"></span><span id="stgm_read"></span>**STGM \_ READ**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Indica que el objeto es de solo lectura, lo que significa que no se pueden realizar modificaciones. Por ejemplo, si se abre un objeto de secuencia con **STGM \_ READ**, se puede llamar al método [**ISequentialStream::Read,**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) pero es posible que no lo haga el método [**ISequentialStream::Write.**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) Del mismo modo, si se abre un objeto de almacenamiento con **STGM \_ READ**, se puede llamar a los métodos [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) e [**IStorage::OpenStorage,**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) pero es posible que los métodos [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) e [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) no lo sean.


</dt> </dl> </dd> <dt>

<span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM \_ WRITE**
</dt> <dd> <dl> <dt>

0x00000001L
</dt> <dt>



Permite guardar los cambios en el objeto , pero no permite el acceso a sus datos. Las implementaciones proporcionadas de [**las interfaces IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) [**e IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) no admiten este modo de solo escritura.


</dt> </dl> </dd> <dt>

<span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM \_ READWRITE**
</dt> <dd> <dl> <dt>

0x00000002L
</dt> <dt>



Habilita el acceso y la modificación de los datos del objeto. Por ejemplo, si se crea o se abre un objeto de secuencia en este modo, es posible llamar a [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) e **IStream::Write.** Tenga en cuenta que esta constante no es una operación **OR binaria** simple de los **elementos STGM \_ WRITE** y **STGM \_ READ.**


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM \_ SHARE \_ DENY \_ NONE**
</dt> <dd> <dl> <dt>

0x00000040L
</dt> <dt>



Especifica que no se deniega el acceso de lectura o escritura a las aperturas posteriores del objeto. Si no se especifica ninguna marca del grupo de uso compartido, se supone que esta marca.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM \_ SHARE \_ DENY \_ READ**
</dt> <dd> <dl> <dt>

0x00000030L
</dt> <dt>



Impide que otros usuarios abran posteriormente el objeto en **modo STGM \_ READ.** Normalmente se usa en un objeto de almacenamiento raíz.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**ESCRITURA DE \_ DENEGACIÓN DE \_ RECURSO COMPARTIDO STGM \_**
</dt> <dd> <dl> <dt>

0x00000020L
</dt> <dt>



Impide que otros usuarios abran posteriormente el objeto **para el acceso STGM \_ WRITE** o **STGM \_ READWRITE.** En el modo de transacción, el uso compartido de **STGM \_ SHARE DENY \_ \_ WRITE** o **STGM SHARE \_ \_ EXCLUSIVE** puede mejorar significativamente el rendimiento porque no requieren instantáneas. Para obtener más información sobre las transacciones, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM \_ SHARE \_ EXCLUSIVE**
</dt> <dd> <dl> <dt>

0x00000010L
</dt> <dt>



Impide que otros usuarios abran posteriormente el objeto en cualquier modo. Tenga en cuenta que este valor no es una operación **OR** bit a bit sencilla de los valores **STGM \_ SHARE DENY \_ \_ READ** y **STGM SHARE DENY \_ \_ \_ WRITE.** En el modo de transacción, el uso compartido de **STGM \_ SHARE DENY \_ \_ WRITE** o **STGM SHARE \_ \_ EXCLUSIVE** puede mejorar significativamente el rendimiento porque no requieren instantáneas. Para obtener más información sobre las transacciones, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM \_ PRIORITY**
</dt> <dd> <dl> <dt>

0x00040000L
</dt> <dt>



Abre el objeto de almacenamiento con acceso exclusivo a la versión más reciente que se ha confirmado. Por lo tanto, otros usuarios no pueden confirmar los cambios en el objeto mientras lo tiene abierto en modo de prioridad. Obtiene ventajas de rendimiento para las operaciones de copia, pero impide que otros usuarios puedan confirmar los cambios. Limite el tiempo que los objetos están abiertos en modo de prioridad. Debe especificar **STGM \_ DIRECT** y **STGM \_ READ** con el modo de prioridad y no puede especificar **STGM \_ DELETEONRELEASE**. **STGM \_ DELETEONRELEASE** solo es válido al crear un objeto raíz, como [**con StgCreateStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) No es válido al abrir un objeto raíz existente, como [**con StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) Tampoco es válido al crear o abrir un subelemento, como [**con IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).


</dt> </dl> </dd> <dt>

<span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM \_ CREATE**
</dt> <dd> <dl> <dt>

0x00001000L
</dt> <dt>



Indica que se debe quitar un objeto de almacenamiento o flujo existente antes de que el nuevo objeto lo reemplace. Se crea un nuevo objeto cuando se especifica esta marca solo si el objeto existente se ha quitado correctamente.

Esta marca se usa al intentar crear:

-   Objeto de almacenamiento en un disco, pero existe un archivo con ese nombre.
-   Un objeto dentro de un objeto de almacenamiento, pero existe un objeto con el nombre especificado.
-   Objeto de matriz de bytes, pero existe uno con el nombre especificado.

Esta marca no se puede usar con operaciones abiertas, como [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) o [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).


</dt> </dl> </dd> <dt>

<span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ CONVERT**
</dt> <dd> <dl> <dt>

0x00020000L
</dt> <dt>



Crea el nuevo objeto conservando los datos existentes en una secuencia denominada "Contenido". En el caso de un objeto de almacenamiento o una matriz de bytes, se da formato a los datos antiguos en una secuencia independientemente de si la matriz de bytes o archivo existente contiene actualmente un objeto de almacenamiento en capas. Esta marca solo se puede usar al crear un objeto de almacenamiento raíz. No se puede usar dentro de un objeto de almacenamiento; por ejemplo, en [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Tampoco es válido usar esta marca y la marca **STGM \_ DELETEONRELEASE** simultáneamente.


</dt> </dl> </dd> <dt>

<span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FAILIFTHERE**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Hace que se produce un error en la operación de creación si existe un objeto existente con el nombre especificado. En este caso, **se devuelve STG \_ E \_ FILEALREADYEXISTS.** Este es el modo de creación predeterminado; es decir, si no se especifica ninguna otra marca de creación, se implica **STGM \_ FAILIFTHERE.**


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ DIRECT**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Indica que, en modo directo, cada cambio en un elemento de almacenamiento o flujo se escribe a medida que se produce. Este es el valor predeterminado si **no se especifica STGM \_ DIRECT** ni **STGM \_ TRANSACTED.**


</dt> </dl> </dd> <dt>

<span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ TRANSACTED**
</dt> <dd> <dl> <dt>

0x00010000L
</dt> <dt>



Indica que, en modo de transacción, los cambios se almacena en búfer y se escriben solo si se llama a una operación de confirmación explícita. Para pasar por alto los cambios, llame al [**método Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) en la [**interfaz IStream,**](/windows/desktop/api/Objidl/nn-objidl-istream) [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)o [**IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) La implementación de archivos compuestos COM de **IStorage** no admite secuencias de transacción, lo que significa que las secuencias solo se pueden abrir en modo directo y no se pueden revertir los cambios a ellas, pero se admiten los almacenamientos con transacciones. Las implementaciones de archivos compuestos, independientes y del sistema de archivos NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) de forma similar no admiten conjuntos de propiedades simples y con transacciones porque estos conjuntos de propiedades se almacenan en secuencias. Sin embargo, se admite la transacción de conjuntos de propiedades no simples, que se pueden crear especificando la marca **PROPSETFLAG \_ NONSIMPLE** en el parámetro *grfFlags* de [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).


</dt> </dl> </dd> <dt>

<span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOSCRATCH**
</dt> <dd> <dl> <dt>

0x00100000L
</dt> <dt>



Indica que, en modo de transacción, normalmente se usa un archivo temporal temporal para guardar las modificaciones hasta que se llama **al método Commit.** La **especificación de STGM \_ NOSCRATCH** permite usar la parte no utilizada del archivo original como espacio de trabajo en lugar de crear un archivo nuevo para ese propósito. Esto no afecta a los datos del archivo original y, en algunos casos, puede dar lugar a un rendimiento mejorado. No es válido especificar esta marca sin especificar **también STGM \_ TRANSACTED** y esta marca solo se puede usar en una raíz abierta. Para obtener más información sobre el modo NoScratch, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOSNAPSHOT**
</dt> <dd> <dl> <dt>

0x00200000L
</dt> <dt>



Esta marca se usa al abrir un objeto de almacenamiento con **STGM \_ TRANSACTED** y sin **STGM \_ SHARE \_ EXCLUSIVE** o **STGM \_ SHARE DENY \_ \_ WRITE**. En este caso, la especificación **de STGM \_ NOSNAPSHOT** impide que la implementación proporcionada por el sistema cree una copia de instantánea del archivo. En su lugar, los cambios realizados en el archivo se escriben al final del archivo. El espacio sin usar no se reclama a menos que se realice la consolidación durante la confirmación y solo haya un escritor actual en el archivo. Cuando el archivo se abre sin modo de instantánea, no se puede realizar otra operación de apertura sin especificar **STGM \_ NOSNAPSHOT**. Esta marca solo se puede usar en una operación raíz abierta. Para obtener más información sobre el modo NoSnapshot, consulte la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ SIMPLE**
</dt> <dd> <dl> <dt>

0x08000000L
</dt> <dt>



Proporciona una implementación más rápida de un archivo compuesto en un caso limitado, pero usado con frecuencia. Para obtener más información, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ DIRECT \_ SWMR**
</dt> <dd> <dl> <dt>

0x00400000L
</dt> <dt>



Admite el modo directo para operaciones de archivo de un solo escritor y varios lectores. Para obtener más información, vea la sección Comentarios.


</dt> </dl> </dd> <dt>

<span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ DELETEONRELEASE**
</dt> <dd> <dl> <dt>

0x04000000L
</dt> <dt>



Indica que el archivo subyacente se destruirá automáticamente cuando se libera el objeto de almacenamiento raíz. Esta característica es muy útil para crear archivos temporales. Esta marca solo se puede usar al crear un objeto raíz, como [**con StgCreateStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) No es válido al abrir un objeto raíz, como [**con StgOpenStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)o al crear o abrir un subelemento, como [**con IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Tampoco es válido usar esta marca y la marca STGM \_ CONVERT simultáneamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Puede combinar estas marcas, pero solo puede elegir una marca de cada grupo de marcas relacionadas. Normalmente, se debe especificar una marca de cada uno de los grupos de acceso y uso compartido para todas las funciones y métodos que usan estas constantes. Las marcas de otros grupos son opcionales.

### <a name="transacted-mode"></a>Modo de transacción

Cuando se especifica la marca **STGM \_ DIRECT,** solo se puede especificar una de las siguientes combinaciones de marcas desde los grupos de acceso y uso compartido.

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

Tenga en cuenta que el modo directo está implícito en la ausencia **de STGM \_ TRANSACTED.** Es decir, si no **se especifica STGM \_ DIRECT** ni **STGM \_ TRANSACTED,** se supone **que STGM \_ DIRECT.**

Cuando se **especifica la \_ marca STGM TRANSACTED,** los objetos se crean o se abren en modo de transacción. En este modo, los cambios en un objeto no se conservan hasta que se confirman. Por ejemplo, los cambios en un objeto de almacenamiento con transacciones no se conservan hasta que se llama al método [**IStorage::Commit.**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) Los cambios en este tipo de objeto de almacenamiento se perderán si el objeto de almacenamiento se libera (versión final) antes de llamar al método **Commit** o si se llama al método [**IStorage::Revert.**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)

Cuando se crea o abre un objeto en modo de transacción, la implementación debe mantener los datos originales y las actualizaciones de estos datos, de modo que las actualizaciones se puedan revertir si es necesario. Esto suele realizarse escribiendo cambios en un área de cero hasta que se confirman, o mediante la creación de una copia, denominada instantánea, de los datos confirmados más recientemente.

Cuando se abre un objeto de almacenamiento raíz en modo de transacción, la ubicación y el comportamiento de los datos iniciales y las copias de instantáneas se pueden controlar para optimizar el rendimiento con las marcas **STGM \_ NOSCRATCH** y **STGM \_ NOSNAPSHOT.** (Se obtiene un objeto de almacenamiento raíz de, por ejemplo, la función [**StgOpenStorageEx;**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) un objeto de almacenamiento obtenido del método [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) es un objeto de subalmacenamiento). Normalmente, los datos temporales y las instantáneas se almacenan en archivos temporales, independientes del almacenamiento.

El efecto de estas marcas depende del número de lectores o escritores que acceden al almacenamiento raíz.

En el caso del "escritor único", se abre un objeto de almacenamiento en modo de transacción para el acceso de escritura y no puede haber ningún otro acceso al archivo. Es decir, el archivo se abre con **STGM \_ TRANSACTED,** el acceso de **STGM \_ WRITE** o **STGM \_ READWRITE** y el uso compartido de **STGM \_ SHARE \_ EXCLUSIVE.** En este caso, los cambios realizados en el objeto de almacenamiento se escriben en el área de scratch. Cuando se confirman esos cambios, se copian en el almacenamiento original. Por lo tanto, si no se realiza realmente ningún cambio en el objeto de almacenamiento, no habrá ninguna transferencia de datos innecesaria.

En el caso de "varios escritores", se abre un objeto de almacenamiento con transacciones para el acceso de escritura, pero se comparte en , como para permitir otros escritores. Es decir, el objeto de almacenamiento se abre con **STGM \_ TRANSACTED,** el acceso de **STGM \_ WRITE** o **STGM \_ READWRITE** y el uso compartido de **STGM \_ SHARE DENY \_ \_ READ**. Si en su lugar se especifica el uso compartido de **STGM \_ SHARE DENY \_ \_ NONE,** el caso es "multiple-writer, multiple-reader". En estos casos, se realizará una instantánea de los datos originales durante la operación de apertura. Por lo tanto, aunque no se realice realmente ningún cambio en el almacenamiento o no lo abra otro escritor simultáneamente, la transferencia de datos sigue siendo necesaria durante la apertura. Como resultado, se puede obtener el mejor rendimiento en tiempo abierto abriendo el objeto de almacenamiento en los modos **STGM \_ SHARE DENY \_ \_ WRITE** o **STGM SHARE \_ \_ EXCLUSIVE.** Para obtener más información sobre cómo se confirman los cambios cuando hay varios escritores, vea [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).

En el caso de "escritor único, lector múltiple", se abre un objeto de almacenamiento con transacciones para el acceso de escritura, pero se comparte con los lectores. Es decir, el objeto de almacenamiento lo abre el escritor con **STGM \_ TRANSACTED,** el acceso de **STGM \_ READWRITE** o **STGM \_ WRITE** y el uso compartido de **STGM \_ SHARE DENY \_ \_ WRITE.** Los lectores abren el almacenamiento con **STGM \_ TRANSACTED,** el acceso de **STGM \_ READ** y el uso compartido de **STGM \_ SHARE DENY \_ \_ NONE**. En este caso, el escritor usa el área de cero para almacenar los cambios no confirmados. Como en los casos anteriores, el lector incurre en una penalización de rendimiento en tiempo de apertura mientras se crea una copia de instantánea de los datos.

Normalmente, el área temporal es un archivo temporal, independiente de los datos originales. Cuando los cambios se confirman en el archivo original, los datos se deben transferir desde el archivo temporal. Para evitar esta transferencia de datos, se puede especificar la marca **\_ STGM NOSCRATCH.** Cuando se especifica esta marca, se usan partes del archivo de objeto de almacenamiento para el área temporal, en lugar de un archivo temporal independiente. Como resultado, la confirmación de los cambios se puede realizar rápidamente, ya que se requiere poca transferencia de datos. La desventaja es que el archivo de almacenamiento puede ser mayor de lo que sería de otro modo, ya que debe crecer para que sea lo suficientemente grande para los datos originales y el área de cero. Para consolidar los datos y quitar esta área innecesaria, vuelva a abrir el almacenamiento raíz en modo de transacción, pero sin establecer la marca **STGM \_ NOSCRATCH.** A continuación, [**llame a IStorage::Commit con**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) la marca **\_ STGC CONSOLIDATE** establecida.

El área de instantánea, como el área temporal, también es, normalmente, un archivo temporal, y esto también puede verse afectado por una marca STGM. Al especificar la marca **STGM \_ NOSNAPSHOT,** no se crea un archivo de instantánea temporal independiente. En su lugar, los datos originales nunca se modifican, incluso si hay uno o varios escritores por objeto. Cuando se confirman los cambios, se agregan al archivo, pero los datos originales permanecen intactos. Este modo aumenta la eficacia porque reduce el tiempo de ejecución al eliminar el requisito de crear una instantánea durante la operación de apertura. Sin embargo, el uso de este modo puede dar lugar a un archivo de almacenamiento muy grande porque los datos del archivo nunca se pueden sobrescribir. Esto no limita el tamaño de los archivos abiertos en el modo NoSnapshot.

### <a name="direct-single-writer-multiple-reader-mode"></a>Direct Single-Writer, Multiple-Reader Mode

Como se describe, es posible tener un único sistema de escritura y varios lectores de un objeto de almacenamiento, si ese objeto se abre en modo de transacción. También es posible lograr el caso de un solo escritor y varios lectores en modo directo, mediante la especificación de la marca **STGM \_ DIRECT \_ SWMR.**

En el modo **STGM \_ DIRECT \_ SWMR,** es posible que un autor de la llamada abra un objeto para el acceso de lectura y escritura, mientras que otros autores de la llamada simultáneamente tienen el archivo abierto para el acceso de solo lectura. No es válido usar esta marca en combinación con la **marca STGM \_ TRANSACTED.** En este modo, el escritor abre el objeto con las marcas siguientes:

**STGM \_ DIRECT \_ SWMR** \| **STGM \_ READWRITE** \| **STGM \_ SHARE \_ DENYWRITE**

y cada uno de los lectores abre el objeto con estas marcas:

**STGM \_ RECURSO \_ COMPARTIDO STGM DE** \| **LECTURA \_ STGM** DE SWMR DIRECTO DENY \| **\_ \_ \_ NONE**

En este modo, para modificar el objeto de almacenamiento, el escritor debe obtener acceso exclusivo al objeto. Esto es posible cuando todos los lectores lo han cerrado. El escritor usa la [**interfaz IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) para obtener este acceso exclusivo.

### <a name="simple-mode"></a>Modo simple

El modo simple **(STGM \_ SIMPLE)** es útil para las aplicaciones que realizan operaciones de guardado completas. Es eficaz, pero tiene las siguientes restricciones:

-   No existe compatibilidad con los subalmacenamientos.
-   El objeto de almacenamiento y los objetos de secuencia obtenidos de él no se pueden serializar.
-   Cada secuencia tiene un tamaño mínimo. Si se escriben menos bytes mínimos en una secuencia cuando se libera la secuencia, la secuencia se extiende al tamaño mínimo. Por ejemplo, el tamaño mínimo para una implementación [**de IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) determinada es de 4 KB. Se crea una secuencia y se escribe en ella 1 KB. En la versión final de **ese IStream,** el tamaño del flujo se ampliará automáticamente a 4 KB. Posteriormente, al abrir la secuencia y llamar al [**método IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) se mostrará un tamaño de 4 KB.
-   No todos los métodos [**de IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) [**o IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) serán compatibles con la implementación de . Para obtener más información, [vea IStorage - Compound File Implementation](istorage-compound-file-implementation.md)e [IStream - Compound File Implementation](istream-compound-file-implementation.md).

[La serialización](/windows/desktop/Midl/marshaling-ole-data-types) es el proceso de empaquetar, desempaquetar y enviar parámetros de método de interfaz a través de los límites de subprocesos o procesos dentro de una llamada a procedimiento remoto (RPC). Para obtener más información, vea [Detalles de serialización](../com/marshaling-details.md) y [Serialización de interfaz.](../com/interface-marshaling.md)

Cuando un objeto de almacenamiento se obtiene mediante una operación Create en modo simple:

-   Se pueden crear elementos de secuencia, pero no abrirse.
-   Cuando se crea un elemento de secuencia mediante una llamada a [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), no es posible crear otra secuencia hasta que se libera ese objeto de secuencia.
-   Una vez escritas todas las secuencias, llame [**a IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) para vaciar los cambios.

Cuando una operación Open obtiene un objeto de almacenamiento en modo simple:

-   Solo es posible abrir un elemento de secuencia a la vez.
-   No es posible cambiar el tamaño de una secuencia llamando al método [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) o buscando o escribiendo más allá del final de la secuencia. Sin embargo, dado que todas las secuencias tienen un tamaño mínimo, es posible usar la secuencia hasta ese tamaño, incluso si originalmente se escribieron menos datos en ella. Para determinar el tamaño de una secuencia, use el [**método IStream::Stat.**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)

Tenga en cuenta que, si un objeto de almacenamiento modifica un elemento de almacenamiento que no está en modo simple, no será posible, de nuevo, abrir ese elemento de almacenamiento en modo simple.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>ObjBase.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
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

 

