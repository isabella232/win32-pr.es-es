---
title: Servicios de Escritorio remoto de programación
description: Temas que proporcionan instrucciones para desarrollar aplicaciones en un Servicios de Escritorio remoto de aplicaciones.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto , directrices de programación
- directrices de programación Servicios de Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1f935ada4dfe486b418b5ec3b6f347eb6166e6b392a3adc1bd8c1e5987a773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999875"
---
# <a name="remote-desktop-services-programming-guidelines"></a>Servicios de Escritorio remoto de programación

La mayoría de las aplicaciones basadas en Windows de 32 o 64 bits existentes se ejecutan "tal y como están" en un entorno de Servicios de Escritorio remoto (anteriormente conocido como Terminal Services). Sin embargo, algunas aplicaciones funcionan correctamente y funcionan bien en Servicios de Escritorio remoto entorno, mientras que otras no. En los temas siguientes se proporcionan directrices para desarrollar aplicaciones en un Servicios de Escritorio remoto específico.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Directrices para varios usuarios](multiple-user-guidelines.md)
</dt> <dd>

Directrices para desarrollar aplicaciones para varios usuarios en Servicios de Escritorio remoto entorno.

</dd> <dt>

[Directrices de rendimiento](performance-guidelines.md)
</dt> <dd>

Directrices para desarrollar aplicaciones que tienen un buen rendimiento en Servicios de Escritorio remoto entorno.

</dd> <dt>

[Directrices generales de programación](general-programming-guidelines.md)
</dt> <dd>

Directrices para desarrollar aplicaciones en un Servicios de Escritorio remoto único.

</dd> </dl>

Muchas de estas directrices son procedimientos de programación recomendados que beneficiarán a las aplicaciones que se ejecutan en Windows entorno. Sin embargo, algunas optimizaciones recomendadas, como limitar los efectos gráficos, son optimizaciones que solo se desean cuando la aplicación se ejecuta en Servicios de Escritorio remoto. Para obtener un ejemplo de código que muestra cómo detectar un entorno Servicios de Escritorio remoto, vea [Detección](detecting-the-terminal-services-environment.md)del entorno Servicios de Escritorio remoto .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>


</dt> <dt>

[Terminal Services ya está Servicios de Escritorio remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Formato de archivo de plantilla administrativa](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[Derechos de acceso y seguridad de la clave del Registro](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[Subárboles del Registro](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[Descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[Derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Access Control modelo](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 