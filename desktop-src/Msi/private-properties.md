---
description: El instalador usa internamente las propiedades privadas y los valores deben ser especificados en la base de datos por el autor del paquete de instalación o por el instalador durante la instalación en los valores determinados por el entorno operativo.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Propiedades privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652887"
---
# <a name="private-properties"></a>Propiedades privadas

El instalador usa internamente las propiedades privadas y los valores deben ser especificados en la base de datos por el autor del paquete de instalación o por el instalador durante la instalación en los valores determinados por el entorno operativo. La única forma en que un usuario puede interactuar con las propiedades privadas es a través de los [eventos de control](control-events.md) en la interfaz de usuario creada del paquete. Los nombres de propiedad privados deben incluir minúsculas. Vea [restricciones en los nombres de propiedad](restrictions-on-property-names.md).

Las propiedades privadas normalmente describen el entorno operativo. Por ejemplo, si la instalación se ejecuta en una plataforma Windows, el instalador establece la propiedad [**WindowsFolder**](windowsfolder.md) en el valor especificado en la tabla de propiedades.

Los valores de propiedad privados no se pueden invalidar en una línea de comandos. Para borrar una propiedad privada de una instalación, déjela fuera de la [tabla de propiedades](property-table.md). En Windows XP y Windows 2000 no se puede establecer una propiedad privada en la fase de la interfaz de usuario de la instalación y, a continuación, pasar el valor a la fase de ejecución.

Para obtener una lista de todas las propiedades privadas estándar que usa el instalador, consulte [referencia de propiedades](property-reference.md). Puede definir una propiedad privada personalizada especificando el nombre y el valor inicial de la propiedad en la tabla de propiedades. Los nombres de propiedad privados siempre deben incluir minúsculas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades públicas](public-properties.md)
</dt> </dl>

 

 



