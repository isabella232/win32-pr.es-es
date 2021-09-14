---
description: Contiene un objeto para cada propiedad del publicador transitorio para la colección TransientSubscriptions primaria. Las suscripciones transitorias se pueden crear sobre la marcha para ejecutar instancias de objeto y desaparecen cuando se destruye el objeto.
ms.assetid: 63921caa-5c22-4203-b1a3-f143928f4742
title: Colección TransientPublisherProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientPublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 707cb974dce632c6eb5f65bc38f1fff8b779e54d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361610"
---
# <a name="transientpublisherproperties-collection"></a>Colección TransientPublisherProperties

Contiene un objeto para cada propiedad del publicador transitorio para la colección [**TransientSubscriptions**](transientsubscriptions.md) primaria. Las suscripciones transitorias se pueden crear sobre la marcha para ejecutar instancias de objeto y desaparecen cuando se destruye el objeto.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Members

La **colección TransientPublisherProperties** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**TransientSubscriptions**](transientsubscriptions.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:

-   [Nombre](#name)
-   [Valor](#value)

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | El nombre de la propiedad. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Acceso         | WriteOnce                                                                                                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                                                                                                 |
| Predeterminado        | "Nueva propiedad"                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="value"></a>Value



| Entrada | Value |
|----------------|---------------------------|
| Descripción    | Valor de la propiedad . |
| Acceso         | ReadWrite                 |
| Tipo           | Variante                   |
| Valor predeterminado        | N/D                       |
| Sistema mínimo | Windows 2000              |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
