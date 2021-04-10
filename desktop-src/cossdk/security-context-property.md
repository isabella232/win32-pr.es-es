---
description: Propiedad de contexto de seguridad
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Propiedad de contexto de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275085"
---
# <a name="security-context-property"></a>Propiedad de contexto de seguridad

Como con cada servicio automático proporcionado por COM+, la comprobación automática de roles se basa en las propiedades incluidas en el contexto del objeto. La determinación de si una comprobación de seguridad debe realizarse en una llamada a un componente se basa en la propiedad de seguridad en el contexto del objeto creado cuando se crea una instancia del componente configurado.

Por lo general, no es necesario preocuparse por esta propiedad. lo usa directamente COM+, no. Sin embargo, en algunas circunstancias, puede que desee tener un control estricto sobre la activación de un objeto. En este caso, la propiedad de seguridad puede afectar al contexto en el que se activa el objeto. Es decir, si un objeto tiene una configuración incompatible con el contexto de su creador, se activará en su propio contexto. La propiedad de seguridad puede influir en esto, como puede ser cualquier propiedad en el contexto del objeto.

Si no desea que la configuración de seguridad afecte a la activación, puede elegir solo la comprobación de acceso de nivel de proceso. De este modo se suprime la propiedad de seguridad en el contexto del objeto, aunque se deshabilita la comprobación basada en roles y la [información del contexto de llamada de seguridad](security-call-context-information.md) no está disponible.

Para obtener más información sobre las comprobaciones de acceso de nivel de proceso, vea [límites de seguridad](security-boundaries.md). Para ver cómo establecer la seguridad de nivel de proceso, consulte [configuración de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md).

Para obtener más información sobre el contexto del objeto, vea [contextos](com--contexts.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar roles de forma eficaz](designing-roles-effectively.md)
</dt> <dt>

[Límites de seguridad](security-boundaries.md)
</dt> <dt>

[Información de contexto de llamada de seguridad](security-call-context-information.md)
</dt> <dt>

[Uso de roles para la autorización de cliente](using-roles-for-client-authorization.md)
</dt> </dl>

 

 



