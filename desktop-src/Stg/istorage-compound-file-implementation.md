---
title: IStorage-Compound de archivos
description: La implementación de archivos compuestos de IStorage permite crear y administrar subalmacenamientos y secuencias dentro de un objeto de almacenamiento que reside en un objeto de archivo compuesto.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage Strctd Stg , implementación de archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab243189d5a8cfb3e053c66bcd752d05bb65ab965657778a3bc3250c30ef8e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992424"
---
# <a name="istorage-compound-file-implementation"></a>IStorage-Compound de archivos

La implementación de archivos compuestos de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) permite crear y administrar subalmacenamientos y secuencias dentro de un objeto de almacenamiento que reside en un objeto de archivo compuesto. Para crear un objeto de archivo compuesto y obtener un **puntero IStorage,** llame a la función de API [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Para abrir un objeto de archivo compuesto existente y obtener su puntero **IStorage** raíz, llame a [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).

Las aplicaciones que usan almacenamiento compuesto deben registrarse en HKEY \_ CLASSES \_ ROOT \\ SystemFileAssociations y deben proporcionar sus propios controladores de propiedades. Para obtener más información, vea la sección "Registrar verbos y otra información de asociación de archivos" de [Registro de aplicaciones.](/windows/desktop/shell/app-registration)

## <a name="when-to-use"></a>Cuándo usar

La mayoría de las aplicaciones usan esta implementación para crear y administrar almacenamientos y flujos.

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)
</dt> <dd>

Crea y abre un objeto de secuencia con el nombre especificado incluido en este objeto de almacenamiento. El nombre no debe superar los 31 caracteres de longitud (sin incluir el terminador de cadena). Los caracteres 000 a 01f, que actúan como el primer carácter del nombre de la secuencia/almacenamiento, se reservan para uso de OLE. Es una restricción de archivo compuesto, no una restricción de almacenamiento estructurado. La implementación de archivos compuestos proporcionada por COM del [**método IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) no admite los comportamientos siguientes:

-   No se admite la marca \_ STGM DELETEONRELEASE.
-   El modo de transacción (STGM \_ TRANSACTED) no se admite para objetos de secuencia.
-   No se admite la apertura de la misma secuencia más de una vez desde el mismo almacenamiento. La marca \_ STGM SHARE \_ EXCLUSIVE sharing-mode debe especificarse en el *parámetro grfMode.*

</dd> <dt>

<span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)
</dt> <dd>

Abre un objeto de secuencia existente dentro de este objeto de almacenamiento mediante los modos de acceso especificados en el *parámetro grfMode.* Los caracteres 000 a 01f, que actúan como el primer carácter del nombre de la secuencia/almacenamiento, se reservan para uso de OLE. Es una restricción de archivo compuesto, no una restricción de almacenamiento estructurado. La implementación de archivos compuestos proporcionada por COM del [**método IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) no admite el comportamiento siguiente:

-   Marca \_ DELETEONRELEASE de STGM.
-   Modo de transacción (STGM \_ TRANSACTED) para objetos de secuencia.
-   Abrir la misma secuencia más de una vez desde el mismo almacenamiento. Se debe especificar \_ la marca STGM SHARE \_ EXCLUSIVE.

</dd> <dt>

<span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)
</dt> <dd>

Crea y abre un nuevo objeto de almacenamiento con el nombre especificado en el modo de acceso especificado. El nombre no debe superar los 31 caracteres de longitud (sin incluir el terminador de cadena). Los caracteres 000 a 01f, que actúan como el primer carácter del nombre de la secuencia/almacenamiento, se reservan para uso de OLE. Es una restricción de archivo compuesto, no una restricción de almacenamiento estructurado. La implementación de archivo compuesto proporcionada por COM del [**método IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) no admite el comportamiento siguiente:

-   La marca STGM \_ PRIORITY para los almacenamientos no raíz.
-   Abrir el mismo objeto de almacenamiento más de una vez desde el mismo almacenamiento primario. Se debe especificar \_ la marca STGM SHARE \_ EXCLUSIVE.
-   Marca \_ DELETEONRELEASE de STGM. Si se especifica esta marca, la función devuelve STG \_ E \_ INVALIDFLAG.

</dd> <dt>

<span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)
</dt> <dd>

Abre un objeto de almacenamiento existente con el nombre especificado en el modo de acceso especificado. Los caracteres 000 a 01f, que actúan como el primer carácter del nombre de la secuencia/almacenamiento, se reservan para uso de OLE. Es una restricción de archivo compuesto, no una restricción de almacenamiento estructurado. La implementación de archivo compuesto proporcionada por COM del [**método IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) no admite el comportamiento siguiente:

-   La marca STGM \_ PRIORITY para los almacenamientos no raíz.
-   Abrir el mismo objeto de almacenamiento más de una vez desde el mismo almacenamiento primario. Se debe especificar \_ la marca STGM SHARE \_ EXCLUSIVE.
-   Marca \_ DELETEONRELEASE de STGM. Si se especifica esta marca, la función devuelve STG \_ E \_ INVALIDFUNCTION.

</dd> <dt>

<span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)
</dt> <dd>

Copia solo los subalmacenamientos y secuencias de este objeto de almacenamiento abierto en otro objeto de almacenamiento. El *parámetro rgiidExclude* se puede establecer en IID IStream para copiar solo \_ los subalmacenamientos o en IID IStorage para copiar solo \_ secuencias.

</dd> <dt>

<span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage::MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)
</dt> <dd>

Copia o mueve un subalmacenamiento o una secuencia de este objeto de almacenamiento a otro objeto de almacenamiento.

</dd> <dt>

<span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)
</dt> <dd>

Garantiza que los cambios realizados en un objeto de almacenamiento abierto en modo de transacción se reflejan en el almacenamiento primario; para un almacenamiento raíz, refleja los cambios en el dispositivo real; por ejemplo, un archivo en disco. Para un objeto de almacenamiento raíz abierto en modo directo, este método no tiene ningún efecto excepto vaciar todos los búferes de memoria en el disco. Para los objetos de almacenamiento no raíz en modo directo, este método no tiene ningún efecto.

La implementación de archivos compuestos proporcionados por COM usa un proceso de confirmación en dos fases a menos que se especifique STGC OVERWRITE en el \_ *parámetro grfCommitFlags.* Este proceso de dos fases garantiza la solidez de los datos, en caso de que se produce un error en la operación de confirmación. En primer lugar, todos los datos nuevos se escriben en el espacio sin usar del archivo subyacente. Si es necesario, se asigna nuevo espacio al archivo. Una vez completado este paso, se actualiza una tabla del archivo mediante una operación de escritura de un solo sector para indicar que los nuevos datos se usarán en lugar del anterior. Los datos antiguos se convierten en espacio libre para usarse en la siguiente operación de confirmación. Por lo tanto, los datos antiguos están disponibles y se pueden restaurar si se produce un error al confirmar los cambios. Si se especifica \_ STGC OVERWRITE, se usa una operación de confirmación de una sola fase. Para obtener más información sobre las marcas de modo de transacción, vea [**ENUMERACIÓN STGC.**](/windows/win32/api/wtypes/ne-wtypes-stgc)

</dd> <dt>

<span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)
</dt> <dd>

Descarta todos los cambios realizados en el objeto de almacenamiento desde la última operación de confirmación.

</dd> <dt>

<span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dd>

Crea y recupera un puntero a un objeto enumerador que se puede usar para enumerar los objetos de almacenamiento y secuencia incluidos en este objeto de almacenamiento. La implementación del archivo compuesto proporcionado por COM toma una instantánea de esa información. Por lo tanto, los cambios en los flujos y almacenamientos no se reflejan en el enumerador hasta que se obtiene un nuevo enumerador.

</dd> <dt>

<span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::D estroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)
</dt> <dd>

Quita el elemento especificado (subalmacenamiento o secuencia) de este objeto de almacenamiento.

</dd> <dt>

<span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage::RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)
</dt> <dd>

Cambia el nombre del subalmacenamiento o secuencia especificados en este objeto de almacenamiento. Los caracteres 000 a 01f, que actúan como el primer carácter del nombre de la secuencia/almacenamiento, se reservan para uso de OLE. Es una restricción de archivo compuesto, no una restricción de almacenamiento estructurado.

</dd> <dt>

<span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dd>

Establece las horas de modificación, acceso y creación del elemento de almacenamiento especificado. La implementación de archivos compuestos proporcionada por COM mantiene los tiempos de modificación y cambio para los objetos de almacenamiento internos. Los objetos de almacenamiento raíz admiten todo lo que admite el sistema de archivos subyacente (o [**ILockBytes).**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) La implementación del archivo compuesto no mantiene ninguna marca de tiempo para los flujos internos. Las marcas de tiempo no admitidas se notifican como cero, lo que permite al autor de la llamada probar el soporte técnico.

</dd> <dt>

<span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)
</dt> <dd>

Asigna el CLSID especificado a este objeto de almacenamiento.

</dd> <dt>

<span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage::SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)
</dt> <dd>

Almacena hasta 32 bits de información de estado en este objeto de almacenamiento. El estado establecido por este método es solo para uso externo. La implementación del archivo compuesto proporcionado por COM no realiza ninguna acción en función del estado.

</dd> <dt>

<span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)
</dt> <dd>

Recupera la estructura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) para este objeto de almacenamiento abierto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si el objeto de almacenamiento se abre en modo simple, se restringe el uso de los métodos anteriores. Un almacenamiento está en modo simple si se abre con el elemento SIMPLE STGM especificado en el parámetro grfMode de la función \_ [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) [**o StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)  Para obtener más información sobre los almacenamientos en modo simple, vea [**STGM Constants**](stgm-constants.md). Si el objeto de almacenamiento en modo simple se obtuvo de la función **StgCreateStorageEx,** se puede llamar al método [**CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) pero no [**al método OpenStream.**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) Si el objeto de almacenamiento en modo simple se obtuvo de la función **StgOpenStorageEx,** se puede llamar al método **OpenStream,** pero no **al método CreateStream.**

Cuando se usa un objeto de almacenamiento en modo simple para crear una secuencia, el tamaño mínimo de esa secuencia suele ser de 4096 bytes. Si se escriben menos datos en la secuencia, el tamaño se redondea hasta 4096 bytes.

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

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 