---
description: ICE64 comprueba que los nuevos directorios del perfil de usuario se han quitado correctamente en escenarios móviles.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546139"
---
# <a name="ice64"></a>ICE64

ICE64 comprueba que los nuevos directorios del perfil de usuario se han quitado correctamente en escenarios móviles.

Si no se corrige una advertencia o un error informados por ICE64, generalmente se producen problemas al limpiar completamente el equipo durante una desinstalación. Cuando un usuario móvil que ha instalado la aplicación inicia sesión en un equipo por primera vez, se copia todo el perfil en el equipo. En el anuncio (que tiene lugar después de la descarga del perfil móvil), el instalador comprueba que el directorio ya existe y, por tanto, no lo elimina durante la desinstalación. Esto deja el directorio en el equipo del usuario de forma permanente.

## <a name="result"></a>Resultado

ICE64 envía una advertencia o un error en una situación de itinerancia si no se quita un nuevo directorio del perfil de usuario que se debe quitar.

## <a name="example"></a>Ejemplo

ICE64 notifica el siguiente error para el ejemplo que se muestra.

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

La carpeta ' MyOtherFolder ' es una carpeta de perfil personalizada. Dado que no aparece en la tabla RemoveFile, no se quita en algunos escenarios.

Para corregir este error, cree una fila para la carpeta en la tabla RemoveFile.

[Tabla de directorio](directory-table.md)



| Directorio     | Directorio \_ primario | DefaultDir  |
|---------------|-------------------|-------------|
| AppDataFolder | TARGETDIR         |             |
| MyFolder      | AppDataFolder     | Subcarpeta  |
| MyOtherFolder | AppDataFolder     | DataFolder2 |



 

[Tabla RemoveFile](removefile-table.md)



| FileKey | Componente\_ | FileName | DirProperty | InstallMode |
|---------|-------------|----------|-------------|-------------|
| Tecla1    | Component1  |          | MyFolder    | 2           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



