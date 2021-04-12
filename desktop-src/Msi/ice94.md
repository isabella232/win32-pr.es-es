---
description: ICE94 comprueba la tabla de acceso directo, la tabla de características y la tabla MsiAssembly y publica una advertencia si hay accesos directos no anunciados que señalan a un archivo de ensamblado en la caché global de ensamblados.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278457"
---
# <a name="ice94"></a>ICE94

ICE94 comprueba la tabla de [acceso directo](shortcut-table.md), la [tabla de características](feature-table.md)y la [tabla MsiAssembly](msiassembly-table.md) y publica una advertencia si hay accesos directos no anunciados que señalan a un archivo de ensamblado en la caché global de ensamblados. Si la entrada en el campo de destino de la tabla de acceso directo no es una característica de la tabla de características, el acceso directo no se anuncia. Si la entrada en el \_ campo componente de la tabla de acceso directo también aparece en la tabla MsiAssembly, el acceso directo apunta a un archivo de ensamblado. Si la entrada del campo de la \_ aplicación de archivo en la tabla MsiAssembly está vacía, el archivo de ensamblado se encuentra en la caché global de ensamblados.

## <a name="result"></a>Resultado

ICE94 envía la siguiente advertencia.



| ADVERTENCIA de ICE94                                                                                | Descripción                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| El acceso directo no anunciado ' \[ 2 \] ' apunta a un archivo de ensamblado en la caché global de ensamblados. | Un acceso directo no anunciado apunta a un archivo de ensamblado en la caché global de ensamblados. |



 

## <a name="example"></a>Ejemplo

ICE94 notifica el siguiente error para el ejemplo:

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

[Tabla de acceso directo](shortcut-table.md) (parcial)



| Acceso directo  | Componente\_ | Destino    |
|-----------|-------------|-----------|
| shortcut1 | c1          | \[archivo1\] |
| shortcut2 | c2          | Feature1  |
| shortcut3 | c3          | \[archivo2\] |



 

[Tabla de características](feature-table.md) (parcial)



| Característica  |
|----------|
| Feature1 |



 

[Tabla MsiAssembly](msiassembly-table.md) (parcial)



| Componente\_ | Aplicación de archivo \_ |
|-------------|-------------------|
| c1          |                   |
| c2          |                   |
| c3          | fa1               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



