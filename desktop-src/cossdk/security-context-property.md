---
description: Propiedad de contexto de seguridad
ms.assetid: 7ffae145-be13-4a2c-beb1-eaa1d11ad9a7
title: Propiedad de contexto de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b061ef7c0d0d0c146b626c11fd550c48ab488a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063883"
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

 

 



