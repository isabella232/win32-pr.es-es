---
title: Entrada del Registro FormatCode
description: Entrada del Registro FormatCode
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Reproductor de Windows Media,Entradas del Registro FormatCode
- Reproductor de Windows Media,extensiones de nombre de archivo
- Reproductor de Windows Media,registry
- registry,file name extensions
- registry,FormatCode entries
- registry,settings for Reproductor de Windows Media
- configuración del Registro de extensión de nombre de archivo
- Entradas del Registro formatCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170569"
---
# <a name="formatcode-registry-entry"></a>Entrada del Registro FormatCode

Cuando Reproductor de Windows Media encuentra una extensión de nombre de archivo personalizada, busca una subclave del Registro que coincida con la extensión. La subclave se describe en [File Name Extension Registry Configuración](file-name-extension-registry-settings.md). Una de las entradas del Registro que pueden aparecer bajo la subclave de la extensión es la **entrada FormatCode.**

La **entrada del Registro FormatCode** especifica el código de formato del Protocolo de transporte multimedia (MTP) para los archivos que tienen la extensión personalizada. La entrada del Registro **FormatCode** tiene el formato siguiente.



| Nombre       | Tipo           | Value                                                             |
|------------|----------------|-------------------------------------------------------------------|
| FormatCode | **REG \_ DWORD** | Entero positivo de 16 bits que identifica el formato del archivo. |



 

Cuando el usuario intenta copiar un archivo multimedia digital que tiene una extensión de nombre de archivo personalizada en un dispositivo portátil, Reproductor de Windows Media busca en el Registro un código de formato asociado a la extensión de nombre de archivo personalizado. Si Reproductor de Windows Media código de formato, usa MTP para determinar si el dispositivo admite el formato de archivo personalizado. Si el dispositivo admite el formato , el archivo multimedia se copia en el dispositivo sin transcodificarse.

Un dispositivo que admite MTP puede proporcionar Reproductor de Windows Media un conjunto de datos DeviceInfo, que contiene, entre otras cosas, una lista de códigos de formato admitidos por el dispositivo.

Si está en proceso de desarrollar un formato de archivo personalizado, puede solicitar un código de formato a Microsoft. Para obtener información sobre cómo solicitar un código de formato, vea Microsoft Media Transport Protocol Porting Kit, que está disponible en el Centro para desarrolladores de [Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensión de nombre de archivo Configuración**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




