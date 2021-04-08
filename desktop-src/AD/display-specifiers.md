---
title: Especificadores de presentación
description: En Active Directory Domain Services, una clase de objeto o clase define un tipo de objeto que se puede crear en Active Directory Domain Services.
ms.assetid: 0c31b02b-9fd3-4547-9ebc-d511a10d7106
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be9df0b81427bafa6ebe6707a33e86b6aff7416
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995095"
---
# <a name="display-specifiers"></a>Especificadores de presentación

En Active Directory Domain Services, una clase de objeto o clase define un tipo de objeto que se puede crear en Active Directory Domain Services. La definición de cada clase de objeto se almacena como un objeto [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) en el [esquema de Active Directory](active-directory-schema.md). Además de la definición de **ClassSchema** , cada clase de objeto puede tener uno o varios especificadores de presentación que especifican los datos de la interfaz de usuario para los objetos de esa clase.

Un especificador de presentación es un objeto de la clase [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) . Los atributos de un objeto **displaySpecifier** especifican datos localizados de la interfaz de usuario que describen los distintos elementos de la interfaz de usuario para una clase de objeto determinada. Los especificadores de presentación almacenan datos de hojas de propiedades, menús contextuales, iconos, asistentes para crear y nombres de clase y atributo localizados. En el caso de las páginas de propiedades y los menús contextuales, el shell de Windows y Active Directory complementos administrativos usan estos datos para formar distintas interfaces de usuario para administradores y usuarios finales: un conjunto de páginas de propiedades y/o menús contextuales se pueden asociar a aplicaciones administrativas mientras que un conjunto diferente de elementos se puede asociar a las aplicaciones de usuario final.

Los objetos [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) se almacenan en contenedores específicos de la configuración regional en el contenedor DisplaySpecifiers del contenedor de configuración, que se replica en todos los controladores de dominio del bosque de la empresa. El contenedor DisplaySpecifiers tiene subcontenedores que corresponden a las distintas configuraciones regionales que admite la instalación de la empresa. Estos subcontenedores se denominan mediante identificadores de idioma. Por ejemplo, el nombre del contenedor de configuración regional para US-English es 409, que corresponde al identificador de idioma hexadecimal, 0x0409. Por lo tanto, una clase de objeto puede tener varios especificadores de pantalla: uno en cada subcontenedor de la configuración regional. Para obtener más información y una lista de los identificadores de idioma posibles, consulte [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings). Para obtener más información acerca de las configuraciones regionales, consulte [configuraciones regionales y idiomas](/windows/desktop/Intl/locales-and-languages).

El nombre de un objeto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) se forma anexando la cadena "-display" al [**lDAPDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) de la clase de objeto. Por ejemplo, el nombre de un objeto **displaySpecifier** para la clase de [**usuario**](/windows/desktop/ADSchema/c-user) es "user-Display".

Puede Agregar, eliminar o modificar las propiedades de los objetos [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) de una clase para especificar los elementos de la interfaz de usuario (nombre de clase, nombres de atributo, hojas de propiedades, menús contextuales, icono, etc.) que aparecen para cada instancia de un objeto de esa clase.

Para obtener más información sobre los especificadores de pantalla, vea [contenedor DisplaySpecifiers](displayspecifiers-container.md).

 

 