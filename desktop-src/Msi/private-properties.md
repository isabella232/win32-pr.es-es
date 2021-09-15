---
description: El instalador usa internamente las propiedades privadas y el autor del paquete de instalación debe especificar sus valores en la base de datos o establecerlo el instalador durante la instalación en valores determinados por el entorno operativo.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Propiedades privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473949"
---
# <a name="private-properties"></a>Propiedades privadas

El instalador usa internamente las propiedades privadas y el autor del paquete de instalación debe especificar sus valores en la base de datos o establecerlo el instalador durante la instalación en valores determinados por el entorno operativo. La única manera en que un usuario puede interactuar con propiedades privadas es a través de Eventos de [control](control-events.md) en la interfaz de usuario del paquete que ha sido el autor. Los nombres de propiedad privada deben incluir letras minúsculas. Vea [Restricciones en los nombres de propiedad.](restrictions-on-property-names.md)

Las propiedades privadas normalmente describen el entorno operativo. Por ejemplo, si la instalación se ejecuta en una plataforma Windows, el instalador establece la propiedad [**WindowsFolder**](windowsfolder.md) en el valor especificado en la tabla Property.

Los valores de propiedad privada no se pueden invalidar en una línea de comandos. Para borrar una propiedad privada de una instalación, déjela fuera de la [tabla Property](property-table.md). En Windows XP y Windows 2000 no se puede establecer una propiedad privada en la fase de la interfaz de usuario de la instalación y, a continuación, pasar el valor a la fase de ejecución.

Para obtener una lista de todas las propiedades privadas estándar usadas por el instalador, vea [Referencia de propiedades](property-reference.md). Puede definir una propiedad privada personalizada especificando el nombre y el valor inicial de la propiedad en la tabla Property. Los nombres de propiedad privada siempre deben incluir letras minúsculas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades públicas](public-properties.md)
</dt> </dl>

 

 



