---
title: Comprobaciones de kernel para controladores no firmados por WHQL
description: En el caso de los dispositivos que limpian Windows 10 y donde el arranque seguro está activado (tenga en cuenta que esto es estándar para todos los dispositivos nuevos desde el lanzamiento de Windows 8,0), todos los controladores nuevos deben estar firmados por WHQL/Sysdev en lugar de simplemente usar certificados con firma cruzada.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418985"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a>Comprobaciones de kernel para controladores no firmados por WHQL

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

En el caso de los dispositivos que limpian Windows 10 y donde el arranque seguro está activado (tenga en cuenta que esto es estándar para todos los dispositivos nuevos desde el lanzamiento de Windows 8,0), todos los controladores nuevos deben estar firmados por WHQL/Sysdev en lugar de simplemente usar certificados con firma cruzada. Los dispositivos que se actualizan y los casos en los que los controladores se han firmado con un certificado cruzado antes de que esta directiva entrara en vigor se excluyen de esta directiva para garantizar la compatibilidad con versiones anteriores. Esta Directiva se anunció el 2015 de abril, pero se aplicará con la edición de aniversario de Windows, publicada en agosto de 2016.

En los casos en los que un controlador no está firmado correctamente, se emitirá como una notificación de PCA de que los controladores se bloquean cuando no supera los requisitos de firma. Esto evita que una experiencia de usuario desconectada posterior del controlador se bloquee en el kernel de forma transparente.

Para obtener más información, consulte [esta entrada de blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), que anuncia el cambio de firma del controlador.

 

 




