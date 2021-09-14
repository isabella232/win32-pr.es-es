---
description: El instalador Windows reduce el costo total de propiedad (TCO) de las aplicaciones al aumentar la capacidad de los clientes de administrar y mantener los componentes de la aplicación durante la instalación y el tiempo de ejecución.
ms.assetid: fbb139e3-c81b-44fc-9e92-bada0be02862
title: Administración de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeff6c25556879429330170ec8190b1296576517
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158841"
---
# <a name="component-management"></a>Administración de componentes

El instalador Windows reduce el costo total de propiedad (TCO) de las aplicaciones al aumentar la capacidad de los clientes de administrar y mantener los componentes de la aplicación durante la instalación y el tiempo de ejecución. La base de datos de instalación realiza un seguimiento de qué aplicaciones requieren un componente determinado, qué archivos componen cada componente, dónde se instala cada archivo en el sistema y dónde se encuentran los orígenes de componentes. Esto permite a los desarrolladores crear paquetes que proporcionan las siguientes ventajas:

-   Mayor resistencia de las aplicaciones. Use el instalador para detectar y reinstalar los componentes dañados sin tener que volver a ejecutar el programa de instalación. El instalador comprueba la ruta de acceso de un componente en tiempo de ejecución. Esto libera a las aplicaciones de la dependencia de las rutas de acceso de archivos estáticos que normalmente difieren entre equipos y pueden apuntar a componentes que faltan. Para obtener más información, vea [Resistencia.](resiliency.md)
-   Instalación a petición. Este conjunto de características no se instala durante la instalación, pero se especifica en la base de datos que se instalará Just-In-Time para su uso si la aplicación lo requiere en el futuro. Los usuarios no necesitan volver a ejecutar la instalación. Para obtener más información, [vea Instalación a petición.](installation-on-demand.md)
-   Anuncio de accesos directos a características, aplicaciones o productos completos en la interfaz de usuario. Los usuarios pueden instalar estos métodos a petición mediante los accesos directos. Los usuarios también pueden quitar características, aplicaciones o productos completos a petición. Para obtener más información, vea [Anuncio](advertisement.md).
-   Personalización de la instalación. Un administrador puede aplicar transformaciones a la base de datos que adapten la instalación a un grupo determinado de usuarios. Para obtener más información, vea [Personalización](customization.md).
-   Implementación más sencilla de actualizaciones de aplicaciones. Use el instalador para actualizar los productos. Para obtener más información, vea [Aplicación de revisiones y actualizaciones.](patching-and-upgrades.md)
-   Pantalla de acceso directo de características. El instalador muestra accesos directos a características que se ejecutan localmente con accesos directos a características que se ejecutan de forma remota. Dado que la base de datos de instalación especifica el contexto de ejecución de cada característica, los usuarios pueden presentar puntos de entrada visiblemente equivalentes según sea necesario.
-   Mantenga las métricas de uso en las características. Los desarrolladores pueden proporcionar un paquete de instalación que mantiene el recuento de uso de una característica por parte de todas las aplicaciones cliente y quita los componentes que no se usan.
-   Incorporar instalaciones. Los desarrolladores pueden incorporar las funcionalidades de administración de componentes del instalador en sus aplicaciones mediante la creación de un paquete de instalación y el uso de las funciones del instalador [en](installer-functions.md) su código de aplicación. En la ilustración siguiente se muestra una aplicación que solicita la instalación de una característica.

    ![aplicación que solicita la instalación de características. ](images/over1.png)

 

 



