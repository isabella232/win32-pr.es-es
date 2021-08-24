---
description: En este tema se describe cómo escribir un controlador de propiedades de Shell personalizado para un Microsoft Media Foundation multimedia.
ms.assetid: f8cf70ff-8324-4308-8adf-a145aa351ca9
title: Proveedores de metadatos personalizados para archivos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1951fd90265299cb53369d521193740b7d4d05e0f1650583965eb670ab375cc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777605"
---
# <a name="custom-metadata-providers-for-media-files"></a>Proveedores de metadatos personalizados para archivos multimedia

En este tema se describe cómo escribir un controlador de propiedades de Shell personalizado para un Microsoft Media Foundation multimedia.

> [!Note]  
> Para obtener información general sobre los proveedores de metadatos Media Foundation, vea [Metadatos multimedia.](media-metadata.md) En este tema se deba a los controladores de propiedades de Shell; no describe la interfaz de metadatos de la versión 1, [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata).

 

Los metadatos están estrechamente vinculados al formato del archivo. En Media Foundation, los formatos de archivo se representan mediante orígenes multimedia. Si desea admitir metadatos para un formato que no se admite de forma nativa en Media Foundation, debe implementar un origen multimedia personalizado con un controlador de propiedades. El controlador de propiedades permite que el sistema de propiedades de Shell lea y escriba metadatos de forma eficaz.

Un controlador de propiedades es un objeto COM que implementa las interfaces siguientes:

-   [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Opcionalmente, también puede exponer la siguiente interfaz:

-   [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)

Si el sistema de propiedades de Shell necesita obtener metadatos para un archivo, llama a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el controlador de propiedades y, a continuación, llama a los métodos de lectura y escritura adecuados en la [**interfaz IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

La Media Foundation utiliza un mecanismo ligeramente diferente, porque la canalización obtiene el controlador de propiedades directamente del origen multimedia. En lugar de llamar a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el controlador de propiedades, la canalización llama a [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en el origen de medios, como se describe en el tema Proveedores de metadatos [de Shell](shell-metadata-providers.md).

Para crear un controlador de propiedades personalizado, haga lo siguiente:

-   Implemente [**la interfaz IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) para exponer [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) El GUID del servicio es **MF \_ PROPERTY HANDLER \_ \_ SERVICE.**
-   Si el origen de medios se va a usar de forma remota, también debe exponer la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a través del método **QueryInterface** del origen multimedia, además de [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice).
-   Para que el controlador de propiedades esté disponible para el sistema de propiedades de Shell, registre el archivo DLL para el controlador de propiedades como se describe en Registrar y distribuir [controladores de propiedades](../properties/prophand-reg-dist.md).
-   El origen de medios se registra por separado, como se describe en [Controladores de esquemas y Byte-Stream controladores](scheme-handlers-and-byte-stream-handlers.md).

### <a name="implementation-tips"></a>Implementación Sugerencias

Para obtener una lista de claves de propiedad de metadatos, vea [Propiedades de metadatos para archivos multimedia.](metadata-properties-for-media-files.md)

Los controladores de propiedades deben ser rápidos; deben proporcionar acceso eficaz de lectura y escritura a los metadatos. (Tenga en cuenta que shell puede recuperar metadatos de cientos de archivos). Por lo tanto, no llame a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) desde el controlador de propiedades. La **función MFStartup** introduce la latencia de inicio, ya que crea varios subprocesos de cola de trabajo y asigna memoria global.

En una implementación típica, el controlador de propiedades y el origen multimedia compartirán parte del mismo código de análisis. Sin embargo, un origen multimedia usa llamadas [**ASINCRÓNICASByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) asincrónicas para E/S, mientras que el controlador de propiedades usa la [**interfaz IStream.**](/windows/win32/api/objidl/nn-objidl-istream) Media Foundation proporciona un objeto auxiliar que encapsula un flujo basado en **IStream** y lo expone como un **flujo DE TIPO IMFByteStream.** Para crear el contenedor, llame a [**MFCreateMFByteStreamOnStream**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemfbytestreamonstream).

Al actualizar los metadatos, se recomienda escribir los datos directamente en la secuencia original. Esta recomendación difiere del comportamiento *de copia* en escritura de la mayoría de los controladores de propiedades, en los que se modifica una copia de los datos. Los archivos multimedia pueden ser muy grandes, por lo que la copia en escritura suele ser demasiado lenta para una implementación eficaz. Para deshabilitar la copia en escritura, establezca la configuración del Registro **ManualSafeSave,** como se describe en Registrar y distribuir [controladores de propiedades](../properties/prophand-reg-dist.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Metadatos multimedia](media-metadata.md)
</dt> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Escribir un origen multimedia personalizado](writing-a-custom-media-source.md)
</dt> </dl>

 

 
