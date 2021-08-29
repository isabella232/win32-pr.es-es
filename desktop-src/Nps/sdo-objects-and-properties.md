---
title: Objetos y propiedades
description: Las características de un objeto en SDO se determinan mediante las propiedades del objeto y los valores asociados a esas propiedades.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbf871f6aa1e36c3d93eb93853660d0aa9b083d89f4030446fedd8c883530694
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128625"
---
# <a name="objects-and-properties"></a>Objetos y propiedades

Las características de un objeto en SDO se determinan mediante las propiedades del objeto y los valores asociados a esas propiedades. A diferencia de otros modelos de objetos, los propios objetos SDO no tienen métodos. Sin embargo, los objetos SDO exponen interfaces COM que proporcionan métodos.

Los objetos de SDO exponen la [**interfaz ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) que proporciona métodos para manipular las propiedades de los objetos. Para acceder a las propiedades del objeto, obtenga una interfaz **ISdo** para el objeto y use los métodos de interfaz [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) y [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) para recuperar y establecer valores para las propiedades. El tema [Recuperación de un SDO de](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) usuario contiene código de ejemplo que muestra cómo obtener la **interfaz ISdo** para un objeto User.

Después de realizar cambios en las propiedades de un objeto, use el método [**ISdo::Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) para escribir los cambios en el almacenamiento persistente del objeto. Puede cancelar los cambios realizados en las propiedades de un objeto antes de llamar a **ISdo::Apply** llamando al [**método ISdo::Restore.**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) Este método restaura los valores de las propiedades de un objeto desde el almacenamiento persistente.

En la tabla siguiente se muestran los tipos de enumeración que enumeran las propiedades de algunos de los objetos de SDO.



| Object                                 | Tipo de enumeración                                       |
|----------------------------------------|--------------------------------------------------------|
| Todos los objetos SDO                        | [**IASCOMMONPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| Objeto User                            | [**Userproperties**](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| Objeto de servicio (servidor de directivas de red) | [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| Objeto de protocolo RADIUS de Microsoft       | [**RADIUSPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS) a partir Windows Server 2008.

 

## <a name="collections"></a>Colecciones

Los objetos a menudo se agrupan en colecciones. La API de SDO proporciona funcionalidad, a través de la interfaz [**colección de ISdo,**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) para enumerar los objetos de una colección y para agregar y eliminar objetos de una colección.

El acceso a una colección se obtiene recuperando una propiedad de colección en el objeto que contiene la colección. Para obtener más información, vea la sección [Jerarquía del modelo de objetos](/windows/desktop/Nps/sdo-object-model-hierarchy).

El tipo de datos de todas las propiedades que corresponden a colecciones es VT \_ DISPATCH.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Jerarquía del modelo de objetos SDO](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Atributos admitidos por SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 