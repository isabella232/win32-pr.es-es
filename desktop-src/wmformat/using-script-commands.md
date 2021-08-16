---
title: Uso de comandos de script
description: Uso de comandos de script
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows SDK de formato multimedia, comandos de script
- Formato de sistemas avanzados (ASF), comandos de script
- ASF (formato de sistemas avanzados), comandos de script
- scripts, comandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b77de3e892d4f7b479822442a2637849df3d4bcd56273deb952246fba14f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195791"
---
# <a name="using-script-commands"></a>Uso de comandos de script

El SDK Windows Media Format admite el uso de comandos de script para comunicar acciones de aplicación en archivos ASF. Cada comando de script se forma de dos cadenas, la primera cadena es el tipo de comando y la segunda son los datos del comando. Por ejemplo, puede usar el tipo de script "URL" y pasar una dirección URL de Internet válida como datos de comando. Cuando una aplicación de lectura que admite comandos de script de tipo "URL" recibe este comando, se abrirá la dirección especificada en una ventana del explorador.

El SDK Windows Media Format proporciona dos opciones para entregar scripts en archivos ASF. Puede crear una secuencia de scripts o puede incluir comandos de script en el encabezado del archivo. Las secuencias de script son útiles porque los comandos de script se entregan en el orden de tiempo de presentación. Si usa comandos de script en el encabezado de archivo, la aplicación deberá recuperar todos los comandos de script antes de iniciar la reproducción. Debe realizar un seguimiento de los tiempos de presentación de los comandos de script y responder a ellos en el momento adecuado.

En las secciones siguientes se describe cómo incluir comandos de script en un archivo ASF.



| Sección                                                                                                                | Descripción                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Para usar una secuencia de scripts](to-use-a-script-stream.md)                                                                   | Describe cómo incluir comandos de script en una secuencia de scripts. |
| [Para agregar datos de script al encabezado](to-add-script-data-to-the-header.md)                                               | Describe cómo incluir comandos de script en el encabezado de archivo. |
| [Uso de comandos de script admitidos por Reproductor de Windows Media](using-script-commands-supported-by-windows-media-player.md) | Describe los comandos de script usados por Reproductor de Windows Media.  |



 

> [!Note]  
> En versiones anteriores del SDK Windows Media Format, se usaban secuencias de script para abrir direcciones web correspondientes al contenido de un archivo ASF. Ahora puede usar secuencias web para trabajar con páginas web sincronizadas. Para obtener más información, vea [Web Secuencias](web-streams.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Comandos de script**](script-commands.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 




