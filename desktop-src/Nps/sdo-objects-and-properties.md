---
title: Objetos y propiedades
description: Las características de un objeto en SDO se determinan mediante las propiedades del objeto y los valores asociados a esas propiedades.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676429"
---
# <a name="objects-and-properties"></a>Objetos y propiedades

Las características de un objeto en SDO se determinan mediante las propiedades del objeto y los valores asociados a esas propiedades. A diferencia de otros modelos de objetos, los propios objetos SDO no tienen métodos. Sin embargo, los objetos SDO exponen interfaces COM que proporcionan métodos.

Los objetos de SDO exponen la interfaz [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) que proporciona métodos para manipular las propiedades de los objetos. Para obtener acceso a las propiedades del objeto, obtenga una interfaz **ISdo** para el objeto y use los métodos de la interfaz [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) y [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) para recuperar y establecer los valores de las propiedades. El tema [recuperar un SDO de usuarios](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contiene código de ejemplo que muestra cómo obtener la interfaz **ISdo** para un objeto de usuario.

Después de realizar cambios en las propiedades de un objeto, use el método [**ISdo:: Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) para escribir los cambios en el almacenamiento persistente para el objeto. Puede cancelar los cambios realizados en las propiedades de un objeto antes de llamar a **ISdo:: Apply** llamando al método [**ISdo:: restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) . Este método restaura los valores de las propiedades de un objeto desde el almacenamiento persistente.

En la tabla siguiente se muestran los tipos de enumeración que enumeran las propiedades de algunos de los objetos de SDO.



| Object                                 | Tipo de enumeración                                       |
|----------------------------------------|--------------------------------------------------------|
| Todos los objetos SDO                        | [**IASCOMMONPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| Objeto de usuario                            | [**USERPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| Objeto de servicio (servidor de directivas de redes) | [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| Objeto de protocolo RADIUS de Microsoft       | [**RADIUSPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.

 

## <a name="collections"></a>Colecciones

A menudo, los objetos se agrupan en colecciones. La API SDO proporciona funcionalidad, a través de la interfaz de [**colección ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) , para enumerar los objetos de una colección y para agregar y eliminar objetos de una colección.

El acceso a una colección se obtiene mediante la recuperación de una propiedad de colección en el objeto que contiene la colección. Para obtener más información, vea la sección [jerarquía del modelo de objetos](/windows/desktop/Nps/sdo-object-model-hierarchy).

El tipo de datos para todas las propiedades que se corresponden con las recopilaciones es VT \_ Dispatch.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Jerarquía del modelo de objetos SDO](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Atributos compatibles con SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 