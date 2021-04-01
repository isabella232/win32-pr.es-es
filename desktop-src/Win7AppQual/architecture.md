---
description: Internet Explorer de acoplamiento flexible (LCIE) mejora la confiabilidad del explorador separando sus componentes y aflojando sus interdependencias.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Arquitectura (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd27246b7b19765288a280bd467de86d2fe50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818467"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Arquitectura (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)

*Internet Explorer de acoplamiento flexible* (LCIE) mejora la confiabilidad del explorador separando sus componentes y aflojando sus interdependencias.

En concreto, LCIE intenta aislar el marco de Windows Internet Explorer y sus pestañas en procesos independientes. En Windows Internet Explorer 8, este aislamiento mejora el rendimiento y la escalabilidad. Este cambio arquitectónico puede afectar a la compatibilidad de extensiones y complementos, incluidos los controles ActiveX, los objetos auxiliares del explorador (BHO) y los componentes de la barra de herramientas de la interfaz de usuario que se crean mediante técnicas de programación anteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Actualizaciones de diseño que afectan a la compatibilidad entre exploradores](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



