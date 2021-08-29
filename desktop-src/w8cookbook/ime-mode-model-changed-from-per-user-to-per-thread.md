---
title: Cambios en el modelo de modo IME
description: Modelo de modo IME cambiado de por usuario a por subproceso
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c86c8ba5e00bf4fb47d2908e626736252a8a6dc54b9c6ac4fa866782fde8d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815205"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a>Modelo de modo IME cambiado de por usuario a por subproceso

## <a name="platforms"></a>Plataformas

<dl> Clientes: Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

En Windows 8, el modo de conversión de IME y el modo de oración IME se basaban en el contexto de usuario y el cambio del modo de una aplicación afectaba a todas las demás aplicaciones. Este comportamiento podría deshabilitarse mediante el valor "Let me set a different input method for each app window" (Permitirme establecer un método de entrada diferente para cada ventana de la aplicación) en la sección de configuración avanzada del panel de control de idioma.

Para mejorar la compatibilidad, en Windows 8.1 los modos se almacenan en un contexto de entrada independientemente de cómo se establezca el control "Let me set a different input method for each app window" (Permitirme establecer un método de entrada diferente para cada ventana de la aplicación). En Windows 8.1, el valor "Let me set a different input method for each app window" (Permitirme establecer un método de entrada diferente para cada ventana de la aplicación) solo afecta a la selección del propio método de entrada.

Al iniciar la aplicación, el modo IME se establece en los siguientes valores predeterminados:



| &nbsp;   | Panel de entrada de software | Teclado de hardware |
|----------|----------------------|-------------------|
| KOR, JPN | Activado                   | Desactivado               |
| CHS,CHT  | Activado                   | Activado                |



 

## <a name="manifestations"></a>Manifestaciones

Cuando un usuario cambia el modo IME en una aplicación, el cambio no afecta a otras aplicaciones.

## <a name="resources"></a>Recursos

-   [Valores del modo de conversión de IME](../intl/ime-conversion-mode-values.md)
-   [Valores del modo de oración IME](../intl/ime-sentence-mode-values.md)

 

 