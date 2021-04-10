---
title: Establecimiento de la tienda en línea inicial
description: Establecimiento de la tienda en línea inicial
ms.assetid: 86d98936-8f20-4395-be5f-37800162aa89
keywords:
- Windows Media Player tiendas en línea, configurar las tiendas en línea iniciales
- tiendas en línea, configurar las tiendas en línea iniciales
- Escriba 1 tiendas en línea, estableciendo las tiendas en línea iniciales
- Escriba 2 tiendas en línea y establezca las tiendas en línea iniciales
- Windows Media Player tiendas en línea, visualización de la primera tienda en línea
- tiendas en línea, primera tienda en línea visualizada
- tipo 1 tiendas en línea, vista primera tienda en línea
- tipo 2 tiendas en línea, vista primera tienda en línea
- primera tienda en línea visualizada
- establecimiento de las tiendas en línea iniciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fff7dc9b2df43f4b18c257b9b9c36998cbc1334
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903698"
---
# <a name="setting-the-initial-online-store"></a>Establecimiento de la tienda en línea inicial

Para obtener más información acerca de cómo redistribuir el software de Windows Media Player con su aplicación, consulte [redistribuir el software de windows media Player](redistributing-windows-media-player-software.md).

Cuando un usuario instala primero Windows Media Player, la aplicación de instalación establece la tienda en línea activa inicial en un valor predeterminado elegido por Microsoft. Los fabricantes de equipos originales (OEM) de equipos personales pueden optar por cambiar esta configuración.

Para especificar y configurar la primera tienda en línea que el usuario ve cuando instala Windows Media Player, debe:

-   Cree un documento ServiceInfo que instale en el disco duro del usuario. Este documento contiene información acerca de cómo configurar la tienda en línea activa inicial.
-   Anexe un conjunto de parámetros de línea de comandos al ejecutar la aplicación de instalación.

Existen tres escenarios para instalar Windows Media Player y establecer la tienda en línea inicial. En las secciones siguientes se proporcionan más detalles sobre cada escenario:

-   [Instalación sin conexión](installing-while-offline.md)
-   [Instalación desde un CD mientras está en línea](installing-from-a-cd-while-online.md)
-   [Instalación desde la web en línea](installing-from-the-web-while-online.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> <dt>

[**Parámetros de la línea de comandos del programa de instalación para tiendas en línea**](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




