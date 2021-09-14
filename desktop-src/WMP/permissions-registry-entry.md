---
title: Entrada del Registro de permisos
description: Entrada del Registro de permisos
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Reproductor de Windows Media,extensiones de nombre de archivo
- Reproductor de Windows Media,permissions
- Reproductor de Windows Media,registry
- registry,file name extensions
- registry,permissions
- registry,settings for Reproductor de Windows Media
- configuración del Registro de extensión de nombre de archivo
- permisos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242504"
---
# <a name="permissions-registry-entry"></a>Entrada del Registro de permisos

Cuando Reproductor de Windows Media encuentra una extensión de nombre de archivo personalizada, busca una subclave del Registro que coincida con la extensión. La subclave se describe en [File Name Extension Registry Configuración](file-name-extension-registry-settings.md). Una de las entradas del Registro que pueden aparecer bajo la subclave de la extensión es la **entrada Permisos.**

La **entrada Permisos** especifica las acciones que Reproductor de Windows Media puede realizar en los archivos que tienen la extensión personalizada. La **entrada Permisos** tiene el siguiente formulario.



| Nombre        | Tipo           | Value                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| Permisos | **REG \_ DWORD** | Conjunto de marcas, cada una de las cuales concede permiso para una acción específica. |



 

El valor de la **entrada Permissions** es or bit a bit **de** una o varias de las marcas siguientes.



| Marca (valor decimal) | Descripción                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1                    | Permiso para la reproducción. Los archivos que tienen la extensión de nombre de archivo registrada se pueden reproducir.                                                                                                                                                                                       |
| 2                    | Permiso para la colocación de carpetas. Los archivos que tienen la extensión de nombre de archivo registrado se incluirán en la lista de reproducción creada cuando el usuario arrastre una carpeta que contenga los archivos y la coloca en la interfaz de usuario del Reproductor.                                                      |
| 4                    | Permiso para CD multimedia. Los archivos que tengan la extensión de nombre de archivo registrado se incluirán en la lista de reproducción creada cuando se inserte un CD que contenga los archivos en la unidad de CD-ROM.                                                                                           |
| 8                    | Permiso para la biblioteca. Los archivos que tienen la extensión de nombre de archivo registrado se pueden agregar a la biblioteca. Necesario para los complementos de conversión.                                                                                                                                    |
| 16                   | Permiso para streaming HTML. Los archivos que tienen la extensión de nombre de archivo registrado se insertarán en la Internet Explorer caché cuando se entreguen desde una secuencia web.                                                                                                            |
| 128                  | Permiso para la transcodificación. Los archivos que tienen la extensión de nombre de archivo registrado se pueden transcodificar para Windows formato multimedia en determinadas condiciones. Vea [IWMPTranscodePolicy::allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode). Requiere Reproductor de Windows Media 10 o posterior. |



 

Cuando el usuario intenta reproducir un archivo multimedia que tiene una extensión de nombre de archivo personalizada, Reproductor de Windows Media busca una subclave del Registro que coincida con la extensión. Si no se encuentra ninguna coincidencia, el reproductor presenta al usuario un cuadro de diálogo de advertencia que solicita permiso al usuario para intentar reproducir el archivo. Si crea archivos multimedia digitales con extensiones de nombre de archivo personalizadas, puede evitar que esta advertencia aparezca en el equipo del usuario registrando la extensión de nombre de archivo y proporcionando una **entrada Permisos.**

La **entrada Permisos** (excepto el valor de marca 128) es compatible con Reproductor de Windows Media serie 9 y versiones posteriores. El valor de marca 128 es compatible con Reproductor de Windows Media 10 y versiones posteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensión de nombre de archivo Configuración**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




