---
title: Interfaces en objetos distribuidos
description: En la computación distribuida, una interfaz es una colección de definiciones y funciones remotas que permite que dos o más programas interoperan entre distintos contextos.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- interfaces MIDL , en objetos distribuidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8661e7e07f08d35151afe8fb256539ed574b0a0162178e3a9e63dc8c43c59ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807142"
---
# <a name="interfaces-in-distributed-objects"></a>Interfaces en objetos distribuidos

En la computación distribuida, una interfaz es una colección de definiciones y funciones remotas que permite que dos o más programas interoperan entre distintos contextos. En una aplicación RPC, una interfaz especifica:

-   Cómo se identifican las aplicaciones cliente y servidor entre sí.
-   Cómo se transmiten los datos entre el cliente y el servidor.
-   Procedimientos remotos a los que puede llamar la aplicación cliente.
-   Tipos de datos para los parámetros y valores devueltos de los procedimientos remotos.

La Lenguaje de definición de interfaz de Microsoft (MIDL) es para implementar interfaces usadas en aplicaciones distribuidas. Con MIDL, una aplicación puede tener una interfaz o muchas. Cada interfaz especifica un contrato distribuido único entre los programas de cliente y servidor. Las aplicaciones basadas en llamadas a procedimientos remotos (RPC), El modelo de objetos componentes (COM) y el Modelo de objetos componentes distribuidos (DCOM) especifican sus interfaces mediante MIDL.

MIDL se parece a C y C++ de muchas maneras. Para obtener información general sobre cómo escribir interfaces MIDL, vea [Desarrollo de la interfaz](/windows/desktop/Rpc/developing-the-interface).

 

 