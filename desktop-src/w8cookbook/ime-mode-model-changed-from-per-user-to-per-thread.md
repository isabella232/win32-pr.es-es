---
title: Cambios en el modelo de modo IME
description: Modelo de modo IME cambiado de por usuario a por subproceso
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443255"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a>Modelo de modo IME cambiado de por usuario a por subproceso

## <a name="platforms"></a>Plataformas

<dl> Clientes: Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

En Windows 8, el modo de conversión de IME y el modo de oración de IME se basaban en el contexto de usuario y el cambio del modo de una aplicación afectaba a todas las demás aplicaciones. Este comportamiento podría deshabilitarse mediante el valor "Let me set a different input method for each app window" (Permitirme establecer un método de entrada diferente para cada ventana de la aplicación) en la sección de configuración avanzada del panel de control de idioma.

Para mejorar la compatibilidad, en Windows 8.1 los modos se almacenan en un contexto de entrada independientemente de cómo se establezca el control "Let me set a different input method for each app window" (Permitirme establecer un método de entrada diferente para cada ventana de la aplicación). En Windows 8.1, el valor "Let me set a different input method for each app window" (Permitirme establecer un método de entrada diferente para cada ventana de la aplicación) solo afecta a la selección del propio método de entrada.

Al iniciar la aplicación, el modo IME se establece en los valores predeterminados siguientes:



| &nbsp;   | Panel de entrada de software | Teclado de hardware |
|----------|----------------------|-------------------|
| KOR, JPN | Activado                   | Desactivado               |
| CHS,CHT  | Activado                   | Activado                |



 

## <a name="manifestations"></a>Manifestaciones

Cuando un usuario cambia el modo IME en una aplicación, el cambio no afecta a otras aplicaciones.

## <a name="resources"></a>Recursos

-   [Valores del modo de conversión de IME](../intl/ime-conversion-mode-values.md)
-   [Valores del modo de oración de IME](../intl/ime-sentence-mode-values.md)

 

 