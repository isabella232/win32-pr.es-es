---
description: Actualmente, las credenciales de nombre de usuario y contraseña son las credenciales más comunes que se usan para la autenticación.
ms.assetid: 1d810f71-9bf5-4c5c-a573-c35081f604cf
title: Administrar contraseñas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d3a5ab2bc034500159adb25dab02b47eb43bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669669"
---
# <a name="handling-passwords"></a>Administrar contraseñas

Actualmente, las credenciales de nombre de usuario y contraseña son las credenciales más comunes que se usan para la autenticación. Aunque otros tipos de credenciales, como los certificados y la biometría, están empezando a encontrar su forma en el mundo de los sistemas y las redes, a menudo se realiza una copia de seguridad mediante contraseñas. Y, incluso cuando se usan certificados, se deben proteger sus claves de cifrado. Por lo tanto, los nombres de usuario y las contraseñas se seguirán usando para las credenciales en el futuro previsible.

Dado que las contraseñas y las claves de cifrado van a estar alrededor de un tiempo, es importante que los sistemas de software las usen de manera segura. Si un sistema de red o equipo va a permanecer seguro, las contraseñas deben protegerse de los intrusos. En primer lugar, esto podría parecer trivial. Sin embargo, el sistema después del sistema y de la red después de que se haya puesto en peligro la red porque un atacante ha podido descubrir las contraseñas de los usuarios. Los problemas van desde los usuarios que comparten sus contraseñas con alguien hasta el software que puede penetrar un atacante.

No es posible almacenar información secreta en el software de un modo totalmente seguro. Además, dado que el almacenamiento de contraseñas y claves de cifrado en un sistema de software nunca puede ser totalmente seguro, se recomienda que no se almacenen en un sistema de software.

Sin embargo, cuando las contraseñas deben almacenarse en un sistema de software, que suele ser el caso, se pueden tomar precauciones. La precaución principal es que sea lo más difícil posible para que un intruso detecte una contraseña. Al igual que el bloqueo de las puertas de la casa, si alguien está determinado para que se interrumpa, es casi imposible evitar que lo hagan. Pero afortunadamente, habrá aumentado el nivel de dificultad en la medida en que el atacante debería encontrar más fácilmente.

Hay muchas maneras de hacer que un atacante pueda detectar contraseñas más difíciles. Sin embargo, el alcance de lo que se puede hacer realmente es normalmente un equilibrio con el que los usuarios de la red o del sistema están dispuestos a vivir. Por ejemplo, supongamos que no se usa el "Inicio de sesión único" y se solicita al usuario una contraseña cada vez que se inicia una aplicación. En la mayoría de los casos, esto crearía una carga significativa para los usuarios y probablemente se quejaría. No solo eso, pero la falta de un inicio de sesión único es ineficaz y degradaría la productividad de los usuarios. Por lo tanto, en la práctica, no se recopila una contraseña por lo general de un usuario, excepto en el momento del inicio de sesión.

Dado que las contraseñas se deben almacenar normalmente en el sistema de software, es importante asegurarse de que las contraseñas se mantengan lo más seguras posible y que se mantenga la comodidad de los usuarios. Para obtener más información, vea los temas siguientes:

-   [Evaluación de amenazas de contraseñas](password-threat-assessment.md)
-   [Técnicas de mitigación de amenazas](threat-mitigation-techniques.md)

> [!Note]  
> Cuando haya terminado de usar las contraseñas en las aplicaciones, borre la información confidencial de la memoria mediante una llamada a la función [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .

 

 

 
