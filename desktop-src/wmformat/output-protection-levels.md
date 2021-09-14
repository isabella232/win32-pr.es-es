---
title: Niveles de protección de salida
description: Niveles de protección de salida
ms.assetid: 89a9fc13-5ade-4a33-8304-05a2ec999fc1
keywords:
- Windows SDK de formato multimedia, niveles de protección de salida (OPL)
- administración de derechos digitales (DRM), niveles de protección de salida (OPL)
- DRM (administración de derechos digitales), niveles de protección de salida (OPL)
- niveles de protección de salida (OPL)
- OPL (niveles de protección de salida)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e5c1e08615b55aa1fb63e6d0c4e7bb82887c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266959"
---
# <a name="output-protection-levels"></a>Niveles de protección de salida

Los niveles de protección de salida (OPL) son clasificaciones numéricas asociadas a diversas tecnologías que reciben contenido multimedia digital. El nivel que admite una tecnología depende de su seguridad. El sistema OPL, introducido en Windows Media DRM 10, permite crear licencias con más flexibilidad que en versiones anteriores. Puede especificar las OPERACIONES mínimas necesarias para la reproducción y la copia. Además, puede especificar excepciones al OPL mínimo, ya sea para permitir una tecnología no clasificada lo suficientemente alta o para no permitir una tecnología con un OPL que supere el mínimo.

Al especificar restricciones a las licencias mediante LASP, un propietario del contenido solo necesita usar dos acciones (Copiar y Reproducir), donde las versiones anteriores tenían acciones independientes definidas para los distintos tipos de dispositivos compatibles con la copia (SDMI, no SDMI y CD de audio de libro rojo).

**Nota** DRM no es compatible con la versión basada en x64 de este SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**Trabajar con niveles de protección de salida**](working-with-output-protection-levels.md)
</dt> </dl>

 

 




