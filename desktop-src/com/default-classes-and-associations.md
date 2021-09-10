---
title: Clases y asociaciones predeterminadas
description: Para determinadas categorías, una sola clase se puede asociar como clase predeterminada.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369688"
---
# <a name="default-classes-and-associations"></a>Clases y asociaciones predeterminadas

Para determinadas categorías, una sola clase se puede asociar como clase predeterminada. La clase predeterminada se selecciona cada vez que se requiere esa categoría concreta de objeto. Aunque esto puede no ser útil para todas las categorías de componentes, establecer una clase predeterminada puede ser útil cuando una clase determinada debe cargarse desde una lista de clases posibles sin la intervención del usuario. Los administradores definen qué clase se puede usar mediante la manipulación del registro.

Para asociar una clase predeterminada a una categoría, introduzca una clave CLSID con el mismo CLSID que el CATID de la categoría de componentes elegida como valor predeterminado. A continuación, agregue una clave TreatAs a esta clave, utilizando el valor para el CLSID de la clase predeterminada para la categoría. Para usar la clase predeterminada para una categoría de componente, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), especificando el CATID para el parámetro CLSID. Esto redirige automáticamente al CLSID establecido como valor predeterminado para esta categoría. La entrada del Registro es la siguiente:

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

Durante la instalación, un componente puede comprobar la existencia de cualquier clave de clase predeterminada para sus categorías y presentar al usuario opciones para invalidar la configuración actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asociación de iconos a una categoría](associating-icons-with-a-category.md)
</dt> <dt>

[Categorización por funcionalidades de componentes](categorizing-by-component-capabilities.md)
</dt> <dt>

[Categorización por funcionalidades de contenedor](categorizing-by-container-capabilities.md)
</dt> <dt>

[Definir categorías de componentes](defining-component-categories.md)
</dt> <dt>

[Administrador de categorías de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




