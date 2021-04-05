---
description: ICE67 comprueba que el destino de un acceso directo no anunciado pertenece al mismo componente que el propio acceso directo o que los atributos del componente de destino garantizan que no cambie las ubicaciones de instalación.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002698"
---
# <a name="ice67"></a>ICE67

ICE67 comprueba que el destino de un acceso directo no anunciado pertenece al mismo componente que el propio acceso directo o que los atributos del componente de destino garantizan que no cambie las ubicaciones de instalación.

Un error al corregir una advertencia o un error informados por ICE67 puede hacer que el acceso directo no sea válido si el componente de destino cambia de estado y el componente de origen no lo hace. Por ejemplo, cuando el componente del archivo de destino se establece en ejecutar desde el origen, una reinstalación que cambia el componente a resultados locales en el componente que contiene el acceso directo no se vuelve a instalar. Por lo tanto, el acceso directo apunta a una ubicación no válida.

Tenga en cuenta que en algunos casos, el uso de un componente diferente para el acceso directo es inevitable. Por ejemplo, si se crea el acceso directo en el perfil de usuario y el archivo se instala en un directorio que no es de perfil, es posible que no pueda usar el mismo componente para ambos fragmentos de datos. (Esto provoca errores en escenarios de varios usuarios, como los descritos en [ICE57](ice57.md)). En este caso, es posible que pueda usar accesos directos anunciados para lograr el comportamiento que desea, o simplemente puede asegurarse de que el componente de destino no puede cambiar de ejecutar desde el origen a local.

## <a name="result"></a>Resultado

ICE67 devuelve un error o una advertencia si el destino de un acceso directo no anunciado no pertenece al mismo componente que el propio método abreviado, o si los atributos del componente de destino no se aseguran de que las ubicaciones de instalación no cambien.

## <a name="example"></a>Ejemplo

ICE67 notifica los siguientes errores y advertencias para el ejemplo que se muestra.

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

Shortcut1 instala Component2, pero Component1 instala su archivo de destino, archivo1. El componente de destino está marcado como opcional (lo que significa que puede ser local o ejecutar desde el origen). Una posible situación que podría provocar un problema es que Component1 cambie de ejecutar desde el origen a local. Esto haría que Shortcut1 apuntara a una ubicación no válida.

Para corregir esta advertencia, instale el acceso directo como parte de Component1 o marque Component1 como LocalOnly o SourceOnly.

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ |
|-------|-------------|
| Archivo1 | Component1  |



 

[Tabla de acceso directo](shortcut-table.md) (parcial)



| Acceso directo  | Componente\_ | Destino      |
|-----------|-------------|-------------|
| Shortcut1 | Component2  | \[\#Archivo1\] |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Atributos |
|------------|------------|
| Component1 | 2          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



