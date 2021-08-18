---
title: Introducción al Administrador de descarga
description: Introducción al Administrador de descarga
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Reproductor de Windows Media online stores,Download Manager
- tiendas en línea, Administrador de descarga
- tiendas en línea de tipo 2, Administrador de descarga
- Reproductor de Windows Media en línea, descarga en tiempo real
- tiendas en línea, descarga en tiempo real
- tiendas en línea de tipo 2, descarga en tiempo real
- Reproductor de Windows Media en línea, descarga en segundo plano
- tiendas en línea, descarga en segundo plano
- tiendas en línea de tipo 2, descarga en segundo plano
- Reproductor de Windows Media,Download Manager
- Reproductor de Windows Media Administrador de descarga
- Administrador de descarga
- descarga en tiempo real
- descarga en segundo plano
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790466db4c09f7c2310729bd6f866bc5066348641a73756eb9199aa685a7fafe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997085"
---
# <a name="download-manager-overview"></a>Introducción al Administrador de descarga

Microsoft Reproductor de Windows Media proporciona paneles de tareas de la tienda en línea que contienen una ventana del explorador hospedado. A través de las tiendas en línea, los usuarios pueden interactuar con las páginas web de la tienda en línea a través de Internet.

El Administrador de descarga de Reproductor de Windows Media proporciona un modelo de objetos que puede usar para controlar las tareas asociadas a la descarga de contenido en el equipo del usuario desde Microsoft Internet Information Services (IIS) mediante el Protocolo de transferencia de hipertexto (HTTP). Con el Administrador de descargas, puede hacer lo siguiente:

-   Administrar varias descargas simultáneamente como una colección.
-   Especifique una dirección URL para un archivo e inicie la descarga mediante HTTP.
-   Consulte el estado y el progreso de la descarga.
-   Pausar, reanudar o cancelar una descarga.
-   Especifique si una descarga se produce en segundo plano o en tiempo real. (La descarga en segundo plano solo está disponible en el sistema operativo Microsoft Windows XP). Vea [Acerca de la descarga en tiempo real y en segundo plano.](#about-background-and-real-time-downloading)
-   Especifique cómo se muestra el contenido en la biblioteca. Consulte [Acerca de la integración de bibliotecas.](#about-library-integration)

El Administrador de descarga es la solución para descargar contenido del código de script en páginas web hospedadas. Para descargar contenido mediante código de C++, use el Windows XP Servicio de transferencia inteligente en segundo plano (BITS). Para obtener más información, vea [BITS](bits.md).

## <a name="about-background-and-real-time-downloading"></a>Acerca de la descarga en segundo plano y en tiempo real

El Administrador de descarga ofrece dos tipos de descarga: en segundo plano y en tiempo real. El tipo que use es su función y es posible permitir que el usuario seleccione también el tipo de descarga. Si decide permitir que el usuario seleccione el tipo de descarga, asegúrese de explicar las diferencias entre los dos tipos disponibles.

La descarga en tiempo real se produce a la vez. Cuando el usuario inicia una descarga de archivos, todo el archivo se transfiere al equipo del usuario en una única secuencia continua. El usuario no puede pausar o interrumpir la descarga. Si el usuario decide cerrar Reproductor de Windows Media antes de que finalice la descarga, pierde los archivos incompletos y debe descargarlos desde el principio para adquirir el contenido.

La principal ventaja de la descarga en tiempo real es que permite al usuario adquirir el contenido más rápido que la descarga en segundo plano. La descarga en tiempo real está disponible para los usuarios de Windows XP, pero es el único tipo de descarga disponible en las versiones del sistema operativo Windows antes de Windows XP.

La descarga en segundo plano se produce por completo. Cuando el usuario inicia una descarga en segundo plano, las partes del archivo se transfieren al equipo del usuario cuando la hora del procesador está disponible. Es posible pausar y reanudar una descarga en segundo plano. Si el usuario decide cerrar Reproductor de Windows Media antes de que finalice la descarga en segundo plano, se guarda la condición de los archivos incompletos y la descarga puede continuar en segundo plano, incluso después de reiniciar el equipo.

La descarga en segundo plano puede tardar más que la descarga en tiempo real porque el proceso de descarga solo se produce cuando el procesador no realiza otras tareas.

La descarga en segundo plano solo está disponible cuando se usa Windows XP.

## <a name="about-library-integration"></a>Acerca de la integración de bibliotecas

Reproductor de Windows Media organizar automáticamente el contenido de la tienda en línea en la biblioteca. Para habilitarlo, debe especificar un valor para el atributo **WM/ContentDistributor** para cada archivo multimedia digital. Cuando se agrega un archivo multimedia digital a la biblioteca, lo que se produce automáticamente cuando se usa el Administrador de descarga, el archivo se muestra automáticamente en el nodo **Purchased Música** or **Purchased Videos** (Vídeos comprados o comprados). Por ejemplo, si el valor de **WM/ContentDistributor** es "Proseware" y el archivo multimedia digital contiene música, el contenido aparecerá en la biblioteca en la siguiente ubicación:

Todas Música compradas o Música/Proseware

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administrador de descarga**](download-manager.md)
</dt> <dt>

[**DownloadCollection.startDownload**](downloadcollection-startdownload.md)
</dt> </dl>

 

 




