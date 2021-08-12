---
description: Propiedad de contexto de seguridad
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Propiedad de contexto de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c537dc8c9b925fff5f7fc4f3da99fd361bfb02f61008b7d7af8a421b9f1d11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546826"
---
# <a name="security-context-property"></a>Propiedad de contexto de seguridad

Al igual que con todos los servicios automáticos proporcionados por COM+, la comprobación automática de roles se basa en las propiedades incluidas en el contexto del objeto. La determinación de si se debe realizar una comprobación de seguridad en una llamada a un componente se basa en la propiedad de seguridad en el contexto de objeto creado cuando se crea una instancia del componente configurado.

Por lo general, no es necesario preocuparse por esta propiedad. COM+, no usted, la usa directamente. Sin embargo, en algunas circunstancias, es posible que desee un control estricto sobre la activación de un objeto. En este caso, la propiedad de seguridad puede afectar al contexto en el que se activa el objeto. Es decir, si un objeto tiene una configuración incompatible con el contexto de su creador, se activará en su propio contexto. La propiedad de seguridad puede influir en esto, al igual que cualquier propiedad en el contexto del objeto.

Si no desea que la configuración de seguridad influya en la activación, puede elegir solo la comprobación de acceso de nivel de proceso. Esto suprime la propiedad de seguridad en el contexto del objeto, aunque deshabilita eficazmente la comprobación basada en roles y hace que la información de contexto de llamada de seguridad [no](security-call-context-information.md) esté disponible.

Para obtener más información sobre las comprobaciones de acceso de nivel de proceso, vea [Límites de seguridad.](security-boundaries.md) Para ver cómo establecer la seguridad de nivel de proceso, vea Establecer un nivel de seguridad para [las comprobaciones de acceso.](setting-a-security-level-for-access-checks.md)

Para obtener más información sobre el contexto de objeto, vea [Contextos](com--contexts.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseño eficaz de roles](designing-roles-effectively.md)
</dt> <dt>

[Límites de seguridad](security-boundaries.md)
</dt> <dt>

[Información de contexto de llamada de seguridad](security-call-context-information.md)
</dt> <dt>

[Uso de roles para la autorización de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



