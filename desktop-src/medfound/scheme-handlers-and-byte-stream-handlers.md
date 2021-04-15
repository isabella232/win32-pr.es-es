---
description: En este tema se describen los detalles internos del modo en que la resolución de origen crea un origen de medios.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Controladores de esquema y controladores de Byte-Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54976f45c7f07e12b6f095297231d306d0644704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715498"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a>Controladores de esquema y controladores de Byte-Stream

En este tema se describen los detalles internos del modo en que la resolución de origen crea un origen de medios. Lea este tema si va a implementar un origen multimedia personalizado para Media Foundation y desea que el origen de medios esté disponible para las aplicaciones a través de la resolución de origen.

La resolución de origen puede crear un origen multimedia a partir de una dirección URL o de una secuencia de bytes (es decir, un puntero [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) ). Para ello, usa objetos auxiliares denominados *Controladores*. En el caso de las direcciones URL, la resolución de origen usa *controladores de esquema*. En el caso de secuencias de bytes, usa *controladores de secuencia de bytes*.

Un controlador de esquema toma una dirección URL como entrada y crea un origen multimedia o un flujo de bytes. Si crea una secuencia de bytes, la resolución de origen la pasará a un controlador de flujo de bytes, que crea el origen de los medios. En la imagen siguiente se ilustra este proceso.

![diagrama que muestra el proceso de resolución de origen](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a>Controladores de esquema

Los controladores de esquema se usan cuando la aplicación llama a [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) o su equivalente asincrónico, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).

La resolución de origen busca controladores de esquema en el registro. Los controladores de esquema se enumeran según el esquema de direcciones URL, con las claves siguientes:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

donde *<scheme>* es el esquema de la dirección URL que el controlador está diseñado para analizar. El esquema incluye el carácter ': ' final; por ejemplo, "http:".

Para registrar un nuevo controlador de esquema, agregue una entrada cuyo nombre sea el CLSID del controlador de esquema, en formato de cadena canónico: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . El valor de la entrada es una cadena (REG \_ SZ) que contiene una breve descripción del controlador, como "mi esquema controlador". La parte importante de la entrada es el CLSID. La resolución de origen crea el controlador mediante una llamada a **CoCreateInstance** con este CLSID.

Los controladores de esquema exponen la interfaz [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) . Si la resolución de origen encuentra un controlador de esquema que coincide con el esquema de la dirección URL, el solucionador de origen llama a [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), pasando la dirección URL original. El controlador de esquema abrirá la dirección URL e intentará analizar el contenido. En ese momento, el controlador de esquema tiene dos opciones:

-   Cree un origen de medios.
-   Cree una secuencia de bytes.

Si crea un origen de medios, la resolución de origen devuelve el origen de medios a la aplicación. Si crea una secuencia de bytes, el solucionador de origen intenta encontrar un controlador de secuencia de bytes adecuado, tal y como se describe en la sección siguiente.

## <a name="byte-stream-handlers"></a>Controladores de Byte-Stream

Los controladores de secuencias de bytes se usan cuando la aplicación llama a [**IMFSourceResolver:: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) o su equivalente asincrónico, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream). También se usan cuando un controlador de esquema devuelve una secuencia de bytes, como se ha descrito anteriormente.

Al igual que con los controladores de esquema, los controladores de secuencias de bytes se enumeran en el registro. Se enumeran por extensión de nombre de archivo o tipo MIME (o ambos), en las claves siguientes:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

donde *<ExtensionOrMimeType>* es la extensión de nombre de archivo o el tipo MIME. Las extensiones de archivo incluyen el carácter '. ' inicial; por ejemplo, ". WMV".

La extensión de nombre de archivo forma parte de la dirección URL, proporcionada por la aplicación. El tipo MIME podría estar disponible a través del atributo de [**\_ tipo de \_ contenido \_ MF BYTESTREAM**](mf-bytestream-content-type-attribute.md) en la secuencia de bytes.

Para registrar un nuevo controlador de flujo de bytes, agregue una entrada cuyo nombre sea el CLSID del controlador, en formato de cadena canónico. El valor de la entrada es una cadena (REG \_ SZ) que contiene una breve descripción del controlador, como "mi controlador de Byte-Stream". La resolución de origen llama a **CoCreateInstance** para crear el controlador a partir del CLSID. Puede registrar el mismo controlador en más de una extensión o tipo MIME.

Los controladores de flujo de bytes exponen la interfaz [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) . Si la resolución de origen encuentra un controlador de secuencia de bytes coincidente, llama a [**IMFByteStreamHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). La entrada a este método es un puntero a la secuencia de bytes, más la dirección URL original, si está disponible. El controlador de flujo de bytes lee el flujo de bytes hasta que analiza los datos suficientes para crear el origen de medios.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solucionador de origen](source-resolver.md)
</dt> </dl>

 

 



