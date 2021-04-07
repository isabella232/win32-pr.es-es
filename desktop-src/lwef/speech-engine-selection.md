---
title: Selección del motor de voz
description: Selección del motor de voz
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903391"
---
# <a name="speech-engine-selection"></a>Selección del motor de voz

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El valor de identificador de idioma de un carácter determina su idioma de entrada de voz predeterminado; El agente de Microsoft solicita a SAPI un motor instalado que coincida con ese idioma. Si una aplicación cliente no especifica una preferencia de idioma, Microsoft Agent intentará encontrar un motor de reconocimiento de voz que coincida con el ID. de idioma predeterminado del usuario (con el identificador de idioma principal y, después, el identificador de idioma secundario). Si no hay ningún motor disponible que coincida con este idioma, la voz se deshabilitará para ese carácter.

También puede solicitar un motor de reconocimiento de voz específico especificando su identificador de modo (mediante la propiedad [**SRModeID**](srmodeid-property.md) de caracteres). Sin embargo, si el identificador de idioma para ese ID. de modo no coincide con la configuración de idioma del cliente, se producirá un error en la llamada (se producirá un error en el control). Después, el motor de reconocimiento de voz seguirá siendo el último que el cliente estableció correctamente el motor, o bien, si no es así, el motor que coincide con el identificador de idioma actual del sistema. Si todavía no hay ninguna coincidencia, la entrada de voz no está disponible para ese cliente.

El agente de Microsoft carga automáticamente un motor de reconocimiento de voz cuando la entrada de voz la inicia un usuario al presionar la tecla de método de escucha o el cliente de entrada-activo llama al método [**Listen**](listen-method.md) . Sin embargo, también se puede cargar un motor cuando se establece o se consulta su identificador de modo, se establece o se consultan las propiedades de la ventana comandos de voz, se consulta [**SRStatus**](srstatus-property.md)o cuando la voz está habilitada y el usuario muestra la página de entrada de voz de las opciones de caracteres avanzadas. Sin embargo, el agente de Microsoft solo mantiene cargados los motores de voz que usan los clientes.

 

 




