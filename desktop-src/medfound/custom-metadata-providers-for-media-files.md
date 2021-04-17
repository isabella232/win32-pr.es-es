---
description: En este tema se describe cómo escribir un controlador de propiedades de Shell personalizado para un Microsoft Media Foundation origen de medios.
ms.assetid: f8cf70ff-8324-4308-8adf-a145aa351ca9
title: Proveedores de metadatos personalizados para archivos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ded77492d03f7b802f6b2f9c25e1009ef97f50
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721345"
---
# <a name="custom-metadata-providers-for-media-files"></a>Proveedores de metadatos personalizados para archivos multimedia

En este tema se describe cómo escribir un controlador de propiedades de Shell personalizado para un Microsoft Media Foundation origen de medios.

> [!Note]  
> Para obtener información general sobre los proveedores de metadatos en Media Foundation, vea [metadatos de medios](media-metadata.md). En este tema se describen los controladores de propiedades de Shell. no describe la interfaz de metadatos de la versión 1, [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata).

 

Los metadatos están estrechamente relacionados con el formato del archivo. En Media Foundation, los formatos de archivo se representan mediante orígenes multimedia. Si desea admitir los metadatos de un formato que no se admite de forma nativa en Media Foundation, debe implementar un origen de medios personalizado con un controlador de propiedades. El controlador de propiedades permite que el sistema de propiedades de Shell Lea y escriba los metadatos de forma eficaz.

Un controlador de propiedades es un objeto COM que implementa las interfaces siguientes:

-   [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Opcionalmente, también puede exponer la siguiente interfaz:

-   [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)

Si el sistema de propiedades de Shell necesita obtener los metadatos de un archivo, llama a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el controlador de propiedades y, a continuación, llama a los métodos de lectura y escritura adecuados en la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

La canalización Media Foundation usa un mecanismo ligeramente diferente, porque la canalización obtiene el controlador de propiedades directamente del origen de los medios. En lugar de llamar a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el controlador de propiedades, la canalización llama a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el origen multimedia, como se describe en el tema sobre los [proveedores de metadatos de Shell](shell-metadata-providers.md).

Para crear un controlador de propiedades personalizado, haga lo siguiente:

-   Implemente la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) para exponer [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore). El GUID del servicio es el **\_ servicio de \_ controlador \_ de propiedades MF**.
-   Si el origen multimedia se va a usar de forma remota, también debe exponer la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a través del método **QueryInterface** del origen multimedia, además de [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice).
-   Para que el controlador de propiedades esté disponible para el sistema de propiedades de Shell, registre el archivo DLL del controlador de propiedades tal y como se describe en [registrar y distribuir controladores de propiedades](../properties/prophand-reg-dist.md).
-   El origen multimedia se registra por separado, tal y como se describe en [controladores de esquema y controladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

### <a name="implementation-tips"></a>Sugerencias de implementación

Para obtener una lista de las claves de propiedad de metadatos, consulte [propiedades de metadatos para archivos multimedia](metadata-properties-for-media-files.md).

Los controladores de propiedades deben ser rápidos; deben proporcionar acceso de lectura y escritura eficaz a los metadatos. (Tenga en cuenta que el shell puede recuperar metadatos de cientos de archivos). Por lo tanto, no llame a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) desde el controlador de propiedad. La función **MFStartup** introduce la latencia de inicio, ya que crea varios subprocesos de cola de trabajo y asigna memoria global.

En una implementación típica, el controlador de propiedades y el origen multimedia compartirán parte del mismo código de análisis. Sin embargo, un origen multimedia usa llamadas asincrónicas de [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) para e/s, mientras que el controlador de propiedades utiliza la interfaz [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Media Foundation proporciona un objeto auxiliar que contiene una secuencia basada en **IStream** y la expone como una secuencia **IMFByteStream** . Para crear el contenedor, llame a [**MFCreateMFByteStreamOnStream**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream).

Al actualizar los metadatos, se recomienda escribir los datos directamente en la secuencia original. Esta recomendación difiere del comportamiento de *copia en escritura* de la mayoría de los controladores de propiedades, en los que se modifica una copia de los datos. Los archivos multimedia pueden ser muy grandes, por lo que la copia en escritura suele ser demasiado lenta para una implementación eficaz. Para deshabilitar la opción de copia en escritura, establezca el valor del registro **ManualSafeSave** , como se describe en [registrar y distribuir controladores de propiedades](../properties/prophand-reg-dist.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Metadatos de medios](media-metadata.md)
</dt> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Escritura de un origen de medios personalizado](writing-a-custom-media-source.md)
</dt> </dl>

 

 
