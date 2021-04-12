---
title: Derechos de acceso de control (AD DS)
description: Todos los objetos de Active Directory Domain Services admiten un conjunto estándar de derechos de acceso definidos en la \_ \_ enumeración ADS Rights enum.
ms.assetid: 27ad74bd-ad87-422e-a4a2-02c0d51c4dd4
ms.tgt_platform: multiple
keywords:
- Derechos de acceso de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 048c4aa685e0c569ef2ac762dcf17366a2394826
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487483"
---
# <a name="control-access-rights-ad-ds"></a>Derechos de acceso de control (AD DS)

Todos los objetos de Active Directory Domain Services admiten un conjunto estándar de derechos de acceso definidos en la enumeración [**ADS \_ Rights \_ enum**](/windows/win32/api/iads/ne-iads-ads_rights_enum) . Estos derechos de acceso se pueden usar en las entradas de Access Control (ACE) del descriptor de seguridad de un objeto para controlar el acceso al objeto. es decir, para controlar quién puede realizar operaciones estándar, como crear y eliminar objetos secundarios, o leer y escribir los atributos del objeto. Sin embargo, para algunas clases de objeto, puede ser conveniente controlar el acceso de forma que los derechos de acceso estándar no los admitan. Para facilitar esto, Active Directory Domain Services permitir que el mecanismo de control de acceso estándar se extienda a través del objeto **controlAccessRight** .

Los derechos de acceso de control se usan de tres maneras:

-   Para los derechos extendidos, que son operaciones especiales no tratadas por el conjunto estándar de derechos de acceso. Por ejemplo, a la clase de usuario se le puede conceder el derecho "enviar como" que puede usar Exchange, Outlook o cualquier otra aplicación de correo para determinar si un usuario determinado puede hacer que otro usuario envíe correo en su nombre. Los derechos extendidos se crean en objetos **controlAccessRight** estableciendo el atributo **validAccesses** en el derecho de acceso de **ad \_ right \_ \_ control \_ Access** (256).
-   Para definir los conjuntos de propiedades, para permitir el control del acceso a un subconjunto de los atributos de un objeto, en lugar de solo a los atributos individuales. Con los derechos de acceso estándar, una única ACE puede conceder o denegar el acceso a todos los atributos de un objeto o a un solo atributo. Los derechos de acceso de control proporcionan una manera para que una única ACE controle el acceso a un conjunto de atributos. Por ejemplo, la clase de usuario es compatible con el conjunto de propiedades **de información personal** que incluye atributos como la dirección postal y el número de teléfono. Los derechos de los conjuntos de propiedades se crean en objetos **controlAccessRight** estableciendo el atributo **validAccesses** para que contenga los derechos de acceso de **ACTR \_ DS \_ Read \_ prop** (16) y **ACTRL \_ DS \_ Write \_ prop** (32).
-   En el caso de las escrituras validadas, para requerir que el sistema realice la comprobación de valores, o la validación, más allá de lo que necesita el esquema, antes de escribir un valor en un atributo en un objeto DS. Esto garantiza que el valor especificado para el atributo se ajusta a la semántica necesaria, está dentro de un intervalo de valores válido o se somete a alguna otra comprobación especial que no se realizaría para una escritura simple de bajo nivel en el atributo. Una escritura validada se asocia a un permiso especial que es distinto del permiso "escribir <attribute> " que permitiría escribir cualquier valor en el atributo sin la comprobación de valores realizada. La escritura validada es la única de los tres derechos de acceso de control que no se puede crear como un nuevo derecho de acceso de control para una aplicación. Esto se debe a que el sistema existente no se puede modificar mediante programación para exigir la validación. Si se ha configurado un derecho de acceso de control en el sistema como una escritura validada, el atributo **validAccesses** de los objetos **controlAccessRight** contendrá el derecho de acceso **ad \_ right \_ DS \_ Self** (8).

    Solo hay tres escrituras validadas definidas en el esquema de Active Directory de Windows 2000:

    -   Self-Membership permiso en un objeto de grupo, que permite agregar o quitar la cuenta del llamador, pero ninguna otra cuenta, de la pertenencia de un grupo.
    -   Permiso validado-DNS-host-name en un objeto de equipo, que permite establecer un atributo de nombre de host DNS que es compatible con el nombre de equipo y el nombre de dominio.
    -   Permiso validado-SPN en un objeto de equipo, que permite establecer un atributo SPN que es compatible con el nombre de host DNS del equipo.

Para mayor comodidad, cada derecho de acceso de control se representa mediante un objeto **controlAccessRight** en el contenedor Extended-Rights de la partición de configuración, aunque los conjuntos de propiedades y las escrituras validadas no se consideran derechos extendidos. Dado que el contenedor de configuración se replica en todo el bosque, los derechos de control se propagan por todos los dominios de un bosque. Hay una serie de derechos de acceso de control predefinidos y, por supuesto, también se pueden definir derechos de acceso personalizados.

Todos los derechos de control de acceso se pueden ver como permisos en el editor ACL.

Para obtener más información y un ejemplo de código de C++ y Visual Basic que establece una ACE para controlar el acceso de lectura y escritura a un conjunto de propiedades, consulte el [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

Para obtener más información sobre el uso de derechos de control de acceso para controlar el acceso a las operaciones especiales, vea:

-   [Crear un derecho de acceso a control](creating-a-control-access-right.md)
-   [Establecer una ACE right de control de acceso en la ACL de un objeto](setting-a-control-access-right-ace-in-an-objectampaposs-acl.md)
-   [Comprobar un derecho de acceso a control en la ACL de un objeto](checking-a-control-access-right-in-an-objectampaposs-acl.md)
-   [Leer un conjunto derecho de control de acceso en la ACL de un objeto](reading-a-control-access-right-set-in-an-objectampaposs-acl.md)

 

 