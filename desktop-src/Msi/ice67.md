---
description: ICE67 comprueba que el destino de un acceso directo no anunciado pertenece al mismo componente que el propio acceso directo, o que los atributos del componente de destino garantizan que no cambia las ubicaciones de instalación.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074557"
---
# <a name="ice67"></a>ICE67

ICE67 comprueba que el destino de un acceso directo no anunciado pertenece al mismo componente que el propio acceso directo, o que los atributos del componente de destino garantizan que no cambia las ubicaciones de instalación.

Si no se corrige una advertencia o un error notificados por ICE67, el acceso directo no será válido si el componente de destino cambia de estado y el componente de origen no lo hace. Por ejemplo, cuando el componente del archivo de destino se establece para ejecutarse desde el origen, una reinstalación que cambia el componente a local da como resultado que el componente que contiene el acceso directo no se vuelva a instalar. Por lo tanto, el acceso directo apunta a una ubicación no válida.

Tenga en cuenta que, en algunos casos, el uso de un componente diferente para el acceso directo es inevitable. Por ejemplo, si el acceso directo se crea en el perfil de usuario y el archivo se instala en un directorio que no es de perfil, es posible que no pueda usar el mismo componente para ambos fragmentos de datos. (Esto produce errores en escenarios de varios usuarios, como los descritos en [ICE57).](ice57.md) En este caso, es posible que pueda usar accesos directos anunciados para lograr el comportamiento deseado, o simplemente puede asegurarse de que el componente de destino no puede cambiar de run-from-source a local.

## <a name="result"></a>Resultado

ICE67 devuelve un error o una advertencia si el destino de un acceso directo no anunciado no pertenece al mismo componente que el propio acceso directo, o si los atributos del componente de destino no garantizan que las ubicaciones de instalación no cambien.

## <a name="example"></a>Ejemplo

ICE67 notifica la advertencia y los errores siguientes para el ejemplo mostrado.

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

Component2 instala Shortcut1, pero component1 instala su archivo de destino, File1. El componente de destino se marca como opcional (lo que significa que puede ser local o ejecutar desde el origen). Una posible situación que provocaría un problema es si Component1 cambia de run-from-source a local. Esto haría que Shortcut1 apuntara a una ubicación no válida.

Para corregir esta advertencia, instale el acceso directo como parte de Component1 o marque Component1 como LocalOnly o SourceOnly.

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ |
|-------|-------------|
| Archivo1 | Componente1  |



 

[Tabla de métodos abreviados](shortcut-table.md) (parcial)



| Acceso directo  | Componente\_ | Destino      |
|-----------|-------------|-------------|
| Acceso directo1 | Componente 2  | \[\#Archivo1\] |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Atributos |
|------------|------------|
| Componente1 | 2          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



