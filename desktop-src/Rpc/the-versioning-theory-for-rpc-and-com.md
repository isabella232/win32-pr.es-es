---
title: La teoría de control de versiones de RPC y COM
description: Teoría de control de versiones para llamada a procedimiento remoto (RPC) y COM.
ms.assetid: c4df0a7b-e1be-481d-9149-317ffc9179b9
keywords:
- RPC llamada a procedimiento remoto, prácticas recomendadas, control de versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03b23c91bf69fbc3c4f72366b80812fd54330d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149512"
---
# <a name="the-versioning-theory-for-rpc-and-com"></a>La teoría de control de versiones de RPC y COM

Solo dos métodos completamente infalibles admiten nuevas funcionalidades sin riesgo de problemas de compatibilidad de conexión:

-   Cambie la versión de la interfaz de acuerdo con las reglas. Esto impide que los nuevos clientes se comuniquen con un servidor antiguo y puede o no impedir que un cliente anterior se comunique con el nuevo servidor. Esto se aclara más adelante en esta sección.
-   Introduzca una interfaz diferente que trabaje con la nueva funcionalidad.

Una interfaz RPC estándar se identifica mediante una combinación de número de versión y GUID; una interfaz COM se identifica mediante su GUID. La versión consta de las partes principales y secundarias. En el caso de las interfaces estándar con el mismo GUID y distintos números de versión, una conexión solo es posible cuando la versión principal es la misma y el cliente no es más alto que la versión secundaria del servidor.

Una consecuencia es que cambiar el GUID de la interfaz RPC interrumpe la compatibilidad de conexión, mientras que cambiar el nombre de la interfaz no.

En RPC estándar, una ruta de acceso para las actualizaciones y extensiones está bien definida y, básicamente, requiere que los nuevos métodos se agreguen al final de la interfaz, y que los nuevos tipos se usen solo en los nuevos métodos. Si se necesitan estas adiciones, se debe aumentar la versión secundaria. Cualquier otro cambio requiere un cambio en la versión principal, ya que el software de cliente y servidor sería incompatible en la conexión. Al cumplir estas reglas, se asegura siempre que haya una conexión entre un cliente nuevo y un servidor anterior, o viceversa, ambos lados son totalmente compatibles.

En el caso de una interfaz COM, no se puede usar el atributo version. Crear nuevas interfaces y heredar de las interfaces antiguas es equivalente a manipular la versión en RPC. Normalmente, el mejor enfoque en COM es crear una nueva interfaz para la funcionalidad expandida. Un equivalente de la versión secundaria es la nueva interfaz que hereda de la antigua. Cambiar los métodos anteriores o los tipos de datos antiguos requiere una interfaz COM completamente nueva, que es una interfaz que no se hereda de la antigua.

En el caso de COM, la función [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) es un método establecido para comprobar si un servidor admite una interfaz; por lo tanto, las situaciones en las que un cliente puede comunicarse con una versión anterior o una nueva de una interfaz se pueden resolver fácilmente.

 

 