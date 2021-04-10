---
title: Asociar iconos a una categoría
description: Asociar iconos a una categoría
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c7a662ab3aaf578f037ff246207d03e4fcd688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075249"
---
# <a name="associating-icons-with-a-category"></a>Asociar iconos a una categoría

La creación de una interfaz de usuario que permita al usuario seleccionar categorías de componentes dentro de una categoría requiere la posibilidad de mostrar una imagen significativa para una categoría determinada. Para asociar un icono a una categoría de componente, cree una clave para el CATId de la categoría y rellene esa clave con una subclave [DefaultIcon](defaulticon.md) . La entrada del registro es la siguiente:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

El nombre de archivo al que hace referencia la clave DefaultIcon puede ser un archivo EXE o un archivo DLL (DLL de solo recursos).

Para asociar un pequeño mapa de bits del cuadro de herramientas de 16x16 con una categoría de componente, cree una clave en **HKEY \_ clases \_ raíz \\ CLSID** para el CATID de la categoría y rellene esa clave con una subclave [ToolBoxBitmap32](toolboxbitmap32.md) , como se muestra en el ejemplo siguiente:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

El nombre de archivo al que hace referencia la clave [ToolBoxBitmap32](toolboxbitmap32.md) también puede ser un archivo exe o DLL (dll de solo recursos).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorización por funcionalidad de componentes](categorizing-by-component-capabilities.md)
</dt> <dt>

[Clasificar por capacidades de contenedor](categorizing-by-container-capabilities.md)
</dt> <dt>

[Clases y asociaciones predeterminadas](default-classes-and-associations.md)
</dt> <dt>

[Definir categorías de componentes](defining-component-categories.md)
</dt> <dt>

[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[Administrador de categorías de componentes](the-component-categories-manager.md)
</dt> </dl>

 

 




