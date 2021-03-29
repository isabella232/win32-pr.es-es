---
description: Los proveedores de componentes compartidos deben considerar la posibilidad de que su componente esté disponible como un ensamblado en paralelo si se cumplen uno o varios de los casos siguientes.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: ¿Debe proporcionar un componente compartido como ensamblado simultáneo?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733adf400ba9ce019d9f749fcd79a1a71380c9e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912501"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a>¿Debe proporcionar un componente compartido como ensamblado simultáneo?

Los proveedores de componentes compartidos deben considerar la posibilidad de que su componente esté disponible como un ensamblado en paralelo si se cumplen una o varias de las siguientes condiciones:

-   El componente expone una interfaz de programación de aplicaciones enriquecida que usan muchas aplicaciones. Por ejemplo, un componente como MSHTML, que permite a las aplicaciones de C y C++ tener acceso al modelo de objetos de HTML dinámico (DHTML).
-   El componente ya está siendo compartido por varias aplicaciones. Por ejemplo, un componente como COMCTL32, que proporciona a las aplicaciones acceso a los controles comunes.
-   El componente es un componente nuevo.
-   El componente es un componente de modo de usuario y no un controlador de dispositivo.

No todos los componentes son un candidato adecuado para un ensamblado en paralelo. Un componente no es un candidato adecuado para un ensamblado en paralelo si se cumple alguna de las siguientes condiciones:

-   El componente controla la comunicación entre las aplicaciones. Por ejemplo, partes de OLE32 no crearía un buen ensamblado en paralelo porque no deseaba tener dos versiones diferentes de las partes que coordinan la comunicación entre las aplicaciones que se ejecutan en el sistema.
-   El componente administra un dispositivo físico o virtual para el sistema. Por ejemplo, un controlador de dispositivo para un administrador de trabajos de impresión.

En algunos casos, es posible que el desarrollador del componente rediseñe un componente existente para que sea adecuado para la publicación como un ensamblado en paralelo. Para obtener más información, consulte [instrucciones para crear ensamblados en paralelo](guidelines-for-creating-side-by-side-assemblies.md).

 

 



