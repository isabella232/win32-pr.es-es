---
description: ICE64 comprueba que los directorios nuevos del perfil de usuario se quitan correctamente en escenarios de itinerancia.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074564"
---
# <a name="ice64"></a>ICE64

ICE64 comprueba que los directorios nuevos del perfil de usuario se quitan correctamente en escenarios de itinerancia.

Por lo general, si no se corrige una advertencia o un error notificado por ICE64, se producirán problemas en la limpieza completa del equipo durante una desinstalación. Cuando un usuario móvil que ha instalado la aplicación inicia sesión en un equipo por primera vez, todo el perfil se copia en el equipo. En el anuncio (que tiene lugar después de la descarga del perfil móvil), el instalador comprueba que el directorio ya está allí y, por tanto, no lo elimina al desinstalarlo. Esto deja el directorio en el equipo del usuario de forma permanente.

## <a name="result"></a>Resultado

ICE64 envía una advertencia o un error en una situación de itinerancia si no se quita un nuevo directorio en el perfil de usuario que se debe quitar.

## <a name="example"></a>Ejemplo

ICE64 notifica el siguiente error para el ejemplo mostrado.

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

La carpeta "MyOtherFolder" es una carpeta de perfil personalizada. Dado que no aparece en la tabla RemoveFile, no se quita en algunos escenarios.

Para corregir este error, cree una fila para la carpeta en la tabla RemoveFile.

[Tabla de directorios](directory-table.md)



| Directorio     | Elemento primario \_ del directorio | DefaultDir  |
|---------------|-------------------|-------------|
| AppDataFolder | TARGETDIR         |             |
| MyFolder      | AppDataFolder     | DataFolder  |
| MyOtherFolder | AppDataFolder     | DataFolder2 |



 

[Tabla RemoveFile](removefile-table.md)



| FileKey | Componente\_ | FileName | DirProperty | InstallMode |
|---------|-------------|----------|-------------|-------------|
| Tecla1    | Componente1  |          | MyFolder    | 2           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



