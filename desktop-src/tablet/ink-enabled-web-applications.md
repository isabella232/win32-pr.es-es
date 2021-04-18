---
description: En el ejemplo de blog de tinta se muestran varias técnicas útiles que se pueden usar en aplicaciones web habilitadas para tinta.
ms.assetid: 4a5a453d-e3c1-40e6-b0eb-99009f0024dd
title: Ink-Enabled aplicaciones Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b14e368c1d2e97e35afa6d72a0fe082f304c5fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715085"
---
# <a name="ink-enabled-web-applications"></a>Ink-Enabled aplicaciones Web

En el ejemplo de [blog de tinta](ink-blog-web-sample.md) se muestran varias técnicas útiles que se pueden usar en aplicaciones web habilitadas para tinta. Entre ellas se incluyen: probar si el equipo cliente puede admitir controles habilitados para tinta, enviar datos de tinta a un servidor y Mostrar datos de tinta en una página web.

## <a name="testing-ink-enablement"></a>Comprobar la habilitación de la tinta

Puede ser útil para probar si el equipo cliente puede mostrar controles habilitados para tinta. Esto le permite tener thewebpageshow un control si el cliente es un Tablet PC o uno diferente si no lo es. Una manera de probarlo es intentar crear un objeto como [InkOverlay](/previous-versions/ms833057(v=msdn.10)), que solo se puede crear en una máquina que tenga instalado el sistema operativo Windows Vista, Windows XP Tablet PC Edition o el kit de desarrollo de software (SDK) de Windows XP Tablet PC Edition. Si crea el objeto dentro de un bloque try/catch y detecta cualquier excepción que se produzca (a menudo se inicia una excepción [FileNotFoundException](/previous-versions/windows/) para indicar que no se puede encontrar el ensamblado con este control), puede detectar si el equipo cliente puede admitir controles habilitados para tinta. En el ejemplo, este código se puede encontrar en el constructor de la `InkArea` clase.

## <a name="submitting-ink-data"></a>Enviar datos de tinta

Una manera sencilla de enviar datos es tomar los datos del control habilitado para la entrada de lápiz, transferirlos a un formulario oculto y, a continuación, enviar el formulario. La entrada de lápiz se puede serializar utilizando el método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) y, a continuación, se convierte en una cadena. En el ejemplo, el formulario oculto se define en AddBlog. aspx y la serialización de la tinta se controla en `InkArea.SerializeInkData` , donde la tinta se serializa en una imagen GIF. (Tenga en cuenta que también se puede serializar de forma similar en otros formatos, como el formato serializado de tinta (ISF)).

## <a name="displaying-ink-data"></a>Mostrar datos de tinta

En el ejemplo, AddBlog. aspx. CS tiene un método llamado `Page_Load` que recupera los datos que se publican en el servidor y los guarda en archivos. A continuación, genera páginas web en el servidor que contiene etiquetas IMG que hacen referencia a los archivos con las imágenes GIF. Ahora solo tiene que ir a esas páginas para ver las imágenes de la tinta. (Tenga en cuenta que si ha serializado la tinta con un formato diferente, como el formato serializado de entrada de lápiz (ISF), deberá convertir la tinta en una imagen del servidor para mostrarla en clientes que no sean tabletas).

Los clientes de Tablet PC pueden volver a cargar la entrada manuscrita en un control habilitado para tinta y permitir que el usuario edite la tinta mediante ISF. Esto es así incluso para la entrada de lápiz guardada con el valor **GIF** de la enumeración [PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) , porque los datos de ISF están contenidos en los metadatos GIF.

 

 
