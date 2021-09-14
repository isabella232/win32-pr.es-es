---
description: Windows El instalador puede configurar la instalación de software mediante los valores de variables definidas en un paquete de instalación o por el usuario.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Acerca de las propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159264"
---
# <a name="about-properties"></a>Acerca de las propiedades

Windows El instalador puede configurar la instalación de software mediante los valores de variables definidas en un paquete de instalación o por el usuario.

Windows El instalador usa tres categorías de variables globales durante una instalación:

-   Propiedades privadas: el instalador usa propiedades privadas internamente y sus valores deben crearse en la base de datos de instalación o establecerse en valores determinados por el entorno operativo.
-   Propiedades públicas: las propiedades públicas se pueden crear en la base de datos y pueden ser modificadas por un usuario o un administrador del sistema en la línea de comandos, mediante la aplicación de una transformación o mediante la interacción con una interfaz de usuario de creación.
-   Propiedades públicas restringidas: por motivos de seguridad, el autor de un paquete de instalación puede restringir las propiedades públicas que un usuario puede cambiar.

No todas las propiedades deben definirse en todos los paquetes, hay un pequeño conjunto de propiedades necesarias que se deben definir en cada paquete. El instalador establece los valores de las propiedades en un orden de precedencia determinado.

[Propiedades privadas](private-properties.md)

[Propiedades públicas](public-properties.md)

[Propiedades públicas restringidas](restricted-public-properties.md)

[Propiedades necesarias](required-properties.md)

[Orden de prioridad de propiedad](order-of-property-precedence.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Utilizar propiedades](using-properties.md)
</dt> <dt>

[Referencia de propiedad](property-reference.md)
</dt> </dl>

 

 



