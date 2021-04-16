---
description: Seguridad de aplicaciones de niveles múltiples
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Seguridad de aplicaciones de niveles múltiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150f7894c7d11e832786e31ab028f9dbac35f6e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677219"
---
# <a name="multi-tier-application-security"></a>Seguridad de aplicaciones de niveles múltiples

Puede encontrar opciones difíciles para decidir exactamente dónde aplicar la seguridad en una aplicación de varios niveles basada en componentes: en la base de datos de. ¿En el nivel intermedio? ¿En los componentes? ¿Alguna otra parte? Todas? A medida que los mecanismos de seguridad aumentan en número y complejidad, el rendimiento disminuye y el comportamiento de la aplicación es menos predecible. No obstante, debe asegurarse de que se protegen los datos, se siguen las reglas de negocios y se registra la actividad significativa, y la aplicación sigue funcionando para los clientes según lo previsto. Debe asegurarse de que todas las rutas de acceso de cliente a través de la aplicación son correctas y que los puntos de control de seguridad que tiene en su lugar serán suficientes.

La decisión más difícil es a menudo si se aplica la seguridad en la base de datos. Históricamente, aquí es donde la seguridad es la más estricta porque se percibe como el único reino que debe ser realmente seguro, y los administradores de bases de datos son muy reticentes a confiar en otros para que apliquen seguridad para ellos. Pero la exigencia de seguridad en la base de datos puede resultar bastante costosa y difícil de escalar, lo que es precisamente el punto de escribir aplicaciones de varios niveles en primer lugar.

La regla general que debe seguir con las aplicaciones escalables de varios niveles mediante COM+ es que, siempre que sea posible, debe exigir una seguridad detallada en la aplicación COM+ en el nivel intermedio. De este modo, podrá aprovechar al máximo los servicios escalables que proporciona COM+. Autentique en la base de datos solo cuando sea absolutamente necesario y evalúe completamente las implicaciones de rendimiento de hacerlo.

Para obtener una explicación de los problemas que se deben tener en cuenta a la hora de decidir dónde realizar las comprobaciones de seguridad, consulte [decidir dónde aplicar la seguridad](deciding-where-to-enforce-security.md).

Para obtener una descripción de algunos escenarios básicos de la protección de aplicaciones de niveles múltiples, vea [escenarios básicos para proteger datos en aplicaciones de varios niveles](basic-scenarios-for-securing-data-in-multi-tier-applications.md).

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

[Administración de la seguridad basada en roles](role-based-security-administration.md)
</dt> <dt>

[Usar la Directiva de restricción de software en COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



