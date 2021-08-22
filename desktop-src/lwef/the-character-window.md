---
title: Ventana De caracteres
description: Ventana De caracteres
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426aab4cbd6e0ad536135cb47ec9a636ea56a0509f3fb0cb75ad6440addc62da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474891"
---
# <a name="the-character-window"></a>Ventana De caracteres

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Microsoft Agent muestra caracteres animados en sus propias ventanas que siempre aparecen en la parte superior de la ventana orden Z (es decir, siempre en la parte superior). Un usuario puede mover la ventana de un carácter arrastrando el carácter con el botón izquierdo del mouse. La imagen de caracteres se mueve con el puntero. Además, una aplicación puede mover un carácter mediante el [**método MoveTo.**](moveto-method.md)

Cuando el usuario hace clic con el botón derecho en un carácter, aparece un menú emergente que muestra los comandos siguientes:

Abrir \| la ventana Cerrar <span class="underline">comandos</span>de V oice

<span class="underline">Ide de H</span>

----------------------------…

Get-Help\*


*OtherHostingApplicationCaption\*\**

\*Los comandos enumerados se basan en el cliente activo de entrada. Para obtener más información sobre cómo definir comandos que aparecen en el menú emergente, vea Información general sobre la interfaz de programación de Microsoft Agent.

\*\*Las entradas enumeradas son todas las demás aplicaciones que hospedan actualmente el carácter. Para obtener más información sobre cómo definir esta entrada, vea Información general sobre la interfaz de programación de Microsoft Agent.

El comando Abrir ventana De cerrar comandos de voz controla la presentación de la ventana \| Comandos del carácter activo actual. Si los servicios de reconocimiento de voz están deshabilitados, este comando está deshabilitado. Si los servicios de reconocimiento de voz no están instalados, este comando no aparece.

El comando Ocultar oculta el carácter. La animación asignada al estado **Ocultar** del carácter se reproduce y oculta el carácter. La letra "H" en hide es la clave de acceso del comando (mnemonic).

Los comandos de las aplicaciones que hospedan actualmente el carácter siguen el comando Ocultar, precedido por un separador. A continuación, aparecen los nombres de otras aplicaciones que usan el carácter , precedidos también por un separador.

 

 




