---
description: El Windows Installer mantiene toda la información sobre la instalación en una base de datos relacional. Puede modificar esta base de datos y, por lo tanto, la instalación, mediante transformaciones y combinaciones.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Combinaciones y transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653039"
---
# <a name="merges-and-transforms"></a>Combinaciones y transformaciones

El Windows Installer mantiene toda la información sobre la instalación en una base de datos relacional. Puede modificar esta base de datos y, por lo tanto, la instalación, mediante transformaciones y combinaciones.

## <a name="transforms"></a>Transformaciones

Una [transformación de base de datos](database-transforms.md) agrega o reemplaza elementos en la base de datos original. Por ejemplo, una transformación puede cambiar todo el texto de la interfaz de usuario de la aplicación de francés a Inglés.

Los usos principales de las transformaciones incluyen:

-   Personalización de paquetes de instalación base para grupos de usuarios concretos.

    Las transformaciones se pueden usar para encapsular las diferentes personalizaciones de un único paquete base que son necesarias para distintos grupos de usuarios. Por ejemplo, esto es útil en organizaciones en las que los departamentos de soporte técnico y Finanzas requieren diferentes instalaciones de un producto determinado. El paquete base de un producto puede estar disponible para todos los usuarios en un punto de instalación administrativa con las personalizaciones adecuadas distribuidas a cada grupo de usuarios por separado.

-   Sincronización de aplicaciones entre lenguajes.

    Las transformaciones son útiles para mantener los paquetes creados en ubicaciones ampliamente separadas sincronizadas durante la creación. Por ejemplo, si una actualización se desarrolla por primera vez para una versión en Inglés de una aplicación que existe en inglés y francés, se puede aplicar una transformación a la versión en inglés actualizada que la convierte en una versión en francés actualizada.

    Se pueden aplicar varias transformaciones a un paquete base y, a continuación, aplicar sobre la marcha durante la instalación. Esto amplía las capacidades del instalador para crear paquetes personalizados y proporciona un mecanismo para asignar eficazmente las instalaciones más adecuadas a distintos grupos de usuarios.

-   Aplicación de revisiones.

    Las transformaciones se pueden usar para aplicar una corrección menor a una aplicación que no garantiza una actualización principal. Para obtener más información acerca de las revisiones, consulte [paquetes de revisiones](patch-packages.md).

## <a name="merges"></a>Combinaciones

Una combinación combina dos bases de datos en una base de datos y agrega, en lugar de reemplazar, la información. Si existe la misma información en ambas bases de datos, se produce un conflicto de fusión mediante combinación. Las combinaciones son útiles para los equipos de desarrollo porque permiten que una aplicación grande se divida en partes que se pueden recombinar más adelante. Por ejemplo, los elementos de base de datos para la instalación de un componente nuevo se pueden desarrollar por separado y, posteriormente, combinarse en la base de datos de instalación principal. Para obtener más información, vea [módulos de combinación](merge-modules.md).

Un equipo de desarrollo puede aplicar una operación de combinación de la siguiente manera:

1.  Separar en grupos y trabajar simultáneamente en distintos componentes de una aplicación de gran tamaño.
2.  A continuación, cada grupo de desarrollo rellena una base de datos con información de instalación para su propio componente, sin preocuparse por los demás componentes de la aplicación.
3.  Una vez completado el desarrollo de un componente, la base de datos de ese componente se puede combinar en la base de datos de instalación principal de toda la aplicación.

 

 



