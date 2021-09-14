---
description: El propósito de la regla de directiva de autorización central (CAPR) es proporcionar una definición de todo el dominio de un aspecto aislado de la directiva de autorización de organizaciones.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Regla de directiva de autorización central
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda6279b2bf28f80f99a0e2608b5bf209855a76a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168958"
---
# <a name="central-authorization-policy-rule"></a>Regla de directiva de autorización central

El propósito de la regla de directiva de autorización central (CAPR) es proporcionar una definición de todo el dominio de un aspecto aislado de la directiva de autorización de la organización. El administrador define el CAPR para aplicar uno de los requisitos de autorización específicos. Puesto que capr define solo un requisito específico deseado de la directiva de autorización, puede definirse y entenderse más sencillamente que si todos los requisitos de la directiva de autorización de la organización se compilan en una única definición de directiva.

Capr tiene los siguientes atributos:

-   Nombre: identifica el CAPR a los administradores.
-   Descripción: define el propósito del CAPR y cualquier información que puedan necesitar los consumidores del CAPR.
-   Expresión de aplicabilidad: define los recursos o situaciones en las que se aplicará la directiva.
-   Id.: identificador para su uso en la auditoría de los cambios en el CAPR.
-   Directiva de Access Control efectiva: un descriptor Windows seguridad que contiene una DACL que define la directiva de autorización efectiva.
-   Expresión de excepción: una o varias expresiones que proporcionan un medio para invalidar la directiva y conceder acceso a una entidad de seguridad según la evaluación de la expresión.
-   Directiva de almacenamiento provisional: un descriptor de seguridad Windows opcional que contiene una DACL que define una directiva de autorización propuesta (lista de entradas de control de acceso) que se probará con la directiva efectiva, pero que no se aplicará. Si hay una diferencia entre los resultados de la directiva efectiva y la directiva de ensayo, la diferencia se registrará en el registro de eventos de auditoría.
    -   Dado que el almacenamiento provisional puede tener un efecto imprevisible en el rendimiento del sistema, un administrador de directiva de grupo debe poder seleccionar máquinas específicas en las que el almacenamiento provisional estará en vigor. Esto permite que la directiva existente esté en su lugar en la mayoría de las máquinas de una unidad organizativa mientras se realiza el almacenamiento provisional en un subconjunto de las máquinas.
    -   P2: un administrador local de un equipo determinado debe poder deshabilitar el almacenamiento provisional si el almacenamiento provisional en esa máquina está causando demasiada degradación del rendimiento.
-   Vínculo hacia atrás a CAP: una lista de vínculos backlink a cualquier CAP que pueda hacer referencia a este CAPR.

Durante la comprobación de acceso, se evalúa la aplicabilidad del CAPR en función de la expresión de aplicabilidad. Si un CAPR es aplicable, se evalúa si proporciona al usuario solicitante el acceso solicitado al recurso identificado. Los resultados de la evaluación DE CAPITAL se unen lógicamente mediante **AND** con los resultados de dacl en el recurso y cualquier otra CAPR aplicable en vigor en el recurso.

CAPR de ejemplo:

``` syntax
[HBI-POLICY]
APPLIES-TO="(@resource.confidentiality == HBI"
SD ="D:(A;;FA;;;AU;(@memberOf("Smartcard Logon")))"
StagingSD = "D:(A;;FA;;;AU;(@memberOf("Smartcard Logon") AND memberOfAny(Resource.ProjectGroups)))"
description="Control access to sensitive information"
 
[RETENTION-POLICY]
Applies-To="@resource.retention == true"
SD ="D:(A;;;FA;;BA)(A;;FR;;;WD)"
description="If the document is marked for retention, then it is read-only for everyone however Local Admins have 
full control to them to put them out of retention when the time comes"
 
[TEST-FINANCE-POLICY]
Applies-To="@resource.label == 'finance'"
SD="D:(A;;FA;;;AU;(member_of(FinanceGroup))"
description="Department: Only employees of the finance department should be able to read documents labeled as finance"
```

## <a name="deny-aces-in-capes"></a>Denegar ACE en CAPE

En Windows 8 no se admiten las ACE de denegación en un CAPR. La experiencia de usuario de creación de CAPR no permitirá la creación de una ACE de denegación. Además, cuando el LSA recupera el CAP de Active Directory, LSA comprobará que ningún CAPR tenga ACE de denegación. Si se encuentra una ACE de denegación en un CAPR, el CAP se tratará como no válido y no se copiará en el registro o SRM.

> [!Note]  
> La comprobación de acceso no exigirá que no haya ninguna ACE de denegación. Se aplicarán las ACE de denegación en un CAPR. Se espera que las herramientas de creación impidan que esto suceda.

 

## <a name="cape-definition"></a>Definición de CABO

Las CAPR se crean a través de una nueva experiencia de usuario Centro de administración de Active Directory (ADAC). En ADAC se proporciona una nueva opción de tarea para crear un CAPR. Cuando se selecciona esta tarea, ADAC le pedirá al usuario un cuadro de diálogo que le pida un nombre CAPR y una descripción. Cuando se proporcionan, se habilitan los controles para definir cualquiera de los elementos CAPR restantes. Para cada uno de los elementos CAPR restantes, la experiencia de usuario llamará a acl-UI para permitir la definición de expresiones o ACL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[Escenario de Access Control dinámica (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
