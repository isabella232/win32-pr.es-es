---
title: Asignar nombres a atributos y clases
description: En este tema se incluyen instrucciones para asignar nombres a los atributos y las clases.
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- Asignar nombres a atributos y clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "105656437"
---
# <a name="naming-attributes-and-classes"></a>Asignar nombres a atributos y clases

En este tema se incluyen instrucciones para asignar nombres a los atributos y las clases.

Para crear una nueva clase o atributo, cumpla las siguientes reglas de nomenclatura:

-   Use el mismo nombre para las propiedades **CN** y **lDAPDisplayName** de un nuevo objeto **attributeSchema** o **ClassSchema** .
-   Identifique la empresa con un prefijo en minúsculas en la primera sección del nombre. Este prefijo puede ser un nombre DNS, un acrónimo u otra cadena que identifique de forma única a la empresa. El prefijo garantiza que todos los atributos y las clases de una empresa específica se muestran de manera consecutiva al examinar el esquema.
-   Si está desarrollando una extensión de esquema como proveedor de software independiente, agregue una abreviatura del nombre de producto del prefijo. Esto agrega distinción entre varios productos que contienen extensiones de esquema LDAP.
-   Use un guión como el carácter siguiente después del prefijo.
-   Especifique un nombre de clase o atributo que sea único dentro de los atributos de la compañía después del guión. Esta parte de Common-Name debe ser descriptiva. No utilice nombres de illogical que no tengan sentido para los desarrolladores y visores del esquema.

Por ejemplo, si la compañía ficticia Fabrikam amplió el esquema agregando un atributo para almacenar un identificador de correo de voz, el **CN** y el **lDAPDisplayName** del nuevo atributo podrían ser "fabrikam-VoiceMailID".

Si no se especifica el **lDAPDisplayName** de un atributo o una clase, el sistema utiliza el **CN** para generar uno. Sin embargo, el algoritmo del sistema para generar el nombre puede dar lugar a conflictos de nombres o nombres difíciles de leer. Para evitar estos problemas, se recomienda especificar explícitamente un **lDAPDisplayName** para todos los atributos y clases.

Para fines de desarrollo y pruebas, puede ser conveniente anexar un sufijo de versión a los **CN** y **lDAPDisplayName**, por ejemplo, "fabrikam-VoiceMailID-001". En un entorno de desarrollo y pruebas distribuido, un sufijo de versión permite a los desarrolladores ejecutar varias versiones de su software simultáneamente. Una vez completadas las pruebas, cambie el nombre del atributo o de la clase para quitar el sufijo.

No es posible eliminar las versiones inactivas de las extensiones de esquema, pero es posible deshabilitarlas y cambiarlas por nombres más claros. Para obtener más información, vea [deshabilitar clases y atributos existentes](disabling-existing-classes-and-attributes.md).

 

 




