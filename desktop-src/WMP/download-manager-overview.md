---
title: Información general del administrador de descargas
description: Información general del administrador de descargas
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player tiendas en línea, administrador de descargas
- tiendas en línea, administrador de descargas
- tipo 2 tiendas en línea, administrador de descargas
- Windows Media Player tiendas en línea, descarga en tiempo real
- tiendas en línea, descarga en tiempo real
- tipo 2 tiendas en línea, descarga en tiempo real
- Windows Media Player tiendas en línea, descarga en segundo plano
- tiendas en línea, descarga en segundo plano
- tipo 2 tiendas en línea, descarga en segundo plano
- Windows Media Player, administrador de descargas
- Administrador de descargas de Windows Media Player
- Administrador de descargas
- descarga en tiempo real
- descarga en segundo plano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076267"
---
# <a name="download-manager-overview"></a>Información general del administrador de descargas

Microsoft Windows Media Player proporciona paneles de tareas de la tienda en línea que contienen una ventana de explorador hospedada. A través de las tiendas en línea, los usuarios pueden interactuar con las páginas web de la tienda en línea a través de Internet.

El administrador de descargas de Windows Media Player proporciona un modelo de objetos que puede usar para controlar las tareas asociadas a la descarga de contenido en el equipo del usuario desde Microsoft Internet Information Services (IIS) mediante el protocolo de transferencia de hipertexto (HTTP). Con Download Manager, puede:

-   Administrar varias descargas simultáneamente como una colección.
-   Especifique una dirección URL para un archivo e inicie su descarga mediante HTTP.
-   Consulte el estado y el progreso de la descarga.
-   Pausar, reanudar o cancelar una descarga.
-   Especifique si se produce una descarga en segundo plano o en tiempo real. (La descarga en segundo plano solo está disponible en el sistema operativo Microsoft Windows XP). Vea [acerca de la descarga en segundo plano y en tiempo real](#about-background-and-real-time-downloading).
-   Especifique cómo se muestra el contenido en la biblioteca. Vea [acerca de la integración de bibliotecas](#about-library-integration).

Download Manager es la solución para descargar contenido del código de script en páginas web hospedadas. Para descargar contenido con código de C++, use el Servicio de transferencia inteligente en segundo plano de Windows XP (BITS). Para obtener más información, vea [bits](bits.md).

## <a name="about-background-and-real-time-downloading"></a>Acerca de la descarga en segundo plano y en tiempo real

Download Manager ofrece dos tipos de descarga: en segundo plano y en tiempo real. El tipo que use depende de usted, y es posible permitir que el usuario seleccione también el tipo de descarga. Si decide permitir al usuario seleccionar el tipo de descarga, asegúrese de explicar las diferencias entre los dos tipos disponibles.

La descarga en tiempo real se produce a la vez. Cuando el usuario inicia una descarga de archivos, todo el archivo se transfiere al equipo del usuario en un flujo único y continuo. El usuario no puede pausar ni interrumpir la descarga. Si el usuario elige cerrar Windows Media Player antes de que finalice la descarga, pierde todos los archivos incompletos y debe descargarlos desde el principio para adquirir el contenido.

La principal ventaja de la descarga en tiempo real es que permite al usuario adquirir el contenido más rápido que la descarga en segundo plano. La descarga en tiempo real está disponible para los usuarios de Windows XP, pero es el único tipo de descarga disponible en las versiones del sistema operativo Windows anteriores a Windows XP.

La descarga en segundo plano se produce de manera escalonada. Cuando el usuario inicia una descarga en segundo plano, las partes del archivo se transfieren al equipo del usuario cuando está disponible el tiempo de procesador. Es posible pausar y reanudar una descarga en segundo plano. Si el usuario elige cerrar Windows Media Player antes de que finalice la descarga en segundo plano, se guarda la condición de los archivos incompletos y la descarga puede continuar en segundo plano, incluso después de reiniciar el equipo.

La descarga en segundo plano puede tardar más que la descarga en tiempo real, ya que el proceso de descarga solo se produce cuando el procesador no realiza otras tareas.

La descarga en segundo plano solo está disponible cuando se usa Windows XP.

## <a name="about-library-integration"></a>Acerca de la integración de bibliotecas

Windows Media Player puede organizar automáticamente el contenido de la tienda en línea en la biblioteca. Para ello, debe especificar un valor para el atributo **WM/ContentDistributor** para cada archivo multimedia digital. Cuando se agrega un archivo multimedia digital a la biblioteca, que se produce automáticamente al usar el administrador de descargas, el archivo aparece automáticamente en el nodo **música comprada** o **vídeos comprados** . Por ejemplo, si el valor de **WM/ContentDistributor** es "Proseware" y el archivo multimedia digital contiene música, el contenido aparecerá en la biblioteca en la siguiente ubicación:

Toda la música/música comprada/Proseware

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administrador de descargas**](download-manager.md)
</dt> <dt>

[**DownloadCollection.startDownload**](downloadcollection-startdownload.md)
</dt> </dl>

 

 




