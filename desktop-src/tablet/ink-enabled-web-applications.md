---
description: El ejemplo ink Blog muestra varias técnicas útiles que se pueden usar en aplicaciones web habilitadas para lápiz.
ms.assetid: 4a5a453d-e3c1-40e6-b0eb-99009f0024dd
title: Ink-Enabled Web Applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8097bd55c34abbcb4469d74642e9dbc9a5f29e3b0b7110a76543fd40f5b1ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043496"
---
# <a name="ink-enabled-web-applications"></a>Ink-Enabled Web Applications

El [ejemplo ink Blog](ink-blog-web-sample.md) muestra varias técnicas útiles que se pueden usar en aplicaciones web habilitadas para lápiz. Estas incluyen: probar si la máquina cliente puede admitir controles habilitados para entrada de lápiz, enviar datos de entrada de lápiz a un servidor y mostrar datos de entrada de lápiz en una página web.

## <a name="testing-ink-enablement"></a>Prueba de la habilitación de entrada de lápiz

Puede ser útil probar si la máquina cliente puede mostrar controles habilitados para entrada de lápiz. Esto le permite tener la páginawebmostrar un control si el cliente es un tablet PC o otro diferente si no lo es. Una manera de probar esto es intentar crear un objeto como [InkOverlay](/previous-versions/ms833057(v=msdn.10)), que solo se puede crear en una máquina que tenga instalado el kit de desarrollo de software (SDK) de Windows Vista, Windows XP Tablet PC Edition o Windows XP Tablet PC Edition Software Development Kit (SDK). Si crea el objeto dentro de un bloque try/catch y detecta las excepciones que se inician (a menudo se produce una [excepción FileNotFoundException](/previous-versions/windows/) para indicar que no se encuentra el ensamblado con este control), puede detectar si el equipo cliente puede admitir controles habilitados para lápiz. En el ejemplo, este código se puede encontrar en el constructor de la `InkArea` clase .

## <a name="submitting-ink-data"></a>Envío de datos de entrada de lápiz

Una manera sencilla de enviar datos es tomar los datos del control habilitado para lápiz, transferirlo a un formulario oculto y, a continuación, enviar el formulario. La entrada de lápiz se puede serializar mediante [el método Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) y, a continuación, se convierte en una cadena. En el ejemplo, el formulario oculto se define en AddBlog.aspx y la serialización de entrada de lápiz se controla en , donde la entrada de lápiz se serializa en una `InkArea.SerializeInkData` imagen GIF. (Tenga en cuenta que también se podría serializar de forma similar en otros formatos, como el formato serializado de entrada de lápiz (ISF).

## <a name="displaying-ink-data"></a>Mostrar datos de entrada de lápiz

En el ejemplo, AddBlog.aspx.cs tiene un método denominado que recupera los datos que se publican en el servidor y `Page_Load` los guarda en archivos. A continuación, genera páginas web en el servidor que contienen etiquetas img que hacen referencia a los archivos con las imágenes GIF. Ahora solo tiene que ir a esas páginas para ver imágenes de la entrada de lápiz. (Tenga en cuenta que si hubiera serializado la entrada de lápiz con un formato diferente, como Ink Serialized Format (ISF), tendría que convertir la entrada de lápiz en una imagen en el servidor para mostrarla en clientes que no son tabletas).

Los clientes de Tablet PC pueden volver a cargar la entrada de lápiz en un control habilitado para la entrada de lápiz y permitir que el usuario edite la entrada de lápiz mediante ISF. Esto es así incluso para la entrada de lápiz guardada con el valor **Gif** de la enumeración [PersistenceFormat,](/previous-versions/ms827245(v=msdn.10)) porque los datos de ISF están contenidos en los metadatos GIF.

 

 
