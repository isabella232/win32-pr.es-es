---
title: Establecimiento de la tienda en línea inicial
description: Establecimiento de la tienda en línea inicial
ms.assetid: 86d98936-8f20-4395-be5f-37800162aa89
keywords:
- Reproductor de Windows Media en línea, establecer las tiendas en línea iniciales
- tiendas en línea, establecimiento de tiendas en línea iniciales
- tiendas en línea de tipo 1, establecer las tiendas en línea iniciales
- tiendas en línea de tipo 2, establecer las tiendas en línea iniciales
- Reproductor de Windows Media en línea, primera tienda en línea vista
- tiendas en línea, primera tienda en línea vista
- tiendas en línea de tipo 1, primera tienda en línea vista
- tiendas en línea de tipo 2, primera tienda en línea vista
- primera tienda en línea vista
- establecimiento de tiendas en línea iniciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0af7f5143bc7e4e8e310927621e4b6bf8c6fa557cf91d138424321140c56d62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123145"
---
# <a name="setting-the-initial-online-store"></a>Establecimiento de la tienda en línea inicial

Para más información sobre cómo redistribuir Reproductor de Windows Media software con la aplicación, consulte [Redistribuir Reproductor de Windows Media Software](redistributing-windows-media-player-software.md).

Cuando un usuario instala por primera Reproductor de Windows Media, la aplicación de instalación establece la tienda en línea activa inicial en un valor predeterminado elegido por Microsoft. Los fabricantes de equipos originales (OEM) de equipos personales pueden optar por cambiar esta configuración.

Para especificar y configurar la primera tienda en línea que el usuario ve cuando instala Reproductor de Windows Media, debe:

-   Cree un documento ServiceInfo que instale en el disco duro del usuario. Este documento contiene información sobre cómo configurar el almacén en línea activo inicial.
-   Anexe un conjunto de parámetros de línea de comandos al ejecutar la aplicación de instalación.

Hay tres escenarios para instalar Reproductor de Windows Media y establecer la tienda en línea inicial. En las secciones siguientes se proporcionan más detalles sobre cada escenario:

-   [Instalación mientras está sin conexión](installing-while-offline.md)
-   [Instalación desde un CD en línea](installing-from-a-cd-while-online.md)
-   [Instalación desde la Web mientras está en línea](installing-from-the-web-while-online.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común a los almacenes en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Configuración de parámetros de la línea de comandos para almacenes en línea**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




