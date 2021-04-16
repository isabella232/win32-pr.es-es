---
title: Instrucciones de programación de Servicios de Escritorio remoto
description: Temas que proporcionan instrucciones para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de Servicios de Escritorio remoto, directrices de programación
- instrucciones de programación Servicios de Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676404"
---
# <a name="remote-desktop-services-programming-guidelines"></a>Instrucciones de programación de Servicios de Escritorio remoto

La mayoría de las aplicaciones basadas en Windows de 32 bits o de 64 bits se ejecutan "tal cual" en un entorno de Servicios de Escritorio remoto (conocido anteriormente como Terminal Services). Sin embargo, algunas aplicaciones funcionan correctamente y funcionan bien en un entorno de Servicios de Escritorio remoto, mientras que otras no. En los temas siguientes se proporcionan instrucciones para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Directrices para varios usuarios](multiple-user-guidelines.md)
</dt> <dd>

Directrices para desarrollar aplicaciones para varios usuarios en un entorno de Servicios de Escritorio remoto.

</dd> <dt>

[Instrucciones de rendimiento](performance-guidelines.md)
</dt> <dd>

Directrices para desarrollar aplicaciones que funcionan bien en un entorno de Servicios de Escritorio remoto.

</dd> <dt>

[Instrucciones generales de programación](general-programming-guidelines.md)
</dt> <dd>

Directrices para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.

</dd> </dl>

Muchas de estas instrucciones son buenas prácticas de programación que beneficiarán a las aplicaciones que se ejecutan en cualquier entorno de Windows. Sin embargo, algunas optimizaciones recomendadas, como la limitación de los efectos gráficos, son optimizaciones que solo deseaba cuando la aplicación se ejecuta en Servicios de Escritorio remoto. Para obtener un ejemplo de código que muestra cómo detectar un entorno de Servicios de Escritorio remoto, consulte [detectar el entorno de servicios de escritorio remoto](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>


</dt> <dt>

[Terminal Services es ahora Servicios de Escritorio remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Formato de archivo de plantilla administrativa](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[Seguridad y derechos de acceso de la clave del registro](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[Subárboles del registro](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[Descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[Derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Modelo de Access Control](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 