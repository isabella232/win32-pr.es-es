---
description: Descripción de los conflictos entre gestos de aplicación y caracteres y símbolos.
ms.assetid: c9b8c284-7c31-4fb0-8cc4-ff09c9c4f228
title: Conflictos entre gestos de aplicación y caracteres y símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5819bfd7013bc39ecb622b09a1ae42816bb969ec63bf062d19597575bb958279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009025"
---
# <a name="conflicts-between-application-gestures-and-characters-and-symbols"></a>Conflictos entre gestos de aplicación y caracteres y símbolos

Algunos gestos de aplicación pueden estar en conflicto con caracteres, combinaciones de caracteres, símbolos, combinaciones de caracteres y símbolos o palabras enteras escritas en un solo trazo. La mayoría de estos conflictos se evitan si se tiene una comprensión detallada del contexto en el que se realiza el gesto de la aplicación.

Por ejemplo, para distinguir un gesto derecho de un guión (-) o un carácter de subrayado ( ), una aplicación puede filtrar por la proximidad del gesto a los caracteres vecinos, el tamaño relativo en comparación con los caracteres u otra información contenida en un \_ paquete. El tiempo del gesto de la aplicación también puede ser un factor determinante a la hora de decidir entre gestos y caracteres. Puede haber más pausa antes de aplicar un gesto de aplicación que antes de introducir caracteres. A menos que un usuario realice una serie de gestos de deshacer o retroceso, también puede haber más pausa después de un gesto que un carácter.

En los temas siguientes se detallan estos conflictos:

-   [Conflictos con símbolos y caracteres latinos](conflicts-with-latin-characters-and-symbols.md)
-   [Conflictos con East-Asian caracteres](conflicts-with-east-asian-characters.md)

 

 



