---
title: Registro de complementos de conversión
description: Registro de complementos de conversión
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Reproductor de Windows Media,complementos de conversión
- Reproductor de Windows Media complementos,conversión
- complementos, conversión
- complementos de conversión, registro
- registro, complementos de conversión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070921"
---
# <a name="registering-conversion-plug-ins"></a>Registro de complementos de conversión

Los formatos de terceros deben registrarse antes Reproductor de Windows Media crear instancias y usar el complemento de conversión. Para registrar el archivo para la conversión, debe registrar la extensión de nombre de archivo asociada al formato.

La lista de extensiones de nombre de archivo registradas se mantiene como un conjunto de claves del Registro. Para obtener más información sobre cómo registrar formatos de terceros, vea [File Name Extension Registry Configuración](file-name-extension-registry-settings.md). En la tabla siguiente se muestra la configuración del valor del Registro para registrar un formato de terceros para la conversión mediante un complemento de conversión.



| Value                  | Parámetro                                                     |
|------------------------|-------------------------------------------------------------|
| **Tiempo de ejecución**            | 13                                                          |
| **Permisos**        | 8 (Permiso para la biblioteca).                             |
| **ConvertPluginCLSID** | Identificador de clase del complemento de conversión, en formato del Registro. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de complementos de conversión**](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




