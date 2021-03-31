---
description: El propósito de la regla de directiva de autorización central (CAPR) es proporcionar una definición en todo el dominio de un aspecto aislado de la Directiva de autorización de la organización.
ms.assetid: 51436332-F06A-4929-B3C1-AD2F66C3273B
title: Regla de directiva de autorización central
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda6279b2bf28f80f99a0e2608b5bf209855a76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083500"
---
# <a name="central-authorization-policy-rule"></a>Regla de directiva de autorización central

El propósito de la regla de directiva de autorización central (CAPR) es proporcionar una definición en todo el dominio de un aspecto aislado de la Directiva de autorización de la organización. El administrador define el CAPR para que aplique uno de los requisitos de autorización específicos. Puesto que CAPR define solo un requisito concreto de la Directiva de autorización, se puede definir y entender más fácilmente que si todos los requisitos de la Directiva de autorización de la organización se compilan en una única definición de directiva.

CAPR tiene los siguientes atributos:

-   Nombre: identifica el CAPR para los administradores.
-   Descripción: define el propósito del CAPR y cualquier información que puedan necesitar los consumidores de la CAPR.
-   Expresión de aplicabilidad: define los recursos o las situaciones en las que se aplicará la Directiva.
-   ID: identificador que se usa en la auditoría de cambios en CAPR.
-   Directiva de Access Control efectiva: un descriptor de seguridad de Windows que contiene una DACL que define la Directiva de autorización efectiva.
-   Expresión de excepción: una o más expresiones que proporcionan un medio para invalidar la Directiva y conceder acceso a una entidad de seguridad de acuerdo con la evaluación de la expresión.
-   Directiva de almacenamiento provisional: un descriptor de seguridad de Windows opcional que contiene una DACL que define una directiva de autorización propuesta (lista de entradas de control de acceso) que se probará con la Directiva vigente, pero no se aplicará. Si hay una diferencia entre los resultados de la Directiva efectiva y la Directiva de almacenamiento provisional, la diferencia se registrará en el registro de eventos de auditoría.
    -   Dado que el almacenamiento provisional puede tener un efecto imprevisible en el rendimiento del sistema, un administrador de directiva de grupo debe ser capaz de seleccionar equipos específicos en los que se aplicará el almacenamiento provisional. Esto permite que la directiva existente esté en su lugar en la mayoría de los equipos de una unidad organizativa mientras se está realizando el almacenamiento provisional en un subconjunto de los equipos.
    -   P2: un administrador local en un equipo determinado debe poder deshabilitar el almacenamiento provisional si el almacenamiento provisional en dicho equipo está causando una degradación del rendimiento.
-   Backlink to CAP: una lista de vínculos a cualquier Cap que puedan hacer referencia a este CAPR.

Durante la comprobación de acceso, se evalúa la aplicabilidad de CAPR en función de la expresión de aplicabilidad. Si un CAPR es aplicable, se evalúa para determinar si proporciona al usuario solicitante el acceso solicitado al recurso identificado. Después, los resultados de la evaluación de cabo se unen lógicamente por **y** con los resultados de la DACL en el recurso y cualquier otro CAPRs aplicable en el recurso.

CAPRs de ejemplo:

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

## <a name="deny-aces-in-capes"></a>Denegar ACE en CAPEs

En Windows 8, las ACE de denegación no se admitirán en CAPR. La experiencia de usuario de creación de CAPR no permitirá la creación de una ACE de denegación. Además, cuando LSA recupera el CAP de Active Directory, LSA comprobará que ningún CAPRs tenga ACE de denegación. Si se encuentra una ACE deny en un CAPR, el extremo se tratará como no válido y no se copiará en el registro o en SRM.

> [!Note]  
> La comprobación de acceso no exigirá que haya ninguna ACE de denegación presente. Se aplicarán las ACE de denegación en un CAPR. Se espera que las herramientas de creación impidan que esto suceda.

 

## <a name="cape-definition"></a>Definición de cabo

CAPRs se crean mediante una nueva experiencia de usuario que se proporciona en Centro de administración de Active Directory (ADAC). En ADAC, se proporciona una nueva opción de tarea para crear un CAPR. Cuando se selecciona esta tarea, ADAC solicitará al usuario un cuadro de diálogo que pide al usuario un nombre de CAPR y una descripción. Cuando se proporcionan, se habilitan los controles para definir cualquiera de los elementos CAPR restantes. Para cada uno de los elementos CAPR restantes, el UX llamará a la interfaz de usuario de ACL para permitir la definición de expresiones y/o ACL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)
</dt> <dt>

[Escenario de Access Control dinámico (DAC)](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap)
</dt> </dl>

 

 
