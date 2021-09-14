---
description: El tipo de datos Filename es una cadena de texto que contiene un nombre de archivo o una carpeta.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Nombre de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074781"
---
# <a name="filename"></a>Nombre de archivo

El tipo de datos Filename es una cadena de texto que contiene un nombre de archivo o una carpeta. De forma predeterminada, se supone que el nombre de archivo usa la sintaxis de nombre de archivo corto; es decir, nombre de ocho caracteres, punto (.) y extensión de 3 caracteres. Siempre se debe proporcionar un nombre de archivo corto porque se puede establecer la propiedad [**SHORTFILENAMES**](shortfilenames.md) o el volumen de destino para la instalación solo puede admitir nombres de archivo cortos.

Para incluir un nombre de archivo largo con el nombre de archivo corto, separelo del nombre de archivo corto con una barra vertical ( \| ).

Por ejemplo, las dos cadenas siguientes son válidas:

-   status.txt
-   projec~1.txt\| Project Status.txt

Los nombres de archivo cortos y largos no deben contener los caracteres siguientes:

-   barra diagonal (/) o ( \\ )
-   signo de interrogación (?)
-   barra vertical ( \| )
-   corchete angular derecho (>)
-   corchete angular izquierdo (<)
-   dos puntos (:)
-   asterisco ( \* )
-   comillas dobles (")

Además, los nombres de archivo cortos no deben contener los caracteres siguientes:

-   signo más (+)
-   coma (,)
-   punto y coma (;)
-   equals sign (=)
-   corchete izquierdo ( \[ )
-   corchete derecho ( \] )

No se permite ningún espacio antes del separador de barra vertical ( ) para la sintaxis de nombre de \| archivo corto/nombre de archivo largo. Es posible que los nombres de archivo cortos no incluyan un espacio, aunque es posible que un nombre de archivo largo. Solo puede existir un espacio después del separador si el nombre de archivo largo del nombre de archivo comienza por el espacio. No se permite ninguna sintaxis de ruta de acceso completa.

> [!Note]  
> El formato de la columna FileName de la tabla [MsiEmbeddedUI](msiembeddedui-table.md) es similar al tipo de datos filename, salvo que el separador de barra vertical ( ) para la sintaxis de nombre de archivo corto o nombre de archivo largo no \| está disponible.

 

 

 



