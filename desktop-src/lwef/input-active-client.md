---
title: Input-Active cliente
description: Input-Active cliente
ms.assetid: b46e91d3-eca7-4a4a-b1ce-27b5e6ad92a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9555b614a30e73df0cc7d1d81cd8192480d49261a32e8be8d164bdb277e4c0f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943965"
---
# <a name="input-active-client"></a>Input-Active cliente

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Dado que varias aplicaciones cliente pueden compartir el mismo carácter y porque varios clientes pueden  usar caracteres diferentes al mismo tiempo, el servidor designa un cliente como cliente activo de entrada y envía la entrada de mouse y voz solo a esa aplicación cliente. Esto mantiene la administración ordenada de la entrada del usuario, de modo que un cliente adecuado responda a la entrada.

Normalmente, la interacción del usuario determina qué aplicación cliente se convierte en entrada-activa. Por ejemplo, si el usuario hace clic en un carácter, la aplicación cliente de ese carácter se convierte en entrada-activa. Del mismo modo, si un usuario habla el nombre de un carácter, se convierte en activo de entrada. Además, cuando el servidor procesa el método [**Show**](show-method.md) de un carácter, el cliente de ese carácter se convierte en activo de entrada.

Cuando un carácter está oculto, el cliente de ese carácter ya no estará activo en la entrada para ese carácter. El servidor hace automáticamente que el cliente activo de los caracteres restantes de entrada-activo. Cuando todos los caracteres están ocultos, no hay ningún cliente activo de entrada. Sin embargo, en esta situación, si el usuario presiona la tecla de acceso rápido Escucha, el Agente seguirá escuchando sus comandos (mediante el motor de reconocimiento de voz que coincide con el carácter superior del último cliente activo de entrada).

Si varios clientes comparten el mismo carácter, el servidor designará su *cliente activo como* cliente activo de entrada. El carácter activo es el más alto en el orden de cliente. Puede establecer que el cliente sea el cliente activo o no activo mediante el [**método Activate.**](activate-method.md) También puede usar el método **Activate** para activar explícitamente la entrada del cliente. pero para evitar interrumpir otros clientes del carácter, debe hacerlo solo cuando la aplicación cliente esté activa. Por ejemplo, si el usuario hace clic en la ventana de la aplicación, activando la aplicación, puede llamar al método **Activate** para recibir y procesar la entrada de mouse y voz dirigida al carácter.

 

 




