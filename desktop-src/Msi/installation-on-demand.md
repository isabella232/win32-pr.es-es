---
description: Con la tecnología de instalación tradicional, es necesario salir de una aplicación y volver a ejecutar el programa de instalación para realizar una tarea de instalación.
ms.assetid: 94c3d5a8-a560-4a1d-b40e-7ebc92d659f3
title: Instalación a petición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f25c83135a0497d09aa0a7800a1272105d0db1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171777"
---
# <a name="installation-on-demand"></a>Instalación a petición

Con la tecnología de instalación tradicional, es necesario salir de una aplicación y volver a ejecutar el programa de instalación para realizar una tarea de instalación. Esto se produjo normalmente cuando un usuario quería que no se eligese una característica o un producto durante la primera ejecución de la instalación. Esto a menudo hacía que el proceso de configuración del producto fuera ineficaz porque requería que el usuario anticipase a la funcionalidad necesaria antes de usar el producto.

La instalación a petición permite ofrecer funcionalidad a usuarios y aplicaciones en ausencia de los propios archivos. Esta noción se conoce como anuncio. El Windows de aplicaciones tiene la capacidad de anunciar funcionalidades y hacer posible la instalación a petición de características de la aplicación o productos completos. Cuando un usuario o aplicación activa una característica o un producto anunciados, el instalador continúa con la instalación de los componentes necesarios. Esto reduce el proceso de configuración porque se puede acceder a funcionalidades adicionales sin tener que salir y volver a ejecutar otro procedimiento de instalación.

Cuando un producto usa el instalador, un usuario puede elegir en el momento de la instalación qué características o aplicaciones instalar y cuáles anunciar. A continuación, si mientras ejecuta una aplicación, el usuario solicita una característica anunciada que aún no se ha instalado, la aplicación llama al instalador para realizar una instalación de nivel de característica Just-In-Time de los archivos necesarios. Si el usuario activa un producto anunciado que aún no se ha instalado, el sistema operativo llama al instalador para aplicar una instalación de nivel de producto Just-In-Time.

[Los](advertisement.md) anuncios y la instalación a petición también pueden facilitar la administración del sistema al permitir a los administradores designar aplicaciones como necesarias u opcionales para distintos grupos de usuarios. Hay dos tipos de publicidad conocidas como "asignación" y "publicación". Si un administrador asigna una aplicación a un grupo, estos usuarios pueden instalar la aplicación a petición. Sin embargo, si el administrador publica la aplicación en el grupo, no aparecen puntos de entrada para estos usuarios y la instalación a petición solo se activa si otra aplicación activa la aplicación publicada.

 

 



