---
title: Controlar los derechos de acceso (AD DS)
description: Todos los objetos de Active Directory Domain Services admiten un conjunto estándar de derechos de acceso definidos en la \_ enumeración ADS RIGHTS \_ ENUM.
ms.assetid: 27ad74bd-ad87-422e-a4a2-02c0d51c4dd4
ms.tgt_platform: multiple
keywords:
- Control de los derechos de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c975ac20cac683e754f1b703bd272356c9b8df8f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881613"
---
# <a name="control-access-rights-ad-ds"></a>Controlar los derechos de acceso (AD DS)

Todos los objetos de Active Directory Domain Services admiten un conjunto estándar de derechos de acceso definidos en la [**\_ enumeración ADS RIGHTS \_ ENUM.**](/windows/win32/api/iads/ne-iads-ads_rights_enum) Estos derechos de acceso se pueden usar en Access Control entradas (ACE) del descriptor de seguridad de un objeto para controlar el acceso al objeto. es decir, para controlar quién puede realizar operaciones estándar, como crear y eliminar objetos secundarios, o leer y escribir los atributos del objeto. Sin embargo, para algunas clases de objeto, puede ser conveniente controlar el acceso de una manera que no sea compatible con los derechos de acceso estándar. Para facilitar esto, Active Directory Domain Services el mecanismo de control de acceso estándar para extenderse a través del **objeto controlAccessRight.**

Los derechos de acceso de control se usan de tres maneras:

-   Para los derechos extendidos, que son operaciones especiales no cubiertas por el conjunto estándar de derechos de acceso. Por ejemplo, a la clase de usuario se le puede conceder un derecho "Enviar como" que puede usar Exchange, Outlook o cualquier otra aplicación de correo, para determinar si un usuario determinado puede hacer que otro usuario envíe correo en su nombre. Los derechos extendidos se crean en **objetos controlAccessRight** estableciendo el atributo **validAccesses** en igual al derecho de acceso **ADS RIGHT \_ \_ DS CONTROL \_ \_ ACCESS** (256).
-   Para definir conjuntos de propiedades, para permitir el control del acceso a un subconjunto de atributos de un objeto, en lugar de simplemente a los atributos individuales. Con los derechos de acceso estándar, una única ACE puede conceder o denegar el acceso a todos los atributos de un objeto o a un único atributo. Los derechos de acceso de control proporcionan una manera de que una única ACE controle el acceso a un conjunto de atributos. Por ejemplo, la clase de usuario admite el **conjunto de propiedades Personal-Information** que incluye atributos como la dirección postal y el número de teléfono. Los derechos de conjunto de propiedades se crean en los objetos **controlAccessRight** estableciendo el atributo **validAccesses** para que contenga los derechos de acceso **ACTR \_ DS \_ READ \_ PROP** (16) y **ACTRL \_ DS \_ WRITE \_ PROP** (32).
-   Para escrituras validadas, para requerir que el sistema realice la comprobación de valores, o validación, más allá de lo que requiere el esquema, antes de escribir un valor en un atributo en un objeto DS. Esto garantiza que el valor especificado para el atributo se ajusta a la semántica necesaria, está dentro de un intervalo legal de valores o se somete a alguna otra comprobación especial que no se realizaría para una escritura simple de bajo nivel en el atributo. Una escritura validada está asociada a un permiso especial distinto del permiso "Atributo de escritura" que permitiría escribir cualquier valor en el atributo sin realizar ninguna comprobación &lt; &gt; de valores. La escritura validada es la única de los tres derechos de acceso de control que no se pueden crear como un nuevo derecho de acceso de control para una aplicación. Esto se debe a que el sistema existente no se puede modificar mediante programación para aplicar la validación. Si se ha configurado un derecho de acceso de control en el sistema como una escritura validada, el atributo **validAccesses** de los objetos **controlAccessRight** contendrá el derecho de acceso **ADS RIGHT \_ \_ DS \_ SELF** (8).

    Solo hay tres escrituras validadas definidas en el Windows 2000 Active Directory esquema:

    -   Self-Membership permiso en un objeto Group, que permite agregar o quitar la cuenta del autor de la llamada, pero ninguna otra cuenta, de la pertenencia de un grupo.
    -   Permiso Validated-DNS-Host-Name en un objeto Computer, que permite establecer un atributo de nombre de host DNS compatible con el nombre de equipo y el nombre de dominio.
    -   Permiso SPN validado en un objeto Computer, que permite establecer un atributo SPN compatible con el nombre de host DNS del equipo.

Para mayor comodidad, cada derecho de acceso de control se representa mediante un **objeto controlAccessRight** en el contenedor Extended-Rights de la partición Configuration, aunque los conjuntos de propiedades y las escrituras validadas no se consideran derechos extendidos. Dado que el contenedor de configuración se replica en todo el bosque, los derechos de control se propagan a todos los dominios de un bosque. Hay una serie de derechos de acceso de control predefinidos y, por supuesto, también se pueden definir derechos de acceso personalizados.

Todos los derechos de acceso de control se pueden ver como permisos en el Editor de ACL.

Para obtener más información y un ejemplo de código de C++ y Visual Basic que establece una ACE para controlar el acceso de lectura y escritura a un conjunto de propiedades, vea Ejemplo de código para establecer una ACE en un objeto [de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

Para obtener más información sobre el uso de derechos de acceso de control para controlar el acceso a operaciones especiales, vea:

-   [Crear un derecho de acceso de control](creating-a-control-access-right.md)
-   [Establecimiento de una ACE de derecho de acceso de control en la ACL de un objeto](setting-a-control-access-right-ace-in-an-objectampaposs-acl.md)
-   [Comprobación de un derecho de acceso de control en la ACL de un objeto](checking-a-control-access-right-in-an-objectampaposs-acl.md)
-   [Leer un conjunto de derecho de acceso de control en la ACL de un objeto](reading-a-control-access-right-set-in-an-objectampaposs-acl.md)

 

 
