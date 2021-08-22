---
description: ICE02 valida que ciertas referencias entre las tablas Component, File y Registry sean recíprocos. Estas referencias deben ser recíproco para que el instalador determine correctamente el estado de instalación de los componentes.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b97696ee4a8f93d49237dbac8661b6bfc72e478922c87b9095620bc5c29dc546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946659"
---
# <a name="ice02"></a>ICE02

ICE02 valida que ciertas referencias entre las tablas [Component](component-table.md), [File](file-table.md) [y Registry](registry-table.md) son recíprocos. Estas referencias deben ser recíproco para que el instalador determine correctamente el estado de instalación de los componentes.

El instalador usa la columna KeyPath de la tabla Component para detectar la presencia del componente que aparece en la columna Component. La columna KeyPath contiene una clave en las tablas Registry o File. Ambas tablas tienen una columna Component que contiene una clave en la tabla Component que apunta al componente que controla la entrada o el archivo \_ del Registro. Estas referencias deben ser recíproco.

## <a name="result"></a>Resultado

ICE02 publica un mensaje de error si encuentra una referencia que debe ser recíproco y no lo es.

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



 

Component Blue hace referencia al archivo rojo, pero el archivo rojo no está controlado por component blue y, por lo \_ \_ tanto, no puede ser el archivo KeyPath. Si se llamó al instalador para obtener el estado de instalación azul, comprobaría incorrectamente si se \_ instaló el archivo rojo. Al cambiar el campo KeyPath de Azul de la tabla de componentes a Blue \_ File se corrige el error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



