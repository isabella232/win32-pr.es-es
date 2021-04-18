---
title: Cargar el carácter predeterminado
description: Cargar el carácter predeterminado
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 387715b5078c4ec875c9abce47039898e4998cf7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704643"
---
# <a name="loading-the-default-character"></a>Cargar el carácter predeterminado

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

En lugar de cargar solo un carácter específico directamente especificando su nombre de archivo, puede cargar el *carácter predeterminado*. El carácter predeterminado es un servicio diseñado para proporcionar un asistente de Windows central y compartido que el usuario elige. Microsoft Agent incluye una hoja de propiedades como parte del servicio de caracteres predeterminado, conocido como el ventana Propiedades de caracteres, que permite al usuario cambiar su selección del carácter predeterminado.

La selección del carácter predeterminado está limitada a un carácter que admite el conjunto de animaciones estándar, lo que garantiza un nivel básico de coherencia entre los caracteres. Esto no evita que un carácter tenga animaciones adicionales.

Sin embargo, dado que el carácter predeterminado está pensado para uso general y puede ser compartido por otras aplicaciones al mismo tiempo, Evite cargar el carácter predeterminado cuando desee un carácter exclusivamente para la aplicación.

Para cargar el carácter predeterminado, llame al método [**Load**](load-method.md) sin especificar un nombre de archivo o una ruta de acceso. El agente de Microsoft carga automáticamente el juego de caracteres actual como carácter predeterminado. Si el usuario aún no ha seleccionado un carácter predeterminado, el agente seleccionará el primer carácter que admita el conjunto de animaciones estándar. Si no hay ninguno disponible, se producirá un error en el método y se notificará la causa.

Aunque una aplicación cliente puede consultar la identidad del carácter, solo un usuario puede cambiar su configuración. Puede usar [**ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) para mostrar el carácter ventana Propiedades.

El servidor notificará a los clientes que han cargado el carácter predeterminado cuando un usuario cambia la selección de caracteres y pasan el GUID del carácter nuevo. El servidor descarga automáticamente el carácter anterior y recarga el carácter nuevo. Las colas de los clientes que han cargado el carácter predeterminado se detienen y se vacían. Sin embargo, las colas de clientes que han cargado explícitamente el carácter utilizando el nombre de archivo del carácter no se ven afectadas. Si es necesario, el servidor también controla automáticamente el restablecimiento del motor de texto a voz (TTS) para el nuevo carácter.

 

 




