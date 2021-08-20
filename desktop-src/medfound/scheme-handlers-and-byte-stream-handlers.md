---
description: En este tema se describen los detalles internos de cómo el solucionador de origen crea un origen multimedia.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Controladores de esquema y Byte-Stream de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7bde81a02762cd9c82e0a7d031582c856da6984ab231775580ddf249caca23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058239"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a>Controladores de esquema y Byte-Stream de esquema

En este tema se describen los detalles internos de cómo el solucionador de origen crea un origen multimedia. Lea este tema si va a implementar un origen multimedia personalizado para Media Foundation y desea que el origen multimedia esté disponible para las aplicaciones a través de la resolución de origen.

El solucionador de origen puede crear un origen multimedia a partir de una dirección URL o de una secuencia de bytes (es decir, un [**puntero IMFByteStream).**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) Para ello, usa objetos auxiliares *denominados controladores*. Para las direcciones URL, el solucionador de origen usa *controladores de esquema*. En el caso de las secuencias de bytes, usa *controladores de flujo de bytes*.

Un controlador de esquema toma una dirección URL como entrada y crea un origen multimedia o una secuencia de bytes. Si crea una secuencia de bytes, el solucionador de origen lo pasará a un controlador de flujo de bytes, que crea el origen multimedia. En la imagen siguiente se muestra este proceso.

![diagrama que muestra el proceso de resolución de origen](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a>Controladores de esquemas

Los controladores de esquema se usan cuando la aplicación llama [**a IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) o a su equivalente asincrónico, [**BeginCreateObjectFromURL.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)

El solucionador de origen busca controladores de esquema en el Registro. Los controladores de esquema se enumeran por esquema de dirección URL, bajo las siguientes claves:

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

donde *<scheme>* es el esquema de dirección URL que el controlador está diseñado para analizar. El esquema incluye el carácter final ":"; por ejemplo, "http:".

Para registrar un nuevo controlador de esquema, agregue una entrada cuyo nombre sea el CLSID del controlador de esquema, en forma de cadena canónica: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` . El valor de la entrada es una cadena (REG SZ) que contiene una breve descripción del controlador, como \_ "Mi controlador de esquema". La parte importante de la entrada es el CLSID. La resolución de origen crea el controlador mediante una llamada **a CoCreateInstance** con este CLSID.

Los controladores de esquema exponen la [**interfaz IMFSchemeHandler.**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) Si el solucionador de origen encuentra un controlador de esquema que coincide con el esquema de dirección URL, el solucionador de origen llama a [**IMFSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), pasando la dirección URL original. El controlador de esquema abrirá la dirección URL e intentará analizar el contenido. En ese momento, el controlador de esquema tiene dos opciones:

-   Cree un origen multimedia.
-   Cree una secuencia de bytes.

Si crea un origen multimedia, el solucionador de origen devuelve el origen de medios a la aplicación. Si crea una secuencia de bytes, el solucionador de origen intenta encontrar un controlador de flujo de bytes adecuado, como se describe en la sección siguiente.

## <a name="byte-stream-handlers"></a>Byte-Stream controladores

Los controladores de flujo de bytes se usan cuando la aplicación llama a [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) o a su equivalente asincrónico, [**BeginCreateObjectFromByteStream.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) También se usan cuando un controlador de esquema devuelve una secuencia de bytes, como se describió anteriormente.

Al igual que con los controladores de esquema, los controladores de flujo de bytes se enumeran en el Registro. Se enumeran por extensión de nombre de archivo o tipo MIME (o ambos), bajo las siguientes claves:

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

donde *<ExtensionOrMimeType>* es la extensión de nombre de archivo o el tipo MIME. Las extensiones de archivo incluyen el carácter inicial "."; por ejemplo, ".wmv".

La extensión de nombre de archivo forma parte de la dirección URL proporcionada por la aplicación. El tipo MIME puede estar disponible a través del atributo [**MF \_ BYTESTREAM \_ CONTENT \_ TYPE**](mf-bytestream-content-type-attribute.md) en la secuencia de bytes.

Para registrar un nuevo controlador de flujo de bytes, agregue una entrada cuyo nombre sea el CLSID del controlador, en forma de cadena canónica. El valor de la entrada es una cadena (REG SZ) que contiene una breve descripción del controlador, como \_ "My Byte-Stream Handler". La resolución de origen llama **a CoCreateInstance** para crear el controlador a partir del CLSID. Puede registrar el mismo controlador en más de una extensión o tipo MIME.

Los controladores de flujo de bytes exponen [**la interfaz IMFByteStreamHandler.**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) Si el solucionador de origen encuentra un controlador de flujo de bytes que coincida, llama a [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). La entrada a este método es un puntero a la secuencia de bytes, además de la dirección URL original, si está disponible. El controlador de flujo de bytes lee de la secuencia de bytes hasta que analiza suficientes datos para crear el origen multimedia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solucionador de origen](source-resolver.md)
</dt> </dl>

 

 



