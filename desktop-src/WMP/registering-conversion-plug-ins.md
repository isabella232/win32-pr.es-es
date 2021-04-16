---
title: Registrar complementos de conversión
description: Registrar complementos de conversión
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Windows Media Player, Complementos de conversión
- Complementos de Windows Media Player, conversión
- complementos, conversión
- Complementos de conversión, registrar
- registro, Complementos de conversión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685512"
---
# <a name="registering-conversion-plug-ins"></a>Registrar complementos de conversión

Los formatos de terceros deben registrarse antes de que Windows Media Player pueda crear instancias y usar el complemento de conversión. Para registrar el archivo para su conversión, debe registrar la extensión de nombre de archivo asociada con el formato.

La lista de extensiones de nombre de archivo registradas se mantiene como un conjunto de claves del registro. Para obtener más información sobre el registro de formatos de terceros, consulte [configuración del registro](file-name-extension-registry-settings.md)de la extensión de nombre de archivo. En la tabla siguiente se enumeran los valores del valor del registro para registrar un formato de terceros para la conversión mediante un complemento de conversión.



| Value                  | Configuración                                                     |
|------------------------|-------------------------------------------------------------|
| **Tiempo de ejecución**            | 13                                                          |
| **Permisos**        | 8 (permiso para la biblioteca).                             |
| **ConvertPluginCLSID** | IDENTIFICADOR de clase del complemento de conversión, en formato de registro. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de complementos de conversión**](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




