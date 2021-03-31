---
description: ICE02 valida que ciertas referencias entre el componente, el archivo y las tablas del registro sean recíprocas. Estas referencias deben ser recíprocas para que el instalador determine correctamente el estado de instalación de los componentes.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808750"
---
# <a name="ice02"></a>ICE02

ICE02 valida que ciertas referencias entre el [componente](component-table.md), el [archivo](file-table.md)y las tablas [del registro](registry-table.md) sean recíprocas. Estas referencias deben ser recíprocas para que el instalador determine correctamente el estado de instalación de los componentes.

El instalador usa la columna de ruta de la tabla de componentes para detectar la presencia del componente que aparece en la columna componente. La columna de ruta de acceso contiene una clave en las tablas del registro o del archivo. Ambas tablas tienen una \_ columna componente que contiene una clave de nuevo en la tabla componente que apunta al componente que controla la entrada o el archivo del registro. Estas referencias deben ser recíprocas.

## <a name="result"></a>Resultado

ICE02 envía un mensaje de error si encuentra una referencia que debe ser recíproca y no es.

## <a name="example"></a>Ejemplo

ICE02 publicaría el siguiente mensaje de error para un archivo. msi que contiene las entradas de base de datos que se muestran.

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

[Tabla de componentes](component-table.md) (parcial)



| Componente | Rutas   |
|-----------|-----------|
| Rojo       | \_Archivo rojo |
| Azul      | \_Archivo rojo |



 

[Tabla de archivos](file-table.md) (parcial)



| Columna de archivo | Componente\_ |
|-------------|-------------|
| \_Archivo rojo   | Rojo         |
| \_Archivo azul  | Azul        |



 

El componente azul hace referencia \_ al archivo rojo, pero \_ el archivo rojo no está controlado por el componente azul y, por lo tanto, no puede ser el archivo de ruta de acceso. Si se llamó al instalador para obtener el estado de instalación azul, comprobará incorrectamente si \_ se instaló el archivo rojo. Si cambia el campo de ruta de la ruta de acceso azul en la tabla de componentes al archivo azul, se \_ corregirá el error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



