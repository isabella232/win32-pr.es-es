---
title: Negociación de Media-Type
description: Muchos protocolos de Internet de la capa de aplicación se basan en el intercambio de mensajes en un formato simple y flexible denominado Extensiones multipropósito de correo Internet (MIME).
ms.assetid: 7a2c9d8f-639a-4865-a62b-63330175f5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb145fa3a76da6574172ddd24888f3b5da7ad85e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421471"
---
# <a name="media-type-negotiation"></a>Negociación de Media-Type

Muchos protocolos de Internet de la capa de aplicación se basan en el intercambio de mensajes en un formato simple y flexible denominado Extensiones multipropósito de correo Internet (MIME). Aunque MIME se originó como estándar para intercambiar mensajes de correo electrónico, se usa hoy en una amplia variedad de aplicaciones para especificar formatos de datos comprendidos mutuamente como tipos MIME o multimedia. El proceso se denomina *negociación de tipo de medio*.

Los tipos de medios son cadenas simples que denotan un tipo y un subtipo (como "texto/sin formato" o "texto/HTML"). Se usan para etiquetar datos o calificar una solicitud. Un explorador Web, por ejemplo, como parte de una solicitud HTTP-for-Data o de Request-for-info, especifica que está solicitando tipos de medios "image/gif" o "image/JPEG", a los que un servidor web responde devolviendo el tipo de medio adecuado y, si la llamada era una solicitud de datos, los propios datos en el formato solicitado.

La negociación del tipo de medio suele ser similar a la forma en que las aplicaciones de escritorio existentes negocian con el Portapapeles del sistema para determinar qué formato de datos se debe pegar cuando un usuario elige editar/pegar o consultas para formatos al recibir un puntero [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) durante una operación de arrastrar y colocar. La sutil diferencia en la negociación del tipo de medio HTTP es que el cliente no conoce con anterioridad el tiempo que tiene disponible el formato del servidor. Por lo tanto, el cliente especifica los tipos de medios que admite, en orden de mayor fidelidad, y el servidor responde con el mejor formato disponible.

Los monikers de dirección URL admiten la negociación de tipo de medio para que los clientes y servidores de Internet acepten los formatos que se van a usar al descargar datos en operaciones de [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) . Para admitir la negociación de tipo de medio, un cliente implementa la interfaz [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) y llama a la función [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85)) para registrarla con el contexto de enlace. El enumerador de formato muestra los formatos que el cliente puede aceptar. Un moniker de dirección URL traduce estos formatos en tipos de medios al enlazar con direcciones URL HTTP.

Los posibles tipos de medios solicitados por el cliente se representan como moniker de dirección URL a través de las estructuras [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) disponibles en el enumerador [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) registrado por el autor de la llamada en el contexto de enlace: cada **FORMATETC** especifica un formato de Portapapeles que identifica el tipo de medio. Por ejemplo, el fragmento de código siguiente especifica que el tipo de medio es PostScript.

``` syntax
FORMATETC fmtetc;
fmtetc.cfFormat = RegisterClipboardFormat(CF_MIME_POSTSCRIPT);
. . .
```

Un cliente puede establecer el formato del portapapeles en el tipo de medio especial CF \_ null para indicar que debe recuperarse el tipo de medio predeterminado del recurso al que apunta la dirección URL. Normalmente, este formato es el último en el que el cliente está interesado. Cuando no se registra ningún enumerador con el contexto de enlace, un moniker de dirección URL funciona como si un enumerador que contiene un solo [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) con **cfFormat**= CF \_ null está disponible, y descarga automáticamente el tipo de medio predeterminado.

Sea cual sea el tipo de medio que se va a usar, el cliente recibe una notificación de la opción por medio del argumento *pformatetc* en su método [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) . La devolución de llamada se produce en el contexto de la llamada del cliente a [**BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage).

> [!Note]  
> Si el contenido recibido es de un tipo de medio no reconocido, el cliente llama automáticamente a [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) para registrar el nuevo tipo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers de URL](url-monikers.md)
</dt> </dl>

 

 