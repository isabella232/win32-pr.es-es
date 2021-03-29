---
title: Extensión de la interfaz de usuario para las nuevas clases de objeto
description: Active Directory Domain Services y su interfaz de usuario del complemento MMC administrativo pueden personalizarse para adaptarse a los requisitos de los administradores y los usuarios.
ms.assetid: 38e3b800-20ad-4da8-ad40-4e90838acfb5
ms.tgt_platform: multiple
keywords:
- Extensión de la interfaz de usuario para las nuevas clases de objeto AD
- Objeto AD, extensión de la interfaz de usuario para las nuevas clases de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154b64a23eff72bf5751085a8e50691cd222abd6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993885"
---
# <a name="user-interface-extension-for-new-object-classes"></a>Extensión de la interfaz de usuario para las nuevas clases de objeto

Active Directory Domain Services y su interfaz de usuario del complemento MMC administrativo pueden personalizarse para adaptarse a los requisitos de los administradores y los usuarios. Active Directory Domain Services habilitar el esquema para que se pueda modificar creando nuevas clases y atributos, o modificando las clases existentes. Los especificadores de presentación para las clases se pueden modificar para reflejar los nuevos elementos de la interfaz de usuario que requieren las modificaciones de esquema.

En la tabla siguiente se enumeran los atributos que se pueden usar para modificar la forma en que los complementos administrativos van a mostrar los objetos de una clase determinada.



| Atributo                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **defaultHidingValue**     | El atributo **defaultHidingValue** es un atributo de un objeto **ClassSchema** . Este atributo contiene un valor booleano que, si es TRUE, hace que las instancias de la clase de objeto se oculten en los complementos administrativos y en el shell de Windows. Esto también significa que un elemento de menú para la nueva clase de objeto no aparece en el menú **contextual de los** complementos administrativos, aunque las propiedades del Asistente para la creación correspondiente se establezcan en el objeto **displaySpecifier** de la nueva clase de objeto. Si este atributo es FALSE, las instancias de la clase serán visibles en los complementos administrativos y el shell. Esto también hace que un elemento de menú cree una nueva instancia de objeto que se va a agregar al **nuevo** menú de complementos administrativos.<br/> Si no se establece ningún valor para este atributo, el valor predeterminado es TRUE. Esto significa que, de forma predeterminada, las instancias del objeto están ocultas.<br/>                                                                |
| **showInAdvancedViewOnly** | El atributo **del showinadvancedviewonly** contiene un valor booleano que, si es true, hace que las instancias de la clase de objeto aparezcan en el complemento usuarios y equipos en la vista avanzada únicamente y no aparecen en el shell de Windows. Si esta propiedad es FALSE, las instancias de la clase serán visibles en la vista normal en el complemento usuarios y equipos y en el shell de Windows.<br/> Si no se establece ningún valor para este atributo, el valor predeterminado es TRUE.<br/> Este atributo se puede establecer en un objeto individual para reemplazar el valor establecido en la clase de objeto. Por ejemplo, la clase **contenedora** tiene este atributo establecido en true, pero el contenedor de **usuario** tiene este valor establecido en false. Por este motivo, el contenedor de **usuario** aparece en el Shell y en la vista normal del complemento usuarios y equipos, pero otros contenedores que no tienen **del SHOWINADVANCEDVIEWONLY** establecido en false solo aparecen en la vista avanzada del complemento usuarios y equipos.<br/> |



 

## <a name="creating-display-specifiers-for-new-classes"></a>Crear especificadores de presentación para clases nuevas

Para personalizar la interfaz de usuario para una nueva clase, cree un objeto de especificador de presentación para la nueva clase para cada configuración regional compatible y, a continuación, establezca los atributos deseados para el especificador de presentación.

## <a name="inheriting-display-specifiers-for-derived-classes"></a>Heredar especificadores de presentación para clases derivadas

Una nueva clase que hereda de una clase existente no hereda el especificador de presentación de la clase primaria. Si la nueva clase va a utilizar algunas o todas las propiedades del especificador de presentación de la clase primaria, cree un nuevo especificador de presentación para la nueva clase y copie las propiedades del especificador de presentación de la clase primaria en el especificador de presentación de objeto nuevo. Esto se debe hacer para todas las configuraciones regionales para las que se aplican las propiedades del especificador de presentación de la clase primaria.

Algunas partes del conjunto de características de la interfaz de usuario, como los elementos de menú y el Asistente para creación de la clase de usuario, se implementan internamente y no están disponibles para su uso por parte de un objeto derivado. En estos casos, es mejor extender una clase existente que usar una clase derivada.

## <a name="modifying-existing-classes"></a>Modificar clases existentes

Se pueden agregar nuevos atributos a una clase existente. Se pueden agregar nuevos componentes de interfaz de usuario (páginas de propiedades, elementos de menú y nombres para mostrar atributos) o reemplazar la interfaz de usuario existente. También es posible diseñar nuevas páginas de propiedades que expongan menos atributos de una clase y crear menús contextuales con menos acciones. Para obtener más información, vea [páginas de propiedades para su uso con especificadores de presentación](property-pages-for-use-with-display-specifiers.md), [menús contextuales para su uso con especificadores de presentación](context-menus-for-use-with-display-specifiers.md)y nombres para mostrar de [clases y atributos](class-and-attribute-display-names.md).

 

 





