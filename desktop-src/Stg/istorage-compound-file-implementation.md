---
title: IStorage-Compound la implementación de archivos
description: La implementación de archivo compuesto de IStorage le permite crear y administrar subalmacenamientos y secuencias en un objeto de almacenamiento que reside en un objeto de archivo compuesto.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage Strctd STG, implementación de archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf37b24a7c68bbe357d99f94e666bfcb613c472
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665835"
---
# <a name="istorage-compound-file-implementation"></a>IStorage-Compound la implementación de archivos

La implementación de archivo compuesto de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) le permite crear y administrar subalmacenamientos y secuencias en un objeto de almacenamiento que reside en un objeto de archivo compuesto. Para crear un objeto de archivo compuesto y obtener un puntero **IStorage** , llame a la función de API [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Para abrir un objeto de archivo compuesto existente y obtener su puntero de **IStorage** raíz, llame a [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).

Las aplicaciones que usan almacenamiento compuesto deben registrarse en \_ las clases HKEY \_ raíz \\ SystemFileAssociations y deben proporcionar sus propios controladores de propiedades. Para obtener más información, vea la sección "registrar verbos y otros datos de Asociación de archivos" del [registro de aplicaciones](/windows/desktop/shell/app-registration).

## <a name="when-to-use"></a>Cuándo usar

La mayoría de las aplicaciones usan esta implementación para crear y administrar almacenamientos y secuencias.

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)
</dt> <dd>

Crea y abre un objeto de flujo con el nombre especificado que contiene este objeto de almacenamiento. El nombre no debe superar los 31 caracteres de longitud (sin incluir el terminador de cadena). Los caracteres 000 a 01f, que actúan como el primer carácter del nombre de la secuencia/almacenamiento, se reservan para uso de OLE. Es una restricción de archivo compuesto, no una restricción de almacenamiento estructurado. La implementación de archivo compuesto proporcionado por COM del método [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) no admite los siguientes comportamientos:

-   \_No se admite la marca DELETEONRELEASE de STGM.
-   El modo de transacción (STGM \_ ) no se admite para los objetos de secuencia.
-   No se admite la apertura de la misma secuencia más de una vez desde el mismo almacenamiento. La \_ marca de modo de uso compartido exclusivo del recurso compartido STGM \_ debe especificarse en el parámetro *grfMode* .

</dd> <dt>

<span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)
</dt> <dd>

Abre un objeto de flujo existente dentro de este objeto de almacenamiento mediante los modos de acceso especificados en el parámetro *grfMode* . Los caracteres 000 a 01f, que actúan como el primer carácter del nombre de la secuencia/almacenamiento, se reservan para uso de OLE. Es una restricción de archivo compuesto, no una restricción de almacenamiento estructurado. La implementación del archivo compuesto proporcionado por COM del método [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) no admite el comportamiento siguiente:

-   \_Marca DELETEONRELEASE de STGM.
-   Modo de transacción (STGM \_ TRANSaccional) para objetos de secuencia.
-   Abrir el mismo flujo más de una vez desde el mismo almacenamiento. \_Se debe especificar la marca de uso compartido STGM \_ .

</dd> <dt>

<span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)
</dt> <dd>

Crea y abre un nuevo objeto de almacenamiento con el nombre especificado en el modo de acceso especificado. El nombre no debe superar los 31 caracteres de longitud (sin incluir el terminador de cadena). Los caracteres 000 a 01f, que actúan como el primer carácter del nombre de la secuencia/almacenamiento, se reservan para uso de OLE. Es una restricción de archivo compuesto, no una restricción de almacenamiento estructurado. La implementación del archivo compuesto proporcionado por COM del método [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) no admite el comportamiento siguiente:

-   \_Marca de prioridad de STGM para los almacenamientos no raíz.
-   Abrir el mismo objeto de almacenamiento más de una vez desde el mismo almacenamiento primario. \_Se debe especificar la marca de uso compartido STGM \_ .
-   \_Marca DELETEONRELEASE de STGM. Si se especifica esta marca, la función devuelve STG \_ E \_ INVALIDFLAG.

</dd> <dt>

<span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)
</dt> <dd>

Abre un objeto de almacenamiento existente con el nombre especificado en el modo de acceso especificado. Los caracteres 000 a 01f, que actúan como el primer carácter del nombre de la secuencia/almacenamiento, se reservan para uso de OLE. Es una restricción de archivo compuesto, no una restricción de almacenamiento estructurado. La implementación del archivo compuesto proporcionado por COM del método [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) no admite el comportamiento siguiente:

-   \_Marca de prioridad de STGM para los almacenamientos no raíz.
-   Abrir el mismo objeto de almacenamiento más de una vez desde el mismo almacenamiento primario. \_Se debe especificar la marca de uso compartido STGM \_ .
-   \_Marca DELETEONRELEASE de STGM. Si se especifica esta marca, la función devuelve STG \_ E \_ INVALIDFUNCTION.

</dd> <dt>

<span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)
</dt> <dd>

Copia solo los subalmacénes y las secuencias de este objeto de almacenamiento abierto en otro objeto de almacenamiento. El parámetro *rgiidExclude* se puede establecer en IID \_ IStream para copiar solo los subalmacenamientos o en IID \_ IStorage para copiar solo flujos.

</dd> <dt>

<span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage:: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)
</dt> <dd>

Copia o mueve un subalmacenamiento o secuencia de este objeto de almacenamiento a otro objeto de almacenamiento.

</dd> <dt>

<span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)
</dt> <dd>

Garantiza que los cambios realizados en un objeto de almacenamiento abierto en modo de transacción se reflejan en el almacenamiento principal. para un almacenamiento raíz, refleja los cambios en el dispositivo real; por ejemplo, un archivo en disco. Para un objeto de almacenamiento raíz abierto en modo directo, este método no tiene ningún efecto excepto para vaciar todos los búferes de memoria en el disco. En el caso de los objetos de almacenamiento no raíz en modo directo, este método no tiene ningún efecto.

La implementación de archivos compuestos proporcionados por COM usa un proceso de confirmación en dos fases, a menos que \_ se especifique STGC overwrite en el parámetro *grfCommitFlags* . Este proceso en dos fases garantiza la solidez de los datos, en caso de que se produzca un error en la operación de confirmación. En primer lugar, todos los datos nuevos se escriben en el espacio no utilizado del archivo subyacente. Si es necesario, se asigna un nuevo espacio al archivo. Una vez completado este paso, se actualiza una tabla del archivo mediante una operación de escritura de un solo sector para indicar que los nuevos datos se van a utilizar en lugar del antiguo. Los datos antiguos se convierten en el espacio libre que se va a usar en la siguiente operación de confirmación. Por lo tanto, los datos antiguos están disponibles y se pueden restaurar si se produce un error al confirmar los cambios. Si \_ se especifica STGC overwrite, se usa una operación de confirmación de fase única. Para obtener más información sobre las marcas del modo de transacción, consulte enumeración [**STGC**](/windows/win32/api/wtypes/ne-wtypes-stgc) .

</dd> <dt>

<span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage:: revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)
</dt> <dd>

Descarta todos los cambios realizados en el objeto de almacenamiento desde la última operación de confirmación.

</dd> <dt>

<span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage:: EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dd>

Crea y recupera un puntero a un objeto de enumerador que se puede utilizar para enumerar los objetos de almacenamiento y de secuencia contenidos en este objeto de almacenamiento. La implementación de archivo compuesto proporcionado por COM toma una instantánea de esa información. Por lo tanto, los cambios en las secuencias y los almacenamientos no se reflejan en el enumerador hasta que se obtiene un nuevo enumerador.

</dd> <dt>

<span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::D estroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)
</dt> <dd>

Quita el elemento especificado (substorage o Stream) de este objeto de almacenamiento.

</dd> <dt>

<span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage:: RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)
</dt> <dd>

Cambia el nombre de la secuencia o el subalmacenamiento especificado en este objeto de almacenamiento. Los caracteres 000 a 01f, que actúan como el primer carácter del nombre de la secuencia/almacenamiento, se reservan para uso de OLE. Es una restricción de archivo compuesto, no una restricción de almacenamiento estructurado.

</dd> <dt>

<span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dd>

Establece las horas de modificación, acceso y creación del elemento de almacenamiento especificado. La implementación de archivo compuesto proporcionado por COM mantiene las horas de modificación y cambio de los objetos de almacenamiento interno. Los objetos de almacenamiento raíz admiten lo que admita el sistema de archivos subyacente (o por [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)). La implementación de archivo compuesto no mantiene ninguna marca de tiempo para las secuencias internas. Las marcas de tiempo no admitidas se muestran como cero, lo que permite al autor de la llamada probar la compatibilidad.

</dd> <dt>

<span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage:: SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)
</dt> <dd>

Asigna el CLSID especificado a este objeto de almacenamiento.

</dd> <dt>

<span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage:: SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)
</dt> <dd>

Almacena hasta 32 bits de información de estado en este objeto de almacenamiento. El estado establecido por este método es solo para uso externo. La implementación del archivo compuesto proporcionado por COM no realiza ninguna acción basada en el estado.

</dd> <dt>

<span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage:: Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)
</dt> <dd>

Recupera la estructura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) para este objeto de almacenamiento abierto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el objeto de almacenamiento se abre en modo simple, el uso de los métodos anteriores está restringido. Un almacenamiento está en modo simple si se abre con el \_ elemento simple STGM especificado en el parámetro *grfMode* de la función [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Para obtener más información acerca de los almacenamientos de modo simple, vea [**constantes STGM**](stgm-constants.md). Si el objeto de almacenamiento de modo simple se obtuvo de la función **StgCreateStorageEx** , se puede llamar al método [**CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) , pero el método [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) no. Si se obtuvo el objeto de almacenamiento en modo simple de la función **StgOpenStorageEx** , se puede llamar al método **OpenStream** , pero el método **CreateStream (** no.

Cuando se usa un objeto de almacenamiento de modo simple para crear una secuencia, el tamaño mínimo de la secuencia suele ser de 4096 bytes. Si se escriben menos datos en la secuencia, el tamaño se redondea hasta 4096 bytes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Límites de implementación de archivos compuestos](structured-storage-interfaces.md)
</dt> <dt>

[**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 