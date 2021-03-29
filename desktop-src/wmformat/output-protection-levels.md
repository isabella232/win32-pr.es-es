---
title: Niveles de protección de salida
description: Niveles de protección de salida
ms.assetid: 89a9fc13-5ade-4a33-8304-05a2ec999fc1
keywords:
- Windows Media Format SDK, niveles de protección de salida (OPL)
- Administración de derechos digitales (DRM), niveles de protección de salida (OPL)
- DRM (administración de derechos digitales), niveles de protección de salida (OPL)
- niveles de protección de salida (OPL)
- OPL (niveles de protección de salida)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e5c1e08615b55aa1fb63e6d0c4e7bb82887c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993992"
---
# <a name="output-protection-levels"></a>Niveles de protección de salida

Los niveles de protección de salida (OPLs) son clasificaciones numéricas asociadas a diversas tecnologías que reciben contenido multimedia digital. El nivel que admite la tecnología depende del grado de seguridad. El sistema de OPL, introducido en Windows Media DRM 10, permite crear licencias con más flexibilidad que en versiones anteriores. Puede especificar el número mínimo de OPLs necesarios para la reproducción y la copia. Además, puede especificar excepciones para el OPL mínimo, para permitir que una tecnología no esté clasificada lo suficientemente alta o para no permitir una tecnología con un OPL que supere el mínimo.

Al especificar restricciones a las licencias mediante OPLs, un propietario de contenido solo necesita usar dos acciones (copiar y reproducir), donde las versiones anteriores tenían acciones independientes definidas para los distintos tipos de dispositivos admitidos para copiar (SDMI, no SDMI y CD de audio de libro rojo).

**Nota:** DRM no es compatible con la versión basada en x64 de este SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Trabajar con niveles de protección de salida**](working-with-output-protection-levels.md)
</dt> </dl>

 

 




