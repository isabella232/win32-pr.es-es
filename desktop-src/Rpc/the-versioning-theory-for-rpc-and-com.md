---
title: Teoría de versiones para RPC y COM
description: Teoría del control de versiones para llamada a procedimiento remoto (RPC) y COM.
ms.assetid: c4df0a7b-e1be-481d-9149-317ffc9179b9
keywords:
- Llamada a procedimiento remoto RPC, procedimientos recomendados, control de versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3681ce1290b7653c28b12c09c93d21de3052e0e6137ed5c6f906afd42f8d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016385"
---
# <a name="the-versioning-theory-for-rpc-and-com"></a>Teoría de versiones para RPC y COM

Solo dos métodos completamente infalibles admiten nuevas funcionalidades sin riesgo de problemas de compatibilidad de conexión:

-   Cambie la versión de la interfaz según las reglas; Esto evita que los clientes nuevos se comuniquen con un servidor antiguo y puede o no impedir que un cliente antiguo se comunique con el nuevo servidor. Esto se aclara más adelante en esta sección.
-   Presenta una interfaz diferente que se ocupa de la nueva funcionalidad.

Una interfaz RPC estándar se identifica mediante una combinación de GUID y número de versión; Una interfaz COM se identifica mediante su GUID. La versión consta de partes principales y secundarias. Para las interfaces estándar con el mismo GUID y números de versión diferentes, solo es posible una conexión cuando la versión principal es la misma y el cliente no es superior a la versión secundaria del servidor.

Una consecuencia es que cambiar el GUID de la interfaz RPC interrumpe la compatibilidad de la conexión, mientras que cambiar el nombre de la interfaz no lo hace.

En RPC estándar, una ruta de acceso para actualizaciones y extensiones está bien definida y básicamente requiere que los nuevos métodos solo se agregan al final de la interfaz y que los nuevos tipos solo se usen en los nuevos métodos. Si se necesitan estas adiciones, se debe aumentar la versión secundaria. Cualquier otro cambio requiere un cambio en la versión principal, ya que el software de cliente y servidor sería incompatible en la conexión. La adhesión a estas reglas garantiza siempre que haya una conexión entre un nuevo cliente y un servidor antiguo, o viceversa, ambos lados son totalmente compatibles.

Para una interfaz COM, no se puede usar el atributo de versión. Crear nuevas interfaces y heredar de las interfaces antiguas es equivalente a manipular la versión en RPC. Normalmente, el mejor enfoque de COM es crear una nueva interfaz para la funcionalidad expandida. Un equivalente de la versión secundaria es la nueva interfaz que hereda de la anterior. Cambiar los métodos antiguos o los tipos de datos antiguos requiere una interfaz COM completamente nueva, una interfaz que no hereda de la anterior.

Para COM, la [**función QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) es un método establecido para comprobar si un servidor admite una interfaz; Por lo tanto, las situaciones en las que un cliente puede hablar con una versión antigua o nueva de una interfaz se pueden resolver fácilmente.

 

 