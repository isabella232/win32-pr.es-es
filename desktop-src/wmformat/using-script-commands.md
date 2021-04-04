---
title: Usar comandos de script
description: Usar comandos de script
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- SDK de Windows Media Format, comandos de script
- Advanced Systems Format (ASF), comandos de script
- ASF (formato de sistemas avanzados), comandos de script
- scripts, comandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075805"
---
# <a name="using-script-commands"></a>Usar comandos de script

El SDK de Windows Media Format admite el uso de comandos de script para comunicar acciones de aplicación en archivos ASF. Cada comando de script se compone de dos cadenas, la primera cadena es el tipo de comando, la segunda son los datos del comando. Por ejemplo, puede usar el tipo de script "URL" y pasar una dirección URL de Internet válida como datos del comando. Cuando una aplicación de lectura que admite comandos de script de tipo "URL" recibe este comando, abrirá la dirección especificada en una ventana del explorador.

El SDK de Windows Media Format proporciona dos opciones para entregar el script en archivos ASF. Puede crear una secuencia de script o puede incluir comandos de script en el encabezado del archivo. Los flujos de script son útiles porque los comandos de script se entregan en el orden temporal de presentación. Si usa comandos de script en el encabezado de archivo, la aplicación tendrá que recuperar todos los comandos de script antes de iniciar la reproducción. Debe realizar un seguimiento de los tiempos de presentación de los comandos de script y responder a ellos en el momento adecuado.

En las secciones siguientes se describe cómo incluir comandos de script en un archivo ASF.



| Sección                                                                                                                | Descripción                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Para usar una secuencia de script](to-use-a-script-stream.md)                                                                   | Describe cómo incluir comandos de script en una secuencia de scripts. |
| [Para agregar datos de script al encabezado](to-add-script-data-to-the-header.md)                                               | Describe cómo incluir comandos de script en el encabezado de archivo. |
| [Usar comandos de script compatibles con Windows Media Player](using-script-commands-supported-by-windows-media-player.md) | Describe los comandos de script utilizados por Media Player de Windows.  |



 

> [!Note]  
> En versiones anteriores del SDK de Windows Media Format, las secuencias de comandos se usaban para abrir direcciones web correspondientes al contenido de un archivo ASF. Ahora puede usar secuencias web para trabajar con páginas web sincronizadas. Para obtener más información, vea [secuencias web](web-streams.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Comandos de script**](script-commands.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 




