---
description: Actualmente, las credenciales de nombre de usuario y contraseña son las credenciales más comunes que se usan para la autenticación.
ms.assetid: 1d810f71-9bf5-4c5c-a573-c35081f604cf
title: Control de contraseñas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99aaf133d23390a6f4efce97940c5116fddf91b45776dfd6847b2712b15b74ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035475"
---
# <a name="handling-passwords"></a>Control de contraseñas

Actualmente, las credenciales de nombre de usuario y contraseña son las credenciales más comunes que se usan para la autenticación. Aunque otros tipos de credenciales, como certificados y biométricas, empiezan a encontrarse en el mundo de los sistemas y las redes, a menudo se les hace una copia de seguridad mediante contraseñas. Y, incluso cuando se usan certificados, sus claves de cifrado deben estar protegidas. Por lo tanto, los nombres de usuario y las contraseñas se seguirán usando para las credenciales en un futuro próximo.

Dado que las contraseñas y las claves de cifrado van a estar en torno a un tiempo, es importante que los sistemas de software las usen de forma segura. Si un sistema de red o equipo va a permanecer seguro, las contraseñas deben protegerse de los falsos intrusos. Esto podría parecer, al principio, trivial. Sin embargo, el sistema después del sistema y la red después de la red se han puesto en peligro porque un atacante ha podido averiguar las contraseñas de los usuarios. Los problemas van desde los usuarios que comparten sus contraseñas con alguien hasta el software que puede ser penetrado por un atacante.

Es imposible almacenar información secreta en software de forma completamente segura. Y dado que el almacenamiento de contraseñas y claves de cifrado en un sistema de software nunca puede ser completamente seguro, se recomienda que no se almacenen en un sistema de software.

Sin embargo, cuando las contraseñas deben almacenarse en un sistema de software, que suele ser el caso, se pueden tomar precauciones. La principal precaución es que sea lo más difícil posible que un intrusista detecte una contraseña. Al igual que bloquear las puertas de la casa, si alguien está determinado a interrumpir, es casi imposible impedir que lo haga. Pero, con suerte, habrá elevado el nivel de dificultad lo suficiente como para que el falso intrusista prefiere encontrar unas precarga más fáciles.

Hay muchas maneras de dificultar el trabajo de un atacante de detectar contraseñas. Sin embargo, la medida de lo que realmente se puede hacer suele ser un intercambio con lo que los usuarios de la red o el sistema están dispuestos a convivir. Por ejemplo, tome el caso en el que no se usa el "inicio de sesión único" y se solicita al usuario una contraseña cada vez que se inicia una aplicación. En la mayoría de los casos, esto crearía una carga significativa para los usuarios y probablemente se quejan. No solo eso, sino que la falta de un inicio de sesión único es ineficaz y degradaría la productividad de los usuarios. Por lo tanto, en la práctica, una contraseña generalmente no se recopila de un usuario, excepto en el momento de iniciar sesión.

Dado que las contraseñas normalmente deben almacenarse en el sistema de software, es importante asegurarse de que las contraseñas se mantienen lo más seguras posible y de que se mantiene la comodidad de los usuarios. Para obtener más información, vea los temas siguientes:

-   [Evaluación de amenazas de contraseña](password-threat-assessment.md)
-   [Técnicas de mitigación de amenazas](threat-mitigation-techniques.md)

> [!Note]  
> Cuando haya terminado de usar contraseñas en aplicaciones, borre la información confidencial de la memoria mediante una llamada a la [**función SecureZeroMemory.**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85))

 

 

 
