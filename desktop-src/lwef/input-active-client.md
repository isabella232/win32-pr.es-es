---
title: Cliente de Input-Active
description: Cliente de Input-Active
ms.assetid: b46e91d3-eca7-4a4a-b1ce-27b5e6ad92a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3223ddc7bb412b333d628f93cc56b27efd0abb7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357416"
---
# <a name="input-active-client"></a>Cliente de Input-Active

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Dado que varias aplicaciones cliente pueden compartir el mismo carácter y que varios clientes pueden usar caracteres diferentes al mismo tiempo, el servidor designa a un cliente como cliente *de entrada-activo* y envía la entrada de mouse y de voz solo a esa aplicación cliente. Esto mantiene la administración ordenada de los datos proporcionados por el usuario para que un cliente adecuado responda a la entrada.

Normalmente, la interacción con el usuario determina qué aplicación cliente pasa a ser de entrada activa. Por ejemplo, si el usuario hace clic en un carácter, la aplicación cliente de ese carácter pasa a ser de entrada activa. Del mismo modo, si un usuario habla el nombre de un carácter, se convierte en una entrada-activa. Además, cuando el servidor procesa el método [**Show**](show-method.md) de un carácter, el cliente de ese carácter pasa a ser de entrada-activo.

Cuando se oculta un carácter, el cliente de ese carácter dejará de ser de entrada-activo para ese carácter. El servidor convierte automáticamente en activo el cliente activo de cualquier carácter restante (s). Cuando todos los caracteres están ocultos, no hay ningún cliente de entrada activo. Sin embargo, en esta situación, si el usuario presiona la tecla de micrófono de escucha, el agente continuará escuchando sus comandos (mediante el motor de reconocimiento de voz que coincide con el carácter superior del último cliente de entrada-activo).

Si hay varios clientes que comparten el mismo carácter, el servidor designará su *cliente activo* como cliente de entrada-activo. El carácter activo es el nivel superior en el orden del cliente. Puede establecer que el cliente sea el cliente activo o no activo mediante el método [**Activar**](activate-method.md) . También puede utilizar el método **Activate** para que la entrada de cliente sea explícitamente activa; pero para evitar interrumpir a otros clientes del carácter, solo debe hacerlo cuando la aplicación cliente esté activa. Por ejemplo, si el usuario hace clic en la ventana de la aplicación y activa la aplicación, puede llamar al método **Activar** para recibir y procesar la entrada de mouse y voz dirigida al carácter.

 

 




