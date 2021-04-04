---
title: Entrada del registro de permisos
description: Entrada del registro de permisos
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player, extensiones de nombre de archivo
- Media Player de Windows, permisos
- Media Player de Windows, registro
- registro, extensiones de nombre de archivo
- registro, permisos
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
- permisos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077292"
---
# <a name="permissions-registry-entry"></a>Entrada del registro de permisos

Cuando Windows Media Player encuentra una extensión de nombre de archivo personalizada, busca una subclave del registro que coincida con la extensión. La subclave se describe en [configuración del registro](file-name-extension-registry-settings.md)de la extensión de nombre de archivo. Una de las entradas del registro que pueden aparecer bajo la subclave de la extensión es la entrada de **permisos** .

La entrada de **permisos** especifica las acciones que puede realizar Windows Media Player en los archivos que tienen la extensión personalizada. La entrada de **permisos** tiene el formato siguiente.



| Nombre        | Tipo           | Value                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| Permisos | **\_valor DWORD reg** | Un conjunto de marcas, cada una de las cuales concede el permiso para una acción específica. |



 

El valor de la entrada **Permissions** es **una operación OR bit a bit** de una o varias de las marcas siguientes.



| Marca (valor decimal) | Descripción                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1                    | Permiso para la reproducción. Se pueden reproducir archivos con la extensión de nombre de archivo registrada.                                                                                                                                                                                       |
| 2                    | Permiso para quitar carpetas. Los archivos que tengan la extensión de nombre de archivo registrada se incluirán en la lista de reproducción que se creó cuando el usuario arrastra una carpeta que contiene los archivos y la coloca en la interfaz de usuario del reproductor.                                                      |
| 4                    | Permiso para el CD de multimedia. Los archivos que tengan la extensión de nombre de archivo registrada se incluirán en la lista de reproducción creada cuando se inserte un CD que contenga los archivos en la unidad de CD-ROM.                                                                                           |
| 8                    | Permiso para la biblioteca. Los archivos que tienen la extensión de nombre de archivo registrada se pueden agregar a la biblioteca. Se requiere para los complementos de conversión.                                                                                                                                    |
| 16                   | Permiso para la transmisión por secuencias de HTML. Los archivos que tengan la extensión de nombre de archivo registrada se insertarán en la memoria caché de Internet Explorer cuando se entreguen desde una secuencia Web.                                                                                                            |
| 128                  | Permiso para la transcodificación. Los archivos que tienen la extensión de nombre de archivo registrada se pueden transcodificar en formato de Windows Media en determinadas condiciones. Vea [IWMPTranscodePolicy:: allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode). Requiere Windows Media Player 10 o posterior. |



 

Cuando el usuario intenta reproducir un archivo multimedia que tiene una extensión de nombre de archivo personalizada, Windows Media Player busca una subclave del registro que coincida con la extensión. Si no se encuentra ninguna coincidencia, el reproductor presenta al usuario un cuadro de diálogo de advertencia que solicita permiso al usuario para intentar reproducir el archivo. Si crea archivos multimedia digitales con extensiones de nombre de archivo personalizadas, puede evitar que esta advertencia aparezca en el equipo del usuario si registra la extensión de nombre de archivo y proporciona una entrada de **permisos** .

La entrada de **permisos** (excepto el valor de marca 128) es compatible con Windows Media Player 9 series y versiones posteriores. Windows Media Player 10 y versiones posteriores admiten el valor de marca 128.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del registro de la extensión de nombre de archivo**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




