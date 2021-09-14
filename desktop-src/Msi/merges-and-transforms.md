---
description: El Windows mantiene toda la información sobre la instalación en una base de datos relacional. Puede modificar esta base de datos y, por tanto, la instalación, mediante transformaciones y mezclas.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Mezclas y transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261292"
---
# <a name="merges-and-transforms"></a>Mezclas y transformaciones

El Windows mantiene toda la información sobre la instalación en una base de datos relacional. Puede modificar esta base de datos y, por tanto, la instalación, mediante transformaciones y mezclas.

## <a name="transforms"></a>Transformaciones

Una [transformación de base de](database-transforms.md) datos agrega o reemplaza elementos de la base de datos original. Por ejemplo, una transformación puede cambiar todo el texto de la interfaz de usuario de una aplicación de francés a inglés.

Entre los usos principales de las transformaciones se incluyen:

-   Personalización de paquetes de instalación base para determinados grupos de usuarios.

    Las transformaciones se pueden usar para encapsular las distintas personalizaciones de un único paquete base que requieren distintos grupos de usuarios. Por ejemplo, esto es útil en organizaciones en las que los departamentos de soporte técnico de finanzas y personal requieren instalaciones diferentes de un producto determinado. El paquete base de un producto puede estar disponible para todos los usuarios en un punto de instalación administrativa con las personalizaciones adecuadas distribuidas a cada grupo de usuarios por separado.

-   Sincronización de aplicaciones entre lenguajes.

    Las transformaciones son útiles para mantener los paquetes escritos en ubicaciones separadas ampliamente sincronizadas durante la creación. Por ejemplo, si primero se desarrolla una actualización para una versión en inglés de una aplicación que existe en inglés y francés, se puede aplicar una transformación a la versión actualizada en inglés que la convierte en una versión actualizada en francés.

    Se pueden aplicar varias transformaciones a un paquete base y, a continuación, aplicarse sobre la marcha durante la instalación. Esto amplía las funcionalidades del instalador para crear paquetes personalizados y proporciona un mecanismo para asignar de forma eficaz las instalaciones más adecuadas a distintos grupos de usuarios.

-   Aplicación de revisiones a aplicaciones.

    Las transformaciones se pueden usar para aplicar una corrección secundaria a una aplicación que no garantiza una actualización principal. Para obtener más información sobre las revisiones, vea [Paquetes de revisión.](patch-packages.md)

## <a name="merges"></a>Combinaciones

Una combinación combina dos bases de datos en una base de datos y agrega información, en lugar de reemplazarla. Si existe la misma información en ambas bases de datos, se produce un conflicto de combinación. Las mezclas son útiles para los equipos de desarrollo porque permiten dividir una aplicación de gran tamaño en partes que se pueden volver a combinar más adelante. Por ejemplo, los elementos de base de datos para la instalación de un nuevo componente se pueden desarrollar por separado y combinarse posteriormente en la base de datos de instalación principal. Para obtener más información, vea [Módulos de mezcla](merge-modules.md).

Un equipo de desarrollo podría aplicar una operación de combinación de la siguiente manera:

1.  Separe en grupos y trabaje simultáneamente en distintos componentes de una aplicación grande.
2.  A continuación, cada grupo de desarrollo rellena una base de datos con información de instalación para su propio componente, sin preocuparse por los demás componentes de la aplicación.
3.  Una vez completado el desarrollo de un componente, la base de datos de ese componente se puede combinar en la base de datos de instalación principal para toda la aplicación.

 

 



