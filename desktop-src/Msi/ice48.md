---
description: ICE48 comprueba si hay directorios codificados de forma hard-code a rutas de acceso locales en la tabla Property.
ms.assetid: 9dcc2475-23a3-4f77-8828-4d0a036670d4
title: ICE48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c9c9ace086d044109e5f9b91bbc471c37094de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074596"
---
# <a name="ice48"></a>ICE48

ICE48 comprueba si hay directorios codificados de forma hard-code a rutas de acceso locales en la [tabla Property](property-table.md).

No codifie las rutas de acceso de directorio a las unidades locales porque los equipos difieren en la configuración de la unidad local. Esta práctica puede ser aceptable si se implementa una aplicación en un gran número de equipos en los que las partes pertinentes de las unidades son iguales.

## <a name="result"></a>Resultado

ICE48 envía un mensaje de error si hay un directorio codificado de forma hard-code a una ruta de acceso local en la tabla Property.

## <a name="example"></a>Ejemplo

ICE48 notificaría la siguiente advertencia para el ejemplo mostrado.

``` syntax
Directory 'Dir1' appears to be hardcoded in the property 
    table to a local drive.
```

[Tabla de directorios](directory-table.md) (parcial)



| Directorio | Elemento primario \_ del directorio | DefaultDir |
|-----------|-------------------|------------|
| Dir1      |                   | SourceDir  |



 

[Tabla de propiedades](property-table.md) (parcial)



| Propiedad. | Value      |
|----------|------------|
| Dir1     | d: \\ source |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



