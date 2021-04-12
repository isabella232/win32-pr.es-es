---
title: Interfaces en objetos distribuidos
description: En el computación distribuida, una interfaz es una colección de definiciones y funciones remotas que permite que dos o más programas interoperen entre distintos contextos.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- interfaces MIDL, en objetos distribuidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cbee13dcbab9ccaa6ef6ad3ad3880daa9b14ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358926"
---
# <a name="interfaces-in-distributed-objects"></a>Interfaces en objetos distribuidos

En el computación distribuida, una interfaz es una colección de definiciones y funciones remotas que permite que dos o más programas interoperen entre distintos contextos. En una aplicación RPC, una interfaz especifica:

-   Cómo se identifican entre sí las aplicaciones cliente y servidor.
-   Cómo se transmiten los datos entre el cliente y el servidor.
-   Procedimientos remotos a los que puede llamar la aplicación cliente.
-   Tipos de datos para los parámetros y valores devueltos de los procedimientos remotos.

El Lenguaje de definición de interfaz de Microsoft (MIDL) es para implementar interfaces utilizadas en aplicaciones distribuidas. Con MIDL, una aplicación puede tener una interfaz o varias. Cada interfaz especifica un contrato distribuido único entre los programas de cliente y servidor. Las aplicaciones basadas en llamadas a procedimiento remoto (RPC), el modelo de objetos componentes (COM) y el modelo de objetos componentes distribuido (DCOM) especifican sus interfaces mediante MIDL.

MIDL es similar a C y C++ en muchos sentidos. Para obtener información general sobre la escritura de interfaces MIDL, vea [desarrollar la interfaz](/windows/desktop/Rpc/developing-the-interface).

 

 