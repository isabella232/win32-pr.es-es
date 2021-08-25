---
description: Seguridad de aplicaciones de varios niveles
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Seguridad de aplicaciones de varios niveles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ba43970c2af5ff6c7abb733767b721091f6a3d3407178d5360e5f96db11d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070475"
---
# <a name="multi-tier-application-security"></a>Seguridad de aplicaciones de varios niveles

Puede enfrentarse a opciones difíciles a la hora de decidir con precisión dónde aplicar la seguridad en una aplicación basada en componentes de varios niveles: ¿En la base de datos? ¿En el nivel intermedio? ¿En los componentes? ¿En otro lugar? ¿Donde quiera? A medida que los mecanismos de seguridad aumentan en número y complejidad, el rendimiento disminuye y el comportamiento de la aplicación es menos predecible. No obstante, debe asegurarse de que los datos están protegidos, de que se siguen las reglas de negocio y de que se registra una actividad significativa y de que la aplicación sigue funcionando para los clientes según lo previsto. Debe estar seguro de que todas las rutas de acceso de cliente a través de la aplicación son correctas y que los puntos de control de seguridad que tenga serán suficientes.

La decisión más difícil suele ser si se debe aplicar la seguridad en la base de datos. Históricamente, aquí es donde la seguridad es más estricta porque se percibe como el único reino que debe ser realmente seguro, y los administradores de bases de datos son muy reacios a confiar en otra persona para exigirles seguridad. Pero aplicar la seguridad en la base de datos puede ser bastante costoso y difícil de escalar, que es precisamente el punto de escribir aplicaciones de varios niveles en primer lugar.

La regla general que se debe seguir con las aplicaciones escalables de varios niveles mediante COM+ es que, siempre que sea posible, debe aplicar la seguridad detallada en la aplicación COM+ en el nivel intermedio. Esto le permite aprovechar completamente los servicios escalables proporcionados por COM+. Autentíquense en la base de datos solo cuando sea absolutamente necesario y sopese totalmente las implicaciones de rendimiento de hacerlo.

Para obtener una explicación de los problemas que se deben tener en cuenta para decidir dónde realizar comprobaciones de seguridad, vea [Decidir dónde aplicar la seguridad.](deciding-where-to-enforce-security.md)

Para obtener una explicación de algunos escenarios básicos en la protección de aplicaciones de varios niveles, consulte Escenarios básicos para proteger datos [en aplicaciones de varios niveles.](basic-scenarios-for-securing-data-in-multi-tier-applications.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> <dt>

[Suplantación y delegación de cliente](client-impersonation-and-delegation.md)
</dt> <dt>

[Seguridad de aplicaciones de biblioteca](library-application-security.md)
</dt> <dt>

[Seguridad de componentes mediante programación](programmatic-component-security.md)
</dt> <dt>

[Administración de seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[Uso de la directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



