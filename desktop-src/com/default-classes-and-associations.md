---
title: Clases y asociaciones predeterminadas
description: Para determinadas categorías, una sola clase puede asociarse como la clase predeterminada.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418374"
---
# <a name="default-classes-and-associations"></a>Clases y asociaciones predeterminadas

Para determinadas categorías, una sola clase puede asociarse como la clase predeterminada. La clase predeterminada se selecciona siempre que se requiera esa categoría determinada de objeto. Aunque puede que esto no sea útil para todas las categorías de componentes, el establecimiento de una clase predeterminada puede ser útil cuando se debe cargar una clase determinada de una lista de clases posibles sin la intervención del usuario. Los administradores definen la clase que se puede usar manipulando el registro.

Para asociar una clase predeterminada a una categoría, introduzca una clave CLSID con el mismo CLSID que el CATId de la categoría de componentes elegida como valor predeterminado. A continuación, agregue una clave treatAs a esta clave, utilizando el valor para el CLSID de la clase predeterminada de la categoría. Para usar la clase predeterminada para una categoría de componentes, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), especificando el CATID para el parámetro CLSID. Esto redirige automáticamente al CLSID establecido como valor predeterminado para esta categoría. La entrada del registro es la siguiente:

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

Durante la instalación, un componente puede comprobar la existencia de cualquier clave de clase predeterminada para sus categorías y presentar al usuario opciones para invalidar la configuración actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asociar iconos a una categoría](associating-icons-with-a-category.md)
</dt> <dt>

[Categorización por funcionalidad de componentes](categorizing-by-component-capabilities.md)
</dt> <dt>

[Clasificar por capacidades de contenedor](categorizing-by-container-capabilities.md)
</dt> <dt>

[Definir categorías de componentes](defining-component-categories.md)
</dt> <dt>

[Administrador de categorías de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




