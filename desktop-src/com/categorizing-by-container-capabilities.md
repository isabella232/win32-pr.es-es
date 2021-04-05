---
title: Clasificar por capacidades de contenedor
description: A menudo, los componentes requieren cierta funcionalidad del contenedor y no funcionarán con un contenedor que no proporcione la compatibilidad.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076290"
---
# <a name="categorizing-by-container-capabilities"></a>Clasificar por capacidades de contenedor

A menudo, los componentes requieren cierta funcionalidad del contenedor y no funcionarán con un contenedor que no proporcione la compatibilidad. La interfaz de usuario debe filtrar los componentes que requieren funcionalidad que el contenedor no admite. Para ello, los componentes se pueden clasificar por la funcionalidad de contenedor requerida.

Un ejemplo de componentes que requieren funcionalidad del contenedor y que no funcionan en contenedores que no admiten esa funcionalidad son controles OLE de marco sencillos. La categorización por funciones de contenedor se realiza mediante una clave del registro adicional dentro de la clave CLSID del componente:

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

Como se muestra en este ejemplo, un componente puede pertenecer a categorías de componentes que indican la funcionalidad admitida, así como a las categorías de componentes que indican la funcionalidad requerida.

En el ejemplo siguiente, el control de botón es un control OLE genérico que no admite ninguna funcionalidad adicional. Funcionará en cualquier contenedor de controles OLE.

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

Compare el ejemplo anterior con el siguiente ejemplo en el que MyDBControl puede usar Visual Basic enlace de datos si el contenedor lo admite. Sin embargo, se ha definido para que funcione en contenedores que no admiten el enlace de datos de Visual Basic (quizás por otra API de base de datos):

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

El control GroupBox es un control Frame simple. Se basa en el contenedor que implementa la interfaz [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) y funcionará correctamente solo en estos contenedores:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

Un contenedor que admite Visual Basic controles enlazados a datos pero no admite controles de fotogramas simples especificaría \_ el control CATID y CATID \_ VBDatabound en la interfaz de usuario del control de inserción. La lista de controles que se muestran al usuario contiene el \_ botón CLSID y el CLSID \_ MyDBControl. \_No se mostraría el GroupBox de CLSID.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asociar iconos a una categoría](associating-icons-with-a-category.md)
</dt> <dt>

[Categorización por funcionalidad de componentes](categorizing-by-component-capabilities.md)
</dt> <dt>

[Clases y asociaciones predeterminadas](default-classes-and-associations.md)
</dt> <dt>

[Definir categorías de componentes](defining-component-categories.md)
</dt> <dt>

[Administrador de categorías de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




