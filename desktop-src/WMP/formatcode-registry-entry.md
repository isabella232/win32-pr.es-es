---
title: Entrada del registro FormatCode
description: Entrada del registro FormatCode
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Windows Media Player, entradas del registro de FormatCode
- Windows Media Player, extensiones de nombre de archivo
- Media Player de Windows, registro
- registro, extensiones de nombre de archivo
- registro, entradas FormatCode
- registro, configuración para Windows Media Player
- configuración del registro de la extensión de nombre de archivo
- Entradas del registro de FormatCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104270751"
---
# <a name="formatcode-registry-entry"></a>Entrada del registro FormatCode

Cuando Windows Media Player encuentra una extensión de nombre de archivo personalizada, busca una subclave del registro que coincida con la extensión. La subclave se describe en [configuración del registro](file-name-extension-registry-settings.md)de la extensión de nombre de archivo. Una de las entradas del registro que pueden aparecer bajo la subclave de la extensión es la entrada **FormatCode** .

La entrada del registro **FormatCode** especifica el código de formato del Protocolo de transporte multimedia (MTP) para los archivos que tienen la extensión personalizada. La entrada del registro **FormatCode** tiene el formato siguiente.



| Nombre       | Tipo           | Value                                                             |
|------------|----------------|-------------------------------------------------------------------|
| FormatCode | **\_valor DWORD reg** | Entero positivo de 16 bits que identifica el formato del archivo. |



 

Cuando el usuario intenta copiar un archivo multimedia digital que tiene una extensión de nombre de archivo personalizada en un dispositivo portátil, Windows Media Player busca en el registro para encontrar un código de formato asociado a la extensión de nombre de archivo personalizada. Si Windows Media Player encuentra un código de formato, utiliza MTP para determinar si el dispositivo admite el formato de archivo personalizado. Si el dispositivo admite el formato, el archivo multimedia se copia en el dispositivo sin ser transcodificado.

Un dispositivo que admite MTP puede proporcionar Windows Media Player con un conjunto de DeviceInfo, que contiene, entre otras cosas, una lista de códigos de formato admitidos por el dispositivo.

Si está en el proceso de desarrollar un formato de archivo personalizado, puede solicitar un código de formato de Microsoft. Para obtener información acerca de cómo solicitar un código de formato, vea el kit de migración de protocolo de transporte de multimedia de Microsoft, que está disponible en el [Centro para desarrolladores de Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración del registro de la extensión de nombre de archivo**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




