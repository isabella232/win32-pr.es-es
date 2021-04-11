---
description: Windows Installer puede configurar la instalación de software mediante los valores de las variables definidas en un paquete de instalación o por el usuario.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Acerca de las propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276540"
---
# <a name="about-properties"></a>Acerca de las propiedades

Windows Installer puede configurar la instalación de software mediante los valores de las variables definidas en un paquete de instalación o por el usuario.

Windows Installer usa tres categorías de variables globales durante una instalación:

-   Propiedades privadas: el instalador usa propiedades privadas internamente y sus valores se deben crear en la base de datos de instalación o establecerse en los valores determinados por el entorno operativo.
-   Propiedades públicas: las propiedades públicas se pueden crear en la base de datos y cambiar por un administrador de usuarios o del sistema en la línea de comandos, mediante la aplicación de una transformación o mediante la interacción con una interfaz de usuario creada.
-   Propiedades públicas restringidas: por motivos de seguridad, el autor de un paquete de instalación puede restringir las propiedades públicas que un usuario puede cambiar.

No todas las propiedades deben definirse en cada paquete, hay un pequeño conjunto de propiedades necesarias que se deben definir en cada paquete. El instalador establece los valores de las propiedades en un orden de prioridad determinado.

[Propiedades privadas](private-properties.md)

[Propiedades públicas](public-properties.md)

[Propiedades públicas restringidas](restricted-public-properties.md)

[Propiedades obligatorias](required-properties.md)

[Orden de prioridad de propiedad](order-of-property-precedence.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Utilizar propiedades](using-properties.md)
</dt> <dt>

[Referencia de propiedades](property-reference.md)
</dt> </dl>

 

 



