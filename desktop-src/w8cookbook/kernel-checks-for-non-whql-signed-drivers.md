---
title: Comprobaciones de kernel para controladores no firmados por WHQL
description: En el caso de los dispositivos que instalan Windows 10 limpiamente y donde el arranque seguro está en (tenga en cuenta que esto es estándar para todos los dispositivos nuevos desde el lanzamiento de Windows 8.0), todos los controladores nuevos deben estar firmados por WHQL/Sysdev en lugar de usar simplemente certificados firmados cruzadamente.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362834"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a>Comprobaciones de kernel para controladores no firmados por WHQL

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

En el caso de los dispositivos que instalan Windows 10 limpiamente y donde el arranque seguro está en (tenga en cuenta que esto es estándar para todos los dispositivos nuevos desde el lanzamiento de Windows 8.0), todos los controladores nuevos deben estar firmados por WHQL/Sysdev en lugar de usar simplemente certificados firmados cruzadamente. Los dispositivos que se actualizan y los casos en los que los controladores se han firmado con un certificado cruzado antes de que esta directiva entrara en vigor se excluyen de esta directiva para garantizar la compatibilidad con versiones anteriores. Esta directiva se anunció en abril de 2015, pero se aplicará con la edición de aniversario de Windows, publicada en agosto de 2016.

En los casos en los que un controlador no está firmado correctamente, se manifesta como una notificación de PCA que los controladores se bloquean cuando no supera los requisitos de firma. Esto evita que una experiencia de usuario desconectada posteriormente del controlador se bloquee en el kernel de forma transparente.

Para obtener más información, consulte esta [entrada de blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), que anuncia el cambio de firma del controlador.

 

 




