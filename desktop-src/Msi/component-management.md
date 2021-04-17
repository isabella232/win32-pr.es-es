---
description: El Windows Installer reduce el costo total de propiedad (TCO) de las aplicaciones, ya que aumenta la capacidad de los clientes de administrar y mantener los componentes de la aplicación durante la instalación y el tiempo de ejecución.
ms.assetid: fbb139e3-c81b-44fc-9e92-bada0be02862
title: Administración de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeff6c25556879429330170ec8190b1296576517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667813"
---
# <a name="component-management"></a>Administración de componentes

El Windows Installer reduce el costo total de propiedad (TCO) de las aplicaciones, ya que aumenta la capacidad de los clientes de administrar y mantener los componentes de la aplicación durante la instalación y el tiempo de ejecución. La base de datos de instalación realiza un seguimiento de las aplicaciones que requieren un componente determinado, los archivos que componen cada componente, donde cada archivo está instalado en el sistema y dónde se encuentran los orígenes de componentes. Esto permite a los desarrolladores crear paquetes que proporcionan las siguientes ventajas:

-   Mayor resistencia de las aplicaciones. Use el instalador para detectar y reinstalar componentes dañados sin tener que volver a ejecutar el programa de instalación. El instalador comprueba la ruta de acceso de un componente en tiempo de ejecución. Esto libera las aplicaciones de dependencia en rutas de acceso de archivo estáticas que suelen diferir entre equipos y pueden indicar que faltan componentes. Para obtener más información, consulte [resistencia](resiliency.md).
-   Instalación a petición. Este conjunto de características no se instala durante la instalación, pero se especifica en la base de datos que se va a instalar Just-in-Time para su uso si lo requiere la aplicación en el futuro. No es necesario que los usuarios vuelvan a ejecutar el programa de instalación. Para obtener más información, consulte [instalación a petición](installation-on-demand.md).
-   Anuncio de accesos directos a características, aplicaciones o productos completos en la interfaz de usuario. Los usuarios pueden instalar estos a petición mediante los métodos abreviados. Los usuarios también pueden quitar características, aplicaciones o productos completos a petición. Para obtener más información, vea el [anuncio](advertisement.md).
-   Personalización de la instalación. Un administrador puede aplicar transformaciones a la base de datos que adapten la instalación de un grupo de usuarios determinado. Para obtener más información, vea [Personalización](customization.md).
-   Implementación más sencilla de las actualizaciones de la aplicación. Use el instalador para actualizar sus productos. Para obtener más información, consulte [revisiones y actualizaciones](patching-and-upgrades.md).
-   Pantalla de acceso directo de características. El instalador muestra accesos directos a las características que se ejecutan localmente con accesos directos a las características que se ejecutan de forma remota. Dado que la base de datos de instalación especifica el contexto de ejecución de cada característica, se pueden presentar puntos de entrada equivalentes de forma visible a los usuarios según sea necesario.
-   Mantenga métricas de uso en las características. Los desarrolladores pueden proporcionar un paquete de instalación que mantenga el recuento de uso de una característica por parte de todas las aplicaciones cliente y quite los componentes que no se estén usando.
-   Incorporar instalaciones. Los desarrolladores pueden incorporar las capacidades de administración de componentes del instalador en sus aplicaciones mediante la creación de un paquete de instalación y el uso de las [funciones del instalador](installer-functions.md) en su código de aplicación. En la ilustración siguiente se muestra una aplicación que solicita la instalación de una característica.

    ![aplicación que solicita la instalación de características. ](images/over1.png)

 

 



