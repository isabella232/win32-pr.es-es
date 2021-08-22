---
description: Control de versiones (Windows guía de calidad de aplicaciones de Windows Server 2008 R2)
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Control de versiones (Windows guía de calidad de aplicaciones de Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f029f5c3c17a481ddebe7976985ddff0f926fd162989a612e23af721b71c58e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994555"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Control de versiones (Windows guía de calidad de aplicaciones de Windows Server 2008 R2)

Uno de los problemas de compatibilidad de aplicaciones más comunes para Windows Internet Explorer son cadenas del Agente de usuario (UA) y vectores de versión. Windows Internet Explorer 8 presenta una nueva cadena ua para ayudar a las aplicaciones a detectar qué versión están ejecutando los usuarios. Además de aumentar simplemente el valor MSIE asociado a Internet Explorer en la cadena ua, Internet Explorer 8 agrega un valor Trident/4.0 para ayudarle a detectar si Internet Explorer 8 se ejecuta en modo Vista de compatibilidad. Estos cambios, además de las comprobaciones de versiones codificadas de forma rígida, pueden presentar problemas de compatibilidad entre exploradores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar actualizaciones que afectan a la compatibilidad entre exploradores](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



