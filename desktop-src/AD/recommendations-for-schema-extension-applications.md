---
title: Recomendaciones para las aplicaciones de extensión de esquema
description: En este tema se incluyen las recomendaciones para las aplicaciones de extensión de esquema.
ms.assetid: 615e927e-a113-4557-b354-55a208a649eb
ms.tgt_platform: multiple
keywords:
- Recomendaciones para aplicaciones de extensión de esquema AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2393211eb910ce4bc490667398da7f38d212ddcf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149168"
---
# <a name="recommendations-for-schema-extension-applications"></a>Recomendaciones para las aplicaciones de extensión de esquema

Además de los requisitos previos, se recomiendan los siguientes procedimientos recomendados para las aplicaciones de extensión de esquema:

-   Busque el maestro de esquema. Enlace al esquema en el controlador de dominio que es el maestro de esquema. Evite cambiar innecesariamente el rol de maestro de esquema entre controladores de DC. Para enlazar con el contenedor de esquema en el maestro de esquema. Para obtener más información, consulte [requisitos previos para la instalación de una extensión de esquema](prerequisites-for-installing-a-schema-extension.md).
-   Antes de realizar cualquier acción, Compruebe la propiedad **allowedChildClassesEffective** del contenedor de esquemas para comprobar que puede crear atributos y/o clases. Si **attributeSchema** y **ClassSchema** no son valores de esa propiedad, no tiene derechos suficientes para agregar atributos o clases al esquema. Para obtener más información, consulte el [código de ejemplo para comprobar los derechos para crear objetos de esquema](example-code-for-checking-for-rights-to-create-schema-objects.md).
-   Asegúrese de que la actualización de esquema permitida esté establecida correctamente en el registro del maestro de esquema. Para crear o establecer este valor, restáurelo a su estado original como parte de la rutina de limpieza de la aplicación. Para obtener más información acerca de cómo comprobar y establecer este valor, vea [habilitar los cambios de esquema en el maestro de esquema](enabling-schema-changes-at-the-schema-master.md).
-   Antes de agregar atributos o clases, asegúrese de que aún no existen. Si existen, compruebe que son los mismos atributos o clases que está agregando, y no un atributo o clase creados por un usuario con diferentes sintaxis y propiedades que no son compatibles con sus atributos o clases.

    En el caso de los atributos, consulte **CN**, **attributeID**, **governsID**, **lDAPDisplayName** y **schemaIDGUID** para asegurarse de que aún no se usan. Si agrega un conjunto de atributos vinculados (un vínculo hacia delante, uno hacia atrás), asegúrese de que no se hayan utilizado los **LinkId** s. Consulta para **governsID** porque el identificador de objeto (OID) debe ser único entre los atributos y las clases.

    En el caso de las clases, consulte **CN**, **governsID**, **attributeID**, **lDAPDisplayName** y **schemaIDGUID** para asegurarse de que aún no se usan. Busque **attributeID** porque el OID debe ser único entre las clases y los atributos.

    Para obtener más información sobre la comprobación de conflictos de nomenclatura, vea [código de ejemplo para detectar colisiones de nomenclatura de esquemas](example-code-for-detecting-schema-naming-collisions.md).

    Si existen atributos o clases que entran en conflicto con los nuevos atributos o clases, la aplicación no debe aplicar los cambios de esquema.

-   Si existe una colisión, la aplicación no debe aplicar los cambios de esquema. Es posible que el administrador de esquema tenga que resolver la colisión y volver a ejecutar la aplicación. Como alternativa, se podría usar un **lDAPDisplayName** diferente. sin embargo, las aplicaciones que utilicen el atributo o el objeto deben tener en cuenta ese cambio. Para ayudar a evitar colisiones de OID, obtenga un OID de una entidad de registro de nombres ISO.
-   Si su aplicación depende de atributos o clases que ha agregado, actualice la caché de esquema antes de agregar los nuevos atributos o clases que dependen de esos atributos o clases. Tenga en cuenta que el atributo operativo **schemaUpdateNow** es sincrónico. Es decir, la llamada al método [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) se bloqueará hasta que se actualice la memoria caché del esquema. Cuando se devuelve la llamada, la memoria caché de esquema se ha actualizado y se puede tener acceso a los nuevos atributos o clases.

    Para obtener más información sobre cómo actualizar la caché de esquemas, vea [código de ejemplo para actualizar la caché de esquema](example-code-for-updating-the-schema-cache.md).

 

 