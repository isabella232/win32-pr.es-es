---
description: Descripción de los conflictos entre los movimientos de aplicación y los caracteres y símbolos.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Conflictos entre los gestos y caracteres y símbolos de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92755990235d494cd3e0dc07218de8a1e47d578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714959"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a>Conflictos entre los gestos y caracteres y símbolos de la aplicación

Algunos gestos de la aplicación pueden entrar en conflicto con caracteres, combinaciones de caracteres, símbolos, combinaciones de caracteres y símbolos o palabras completas escritas en un solo trazo. La mayoría de estos conflictos se evitan al tener un conocimiento detallado del contexto en el que se realiza el gesto de la aplicación.

Por ejemplo, para distinguir un gesto correcto de un guión (-) o un carácter de subrayado ( \_ ), una aplicación puede filtrar el cierre de los caracteres contiguos, el tamaño relativo en comparación con los caracteres u otra información contenida en un paquete. El tiempo del gesto de aplicación también puede ser un factor determinante a la hora de decidir entre los gestos y los caracteres. Puede haber más de una pausa antes de aplicar un gesto de aplicación que antes de introducir caracteres. A menos que un usuario realice una serie de movimientos de deshacer o de retroceso, también puede haber más de una pausa después de un movimiento que un carácter.

En los temas siguientes se detallan estos conflictos:

-   [Conflictos con caracteres latinos y símbolos](conflicts-with-latin-characters-and-symbols.md)
-   [Conflictos con caracteres de East-Asian](conflicts-with-east-asian-characters.md)

 

 



