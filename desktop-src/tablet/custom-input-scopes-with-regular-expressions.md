---
description: Puede definir ámbitos de entrada personalizados mediante modelos de lenguaje compuestos de expresiones regulares para escribir a mano y asignarlos a campos. Por ejemplo, si va a crear una aplicación de base de datos para elementos de almacenamiento y desea que los usuarios puedan escribir números de pieza mediante el panel de escritura del Panel de entrada de Tablet PC. Si la sintaxis de número de pieza consta de tres letras seguidas de cuatro números seguidos de otra letra (por ejemplo, ABC1234D), el reconocedor de escritura a mano tendría dificultades para reconocer dicha entrada porque no está definido en el modelo de lenguaje. No hay ningún factoid predefinido que se corresponda con esta sintaxis, ni Microsoft puede incluir la sintaxis para cada campo posible que una aplicación pueda necesitar. Las expresiones regulares de escritura a mano proporcionan una manera sencilla para que las aplicaciones definan su propio modelo de lenguaje para un campo de uso especial determinado. Nota Cuando se trabaja en una aplicación habilitada para entrada de lápiz que usa la propiedad Factoid del objeto RecognizerContext, no se pueden usar factoids de la versión 1 en una expresión regular.
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: Ámbitos de entrada personalizados con expresiones regulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2349893e4a4f478924a20877d0dec94d63a8adda8bea17eba8c8f029c63d5077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045882"
---
# <a name="custom-input-scopes-with-regular-expressions"></a>Ámbitos de entrada personalizados con expresiones regulares

Puede definir ámbitos de entrada personalizados mediante modelos de lenguaje compuestos de expresiones regulares para escribir a mano y asignarlos a campos.

Por ejemplo, si va a crear una aplicación de base de datos para elementos de almacenamiento y desea que los usuarios puedan escribir números de pieza mediante el panel de escritura del Panel de entrada de Tablet PC. Si la sintaxis de número de pieza consta de tres letras seguidas de cuatro números seguidos de otra letra (por ejemplo, ABC1234D), el reconocedor de escritura a mano tendría dificultades para reconocer dicha entrada porque no está definido en el modelo de lenguaje. No hay ningún factoid predefinido que se corresponda con esta sintaxis, ni Microsoft puede incluir la sintaxis para cada campo posible que una aplicación pueda necesitar. Las expresiones regulares de escritura a mano proporcionan una manera sencilla para que las aplicaciones definan su propio modelo de lenguaje para un campo de uso especial determinado.

> [!Note]  
> Cuando se trabaja en una aplicación habilitada para entrada de lápiz que usa la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) del objeto [**RecognizerContext,**](inkrecognizercontext-class.md) no se pueden usar factoids de la versión 1 en una expresión regular.

 

 

 



