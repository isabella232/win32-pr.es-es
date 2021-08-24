---
description: ICE94 comprueba la tabla de accesos directos, la tabla de características y la tabla MsiAssembly y envía una advertencia si hay accesos directos sin invertir que apuntan a un archivo de ensamblado en la caché global de ensamblados.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd203fe35b6bedc7d36f3e5a5c18fc6a235d3e65924b41909803e67ab79337e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894895"
---
# <a name="ice94"></a>ICE94

ICE94 comprueba la [](feature-table.md)tabla de accesos directos [,](shortcut-table.md)la tabla de características y la tabla [MsiAssembly](msiassembly-table.md) y envía una advertencia si hay accesos directos sin invertir que apuntan a un archivo de ensamblado en la caché global de ensamblados. Si la entrada del campo Destino de la tabla Acceso directo no es una característica de la tabla Característica, el acceso directo no se invierte. Si la entrada del campo Componente de la tabla Acceso directo también aparece en la tabla MsiAssembly, el acceso directo \_ apunta a un archivo de ensamblado. Si la entrada del campo Aplicación de archivo de la tabla MsiAssembly está vacía, el archivo \_ de ensamblado se encuentra en la caché global de ensamblados.

## <a name="result"></a>Resultado

ICE94 publica la advertencia siguiente.



| Advertencia de ICE94                                                                                | Descripción                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| El acceso directo no anunciado \[ '2' \] apunta a un archivo de ensamblado en la caché global de ensamblados. | Un acceso directo sin invertir apunta a un archivo de ensamblado en la caché global de ensamblados. |



 

## <a name="example"></a>Ejemplo

ICE94 notifica el siguiente error para el ejemplo:

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

[Tabla de métodos abreviados](shortcut-table.md) (parcial)



| Acceso directo  | Componente\_ | Destino    |
|-----------|-------------|-----------|
| shortcut1 | c1          | \[file1\] |
| shortcut2 | c2          | feature1  |
| shortcut3 | c3          | \[file2\] |



 

[Tabla de características](feature-table.md) (parcial)



| Característica  |
|----------|
| feature1 |



 

[Tabla MsiAssembly](msiassembly-table.md) (parcial)



| Componente\_ | Aplicación de \_ archivo |
|-------------|-------------------|
| c1          |                   |
| c2          |                   |
| c3          | fa1               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



