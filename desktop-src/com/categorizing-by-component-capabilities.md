---
title: Categorización por funcionalidades de componentes
description: Las categorías de componentes se pueden usar para mostrar un subconjunto de todos los componentes instalados.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251e8197c00a39c8d9666dee7122be7445402fc84ce7b3508987bcf79f27df15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048753"
---
# <a name="categorizing-by-component-capabilities"></a>Categorización por funcionalidades de componentes

Las categorías de componentes se pueden usar para mostrar un subconjunto de todos los componentes instalados. Cada categoría de componente se identifica mediante un GUID, denominado identificador de categoría (CATID). Cada CATID tiene una lista de nombres legibles y etiquetados con configuración regional asociados. Una lista de los CATID y los nombres legibles se almacena en una ubicación conocida del registro.

Por ejemplo, todos los componentes que implementan la funcionalidad para la inserción de documentos OLE se pueden clasificar dentro de una categoría de componentes. En el pasado, estos objetos se habrían identificado mediante la clave "Insertable" en el Registro. Para usar categorías de componentes en su lugar, se agregaría la siguiente información al Registro:

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

Cada clase que implementa la funcionalidad correspondiente a una categoría de componente muestra el identificador de categoría de esa categoría dentro de la clave CLSID del Registro. Dado que un único componente puede admitir una amplia gama de funcionalidades, los componentes pueden pertenecer a varias categorías de componentes. Por ejemplo, un control OLE determinado podría admitir toda la funcionalidad necesaria para participar como inserción de documentos OLE, enlace de datos de Microsoft Visual Basic y funcionalidad de Internet. Este control tendría la siguiente información almacenada en su clave CLSID en el Registro:

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

Con esta información, un contenedor puede enumerar los controles instalados en un sistema y mostrar solo los controles que admiten la funcionalidad requerida por el contenedor. El uso de categorías de componentes proporciona una manera de clasificar los componentes por la funcionalidad implementada del componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asociación de iconos a una categoría](associating-icons-with-a-category.md)
</dt> <dt>

[Categorización por funcionalidades de contenedor](categorizing-by-container-capabilities.md)
</dt> <dt>

[Clases y asociaciones predeterminadas](default-classes-and-associations.md)
</dt> <dt>

[Definir categorías de componentes](defining-component-categories.md)
</dt> <dt>

[Administrador de categorías de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




