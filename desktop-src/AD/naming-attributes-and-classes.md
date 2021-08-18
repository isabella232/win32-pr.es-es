---
title: Asignar nombres a atributos y clases
description: En este tema se incluyen instrucciones para asignar nombres a atributos y clases.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Asignar nombres a atributos y clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e042decaf7d3dd15606ea7e138d9e6315d4200f2a641c10381951f2657a5aafe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186015"
---
# <a name="naming-attributes-and-classes"></a>Asignar nombres a atributos y clases

En este tema se incluyen instrucciones para asignar nombres a atributos y clases.

Para crear una nueva clase o atributo, siga las siguientes reglas de nomenclatura:

-   Use el mismo nombre para las propiedades **cn** y **lDAPDisplayName** de un nuevo **objeto attributeSchema** **o classSchema.**
-   Identifique la empresa con un prefijo en minúsculas en la primera sección del nombre. Este prefijo puede ser un nombre DNS, un acrónimo u otra cadena que identifique de forma única a la empresa. El prefijo garantiza que todos los atributos y clases de una empresa específica se muestran consecutivamente al examinar el esquema.
-   Si va a desarrollar una extensión de esquema como proveedor de software independiente, agregue una abreviatura del nombre del producto del prefijo. Esto agrega distinción entre varios productos que contienen extensiones de esquema LDAP.
-   Use un guion como carácter siguiente después del prefijo.
-   Especifique un atributo o nombre de clase que sea único dentro de los atributos de la empresa después del guion. Esta parte del nombre común debe ser descriptiva. No use nombres ilegológicos que no tienen sentido para los desarrolladores y los visores del esquema.

Por ejemplo, si la empresa fabrikam ficticia extendió el esquema agregando un atributo para almacenar un identificador de correo de voz, **el cn** y **lDAPDisplayName** del nuevo atributo podrían ser "fabrikam-VoiceMailID".

Si no **se especifica lDAPDisplayName** de un atributo o clase, el sistema usa **el cn** para generar uno. Sin embargo, el algoritmo del sistema para generar el nombre puede provocar conflictos de nombres o nombres difíciles de leer. Para evitar estos problemas, se recomienda especificar explícitamente **lDAPDisplayName** para todos los atributos y clases.

Con fines de desarrollo y pruebas, puede ser conveniente anexar un sufijo de versión a **cn** y **lDAPDisplayName,** por ejemplo, "fabrikam-VoiceMailID-001". En un entorno de desarrollo y prueba distribuido, un sufijo de versión permite a los desarrolladores ejecutar varias versiones de su software simultáneamente. Una vez completadas las pruebas, cambie el nombre del atributo o la clase para quitar el sufijo.

No es posible eliminar las versiones en desuso de las extensiones de esquema, pero es posible deshabilitarlas y cambiarles el nombre con nombres desconocidos. Para obtener más información, [vea Deshabilitar clases y atributos existentes.](disabling-existing-classes-and-attributes.md)

 

 




