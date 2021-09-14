---
description: ICE02 valida que ciertas referencias entre las tablas Component, File y Registry son recíprocas. Estas referencias deben ser recíprocas para que el instalador determine correctamente el estado de instalación de los componentes.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074684"
---
# <a name="ice02"></a>ICE02

ICE02 valida que ciertas referencias entre las tablas [Component](component-table.md), [File](file-table.md)y [Registry](registry-table.md) son recíprocas. Estas referencias deben ser recíprocas para que el instalador determine correctamente el estado de instalación de los componentes.

El instalador usa la columna KeyPath de la tabla Component para detectar la presencia del componente enumerado en la columna Component. La columna KeyPath contiene una clave en las tablas Registry o File. Ambas tablas tienen una columna Component que contiene una clave en la tabla Component que apunta al componente que controla la entrada o el \_ archivo del Registro. Estas referencias deben ser recíprocas.

## <a name="result"></a>Resultado

ICE02 publica un mensaje de error si encuentra una referencia que debe ser recíproca y no es.

## <a name="example"></a>Ejemplo

ICE02 publicaría el siguiente mensaje de error para un archivo .msi que contiene las entradas de base de datos mostradas.

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

[Tabla de componentes](component-table.md) (parcial)



| Componente | KeyPath   |
|-----------|-----------|
| Rojo       | Archivo \_ rojo |
| Azul      | Archivo \_ rojo |



 

[Tabla de archivos](file-table.md) (parcial)



| Columna de archivo | Componente\_ |
|-------------|-------------|
| Archivo \_ rojo   | Rojo         |
| Archivo \_ azul  | Azul        |



 

Component Blue hace referencia a Red File, pero Red File no está controlado por Component Blue y, por \_ lo \_ tanto, no puede ser el archivo KeyPath. Si se llamó al instalador para obtener el estado de instalación azul, comprobaría incorrectamente si se instaló \_ el archivo rojo. Al cambiar el campo KeyPath de Azul en la tabla de componentes a Blue \_ File se corrige el error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



