---
title: Media-Type negociación
description: Muchos protocolos de Internet del nivel de aplicación se basan en el intercambio de mensajes en un formato sencillo y flexible denominado Extensiones multipropósito de correo de Internet (MIME).
ms.assetid: 7a2c9d8f-639a-4865-a62b-63330175f5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb145fa3a76da6574172ddd24888f3b5da7ad85e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359833"
---
# <a name="media-type-negotiation"></a>Media-Type negociación

Muchos protocolos de Internet del nivel de aplicación se basan en el intercambio de mensajes en un formato sencillo y flexible denominado Extensiones multipropósito de correo de Internet (MIME). Aunque MIME se originó como un estándar para intercambiar mensajes de correo electrónico, hoy en día lo usan una amplia variedad de aplicaciones para especificar formatos de datos que se entiendan mutuamente como tipos MIME o multimedia. El proceso se denomina *negociación de tipo multimedia*.

Los tipos multimedia son cadenas simples que denotan un tipo y un subtipo (como "text/plain" o "text/HTML"). Se usan para etiquetar datos o calificar una solicitud. Un explorador web, por ejemplo, como parte de una solicitud HTTP-for-data o request-for-info, especifica que solicita tipos multimedia "image/gif" o "image/jpeg", a los que un servidor web responde devolviendo el tipo de medio adecuado y, si la llamada era una solicitud de datos, los propios datos en el formato solicitado.

La negociación de tipo multimedia suele ser similar a la forma en que las aplicaciones de escritorio existentes negocian con el Portapapeles del sistema para determinar qué formato de datos se va a pegar cuando un usuario elige Editar/Pegar o consulta los formatos al recibir un puntero [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) durante una operación de arrastrar y colocar. La diferencia sutil en la negociación de tipo de medio HTTP es que el cliente no sabe con antelación qué formatos tiene disponibles el servidor. Por lo tanto, el cliente especifica por adelantado los tipos de medios que admite, en orden de máxima fidelidad, y el servidor responde con el mejor formato disponible.

Los monikers de url admiten la negociación de tipo multimedia como una manera de que los clientes y servidores de Internet acepten los formatos que se usarán al descargar datos en operaciones [**BindToStorage.**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) Para admitir la negociación de tipo multimedia, un cliente implementa la interfaz [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) y llama a la función [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85)) para registrarla con el contexto de enlace. El enumerador de formato enumera los formatos que el cliente puede aceptar. Un moniker de dirección URL convierte estos formatos en tipos multimedia al enlazar a direcciones URL HTTP.

Los posibles tipos de medios solicitados por el cliente se representan en monikers de dirección URL a través de estructuras [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) disponibles en el enumerador [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) registrado por el autor de la llamada en el contexto de enlace: cada **FORMATETC** especifica un formato de Portapapeles que identifica el tipo de medio. Por ejemplo, el siguiente fragmento de código especifica que el tipo de medio es PostScript.

``` syntax
FORMATETC fmtetc;
fmtetc.cfFormat = RegisterClipboardFormat(CF_MIME_POSTSCRIPT);
. . .
```

Un cliente puede establecer el formato del Portapapeles en el tipo de medio especial CF NULL para indicar que se debe recuperar el tipo de medio predeterminado del recurso al que apunta \_ la dirección URL. Este formato suele ser el último en el que el cliente está interesado. Cuando no se registra ningún enumerador con el contexto de enlace, un moniker de dirección URL funciona como si hubiera disponible un enumerador que contiene un [**solo FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) con **cfFormat**=CF NULL, descargando automáticamente el tipo de medio \_ predeterminado.

Sea cual sea el tipo de medio que se va a usar, se notifica al cliente la elección mediante el argumento *pformatetc* en su [**método IBindStatusCallback::OnDataAvailable.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) La devolución de llamada se produce en el contexto de la llamada del cliente [**a BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage).

> [!Note]  
> Si el contenido recibido es de un tipo multimedia desconocido, el cliente llama automáticamente a [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) para registrar el nuevo tipo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[URL Monikers](url-monikers.md)
</dt> </dl>

 

 