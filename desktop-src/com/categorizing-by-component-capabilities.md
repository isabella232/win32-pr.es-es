---
title: Categorización por funcionalidad de componentes
description: Las categorías de componentes se pueden usar para mostrar un subconjunto de todos los componentes instalados.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714143"
---
# <a name="categorizing-by-component-capabilities"></a>Categorización por funcionalidad de componentes

Las categorías de componentes se pueden usar para mostrar un subconjunto de todos los componentes instalados. Cada categoría de componente se identifica mediante un GUID, denominado ID. de categoría (CATId). Cada CATId tiene una lista de nombres legibles etiquetados por la configuración regional asociados a él. Una lista de los CATID y los nombres legibles se almacena en una ubicación conocida en el registro.

Por ejemplo, todos los componentes que implementan la funcionalidad para la incrustación de documentos OLE se pueden clasificar en una categoría de componente. En el pasado, estos objetos se identificaban con la clave "insertable" en el registro. Para utilizar las categorías de componentes en su lugar, se agregaría la siguiente información al registro:

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

Cada clase que implementa la funcionalidad correspondiente a una categoría de componente muestra el identificador de categoría de esa categoría dentro de la clave CLSID en el registro. Dado que un único componente puede admitir una amplia gama de funciones, los componentes pueden pertenecer a varias categorías de componentes. Por ejemplo, un control OLE determinado podría admitir toda la funcionalidad necesaria para participar como la incrustación de documentos OLE, el enlace de datos de Microsoft Visual Basic y la funcionalidad de Internet. Este tipo de control tendría la siguiente información almacenada en su clave CLSID en el registro:

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

Con esta información, un contenedor puede enumerar los controles instalados en un sistema y mostrar solo los controles que admiten la funcionalidad requerida por el contenedor. El uso de categorías de componentes proporciona una manera de clasificar los componentes por la funcionalidad implementada del componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asociar iconos a una categoría](associating-icons-with-a-category.md)
</dt> <dt>

[Clasificar por capacidades de contenedor](categorizing-by-container-capabilities.md)
</dt> <dt>

[Clases y asociaciones predeterminadas](default-classes-and-associations.md)
</dt> <dt>

[Definir categorías de componentes](defining-component-categories.md)
</dt> <dt>

[Administrador de categorías de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




