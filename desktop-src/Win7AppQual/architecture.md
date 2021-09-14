---
description: Las Internet Explorer de acoplamiento flexible (LCIE) mejoran la confiabilidad del explorador al separar sus componentes y aflojar su interdependencia.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Arquitectura (Windows guía de calidad de la aplicación Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd27246b7b19765288a280bd467de86d2fe50f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249393"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Arquitectura (Windows guía de calidad de la aplicación Windows Server 2008 R2)

*Las Internet Explorer* de acoplamiento flexible (LCIE) mejoran la confiabilidad del explorador al separar sus componentes y aflojar su interdependencia.

En concreto, LCIE intenta aislar el marco Windows Internet Explorer y sus pestañas en procesos independientes. En Windows Internet Explorer 8, este aislamiento mejora el rendimiento y la escalabilidad. Este cambio de arquitectura podría afectar a la compatibilidad de extensiones y complementos, incluidos los controles de ActiveX, los objetos auxiliares de explorador (SPO) y los componentes de la barra de herramientas de la interfaz de usuario que se han creado mediante técnicas de programación anteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar actualizaciones que afectan a la compatibilidad entre exploradores](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



