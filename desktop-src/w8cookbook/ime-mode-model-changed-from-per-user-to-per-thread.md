---
title: Cambios en el modelo de modo IME
description: Modelo de modo IME cambiado de por usuario a por subproceso
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781c322949f17d4d3313b6a9b7b5eff9b1e83b06
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359314"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a>Modelo de modo IME cambiado de por usuario a por subproceso

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

En Windows 8, el modo de conversión de IME y el modo de oración IME se basaban en el contexto de usuario y el cambio de modo de una aplicación afectaba a todas las demás aplicaciones. Este comportamiento se puede deshabilitar mediante la configuración de la opción "permitirme establecer un método de entrada diferente para cada aplicación" en la sección Configuración avanzada del panel de control del lenguaje.

Con el fin de mejorar la compatibilidad, en Windows 8.1 los modos se almacenan en un contexto de entrada independientemente de la forma en que se establece el control "permitirme establecer un método de entrada diferente para cada ventana de la aplicación". En Windows 8.1, la configuración "permitirme establecer un método de entrada diferente para cada aplicación" afecta solo a la selección del propio método de entrada.

Al iniciarse la aplicación, el modo IME se establece en los valores predeterminados siguientes:



|          | Panel de entrada de software | Teclado de hardware |
|----------|----------------------|-------------------|
| KOR, JPN | Activado                   | Off               |
| CHS, CHT  | Activado                   | Activado                |



 

## <a name="manifestations"></a>Manifestaciones

Cuando un usuario cambia el modo IME en una aplicación, el cambio no afecta a otras aplicaciones.

## <a name="resources"></a>Recursos

-   [Valores del modo de conversión IME](../intl/ime-conversion-mode-values.md)
-   [Valores del modo de oración IME](../intl/ime-sentence-mode-values.md)

 

 