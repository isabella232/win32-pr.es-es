---
title: Recomendaciones aplicaciones de extensión de esquema
description: En este tema se incluyen recomendaciones para las aplicaciones de extensión de esquema.
ms.assetid: 615e927e-a113-4557-b354-55a208a649eb
ms.tgt_platform: multiple
keywords:
- Recomendaciones ad para aplicaciones de extensión de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0a01e68fbe9751b778caa2404d02afb1ddd7704457c9cf0aedcc914387ab5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025273"
---
# <a name="recommendations-for-schema-extension-applications"></a>Recomendaciones aplicaciones de extensión de esquema

Además de los requisitos previos, se recomiendan los siguientes procedimientos recomendados para las aplicaciones de extensión de esquema:

-   Busque el maestro de esquema. Enlace al esquema en el controlador de dominio que es el maestro de esquema. Evite cambiar innecesariamente el rol maestro de esquema entre los DCs. Para enlazar al contenedor de esquemas en el maestro de esquema. Para obtener más información, vea [Requisitos previos para instalar una extensión de esquema.](prerequisites-for-installing-a-schema-extension.md)
-   Antes de realizar cualquier acción, compruebe la **propiedad allowedChildClassesEffective** del contenedor de esquemas para comprobar que puede crear atributos o clases. Si **attributeSchema** y **classSchema** no son valores de esa propiedad, no tiene derechos suficientes para agregar atributos o clases al esquema. Para obtener más información, vea [Código de ejemplo para comprobar los derechos para crear objetos de esquema.](example-code-for-checking-for-rights-to-create-schema-objects.md)
-   Asegúrese de que la opción Actualización de esquema permitida esté establecida correctamente en el Registro del maestro de esquema. Para crear o establecer este valor, restáurelo a su estado original como parte de la rutina de limpieza de la aplicación. Para obtener más información sobre cómo comprobar y establecer este valor, vea [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).
-   Antes de agregar atributos o clases, asegúrese de que aún no existen. Si existen, compruebe que son los mismos atributos o clases que está agregando y no un atributo o clase creado por alguien con una sintaxis y propiedades diferentes que no son compatibles con sus atributos o clases.

    Para los atributos, consulte **cn**, **attributeID**, **governsID,** **lDAPDisplayName** y **schemaIDGUID** para asegurarse de que no se usan ya. Si agrega un conjunto de atributos vinculados (un vínculo hacia delante, un vínculo hacia atrás), asegúrese de que los **id.** de vínculo no se han usado todavía. Consulta de **governsID porque** el identificador de objeto (OID) debe ser único entre atributos y clases.

    Para las clases, consulte **cn**, **governsID**, **attributeID**, **lDAPDisplayName** y **schemaIDGUID** para asegurarse de que no se usan ya. Consulte **attributeID porque** el OID debe ser único entre clases y atributos.

    Para obtener más información sobre cómo comprobar las colisiones de nomenclatura, vea Código de ejemplo para detectar [conflictos de nomenclatura de esquemas.](example-code-for-detecting-schema-naming-collisions.md)

    Si existen atributos o clases que entren en conflicto con los nuevos atributos o clases, la aplicación no debe aplicar los cambios de esquema.

-   Si existe este tipo de colisión, la aplicación no debe aplicar los cambios de esquema. Es posible que el administrador del esquema tenga que resolver la colisión y, a continuación, volver a ejecutar la aplicación. Como alternativa, se **podría usar otro lDAPDisplayName;** sin embargo, cualquier aplicación que use el atributo u objeto debe tener en cuenta ese cambio. Para ayudar a evitar colisiones de OID, obtenga un OID de una autoridad de registro de nombres ISO.
-   Si la aplicación depende de los atributos o clases que ha agregado, actualice la caché de esquemas antes de agregar los nuevos atributos o clases que dependen de esos atributos o clases. Tenga en cuenta que el **atributo operativo schemaUpdateNow** es sincrónico. Es decir, la [**llamada al método IADs::P ut**](/windows/desktop/api/iads/nf-iads-iads-put) se bloqueará hasta que se actualice la caché de esquemas. Cuando se devuelve la llamada, se ha actualizado la caché de esquemas y se puede acceder a los nuevos atributos o clases.

    Para obtener más información sobre cómo actualizar la caché de esquemas, vea [Ejemplo de código para actualizar la caché de esquemas.](example-code-for-updating-the-schema-cache.md)

 

 