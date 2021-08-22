---
description: Los proveedores de componentes compartidos deben considerar la posibilidad de que su componente esté disponible como un ensamblado en paralelo si se cumple uno o varios de los casos siguientes.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: ¿Debe proporcionar un componente compartido como ensamblado en paralelo?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92dbd205db37c769050614c60ce4cc3637b27be9108f25b3c1c8f553851df82d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141898"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a>¿Debe proporcionar un componente compartido como ensamblado en paralelo?

Los proveedores de componentes compartidos deben considerar la posibilidad de que su componente esté disponible como un ensamblado en paralelo si se cumple una o varias de las siguientes condiciones:

-   El componente expone una interfaz de programación de aplicaciones enriquecida que usan muchas aplicaciones. Por ejemplo, un componente como MSHTML, que permite que las aplicaciones de C y C++ accedan al modelo de objetos HTML dinámico (DHTML).
-   El componente ya lo comparten varias aplicaciones. Por ejemplo, un componente como COMCTL32, que proporciona a las aplicaciones acceso a los controles comunes.
-   El componente es un nuevo componente.
-   El componente es un componente en modo de usuario y no un controlador de dispositivo.

No todos los componentes son candidatos adecuados para un ensamblado en paralelo. Un componente no es un candidato adecuado para un ensamblado en paralelo si se cumple alguna de las siguientes condiciones:

-   El componente controla la comunicación entre las aplicaciones. Por ejemplo, las partes de OLE32 no crearían un buen ensamblado en paralelo porque no desearía tener dos versiones diferentes de las partes que coordinan la comunicación entre las aplicaciones que se ejecutan en el sistema.
-   El componente administra un dispositivo físico o virtual para el sistema. Por ejemplo, un controlador de dispositivo para un administrador de trabajos de impresión.

En algunos casos, es posible que el desarrollador del componente rediseñar un componente existente para que sea adecuado para su publicación como un ensamblado en paralelo. Para obtener más información, vea Directrices para [crear ensamblados en paralelo.](guidelines-for-creating-side-by-side-assemblies.md)

 

 



