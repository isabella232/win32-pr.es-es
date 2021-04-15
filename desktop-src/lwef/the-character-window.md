---
title: La ventana de caracteres
description: La ventana de caracteres
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421660"
---
# <a name="the-character-window"></a>La ventana de caracteres

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El agente de Microsoft muestra los caracteres animados en sus propias ventanas que siempre aparecen en la parte superior del orden z de la ventana (es decir, siempre visible). Un usuario puede mover la ventana de un carácter arrastrando el carácter con el botón primario del mouse. La imagen de caracteres se mueve con el puntero. Además, una aplicación puede desplace un carácter mediante el método [**moveTo**](moveto-method.md) .

Cuando el usuario hace clic con el botón secundario en un carácter, aparece un menú emergente que muestra los siguientes comandos:

Abra la \| ventana de comandos cerrar <span class="underline">V</span>oz

IDE de <span class="underline">H</span>

----------------------------…

Get-Help\*


*OtherHostingApplicationCaption\*\**

\*Los comandos enumerados se basan en el cliente de entrada-activo. Para obtener más información sobre la definición de comandos que aparecen en el menú emergente, vea la introducción a la interfaz de programación de Microsoft Agent.

\*\*Las entradas que se muestran son todas las demás aplicaciones que hospedan el carácter actualmente. Para obtener más información sobre la definición de esta entrada, vea la introducción a la interfaz de programación del agente de Microsoft.

El \| comando abrir cerrar la ventana comandos de voz controla la presentación de la ventana comandos del carácter activo actual. Si los servicios de reconocimiento de voz están deshabilitados, este comando está deshabilitado. Si no están instalados los servicios de reconocimiento de voz, este comando no aparece.

El comando Hide oculta el carácter. La animación asignada al estado **ocultar** del carácter se reproduce y oculta el carácter. La letra "H" en Hide es la tecla de acceso del comando (mnemotécnico).

Los comandos de las aplicaciones que hospedan el carácter actualmente siguen el comando Hide, precedido por un separador. A continuación, los nombres de otras aplicaciones que utilizan el carácter aparecen, también precedidos por un separador.

 

 




