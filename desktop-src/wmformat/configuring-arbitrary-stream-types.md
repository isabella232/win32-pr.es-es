---
title: Configuración de tipos de flujo arbitrarios
description: Configuración de tipos de flujo arbitrarios
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- flujos, configurar tipos de secuencia arbitrarios
- códecs, configurar tipos de secuencias arbitrarios
- flujos, GenProfile
- códecs, GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714173"
---
# <a name="configuring-arbitrary-stream-types"></a>Configuración de tipos de flujo arbitrarios

La mayoría de los tipos de secuencias arbitrarias solo necesitan una velocidad de bits, una ventana de búfer y un tipo de medio principal adecuado en la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Sin embargo, algunos tipos arbitrarios requieren una configuración adicional.

Si tiene problemas para configurar una secuencia, consulte la aplicación de ejemplo llamada GenProfile, que se incluye con este SDK. La biblioteca definida en GenProfile contiene código para incluir todos los tipos de secuencias. Para obtener más información sobre GenProfile y los otros ejemplos, vea [aplicaciones de ejemplo](sample-applications.md).

En las secciones siguientes se describe cómo configurar tipos de secuencia arbitrarios.



| Sección                                                                                                                                        | Descripción                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Configurar secuencias de scripts](configuring-script-streams.md)                                                                                   | Describe cómo configurar secuencias de scripts.                                                  |
| [Configuración de secuencias de transferencia de archivos](configuring-file-transfer-streams.md)                                                                     | Describe cómo configurar secuencias de transferencia de archivos.                                           |
| [Configuración de secuencias Web](configuring-web-streams.md)                                                                                         | Describe cómo configurar secuencias Web.                                                     |
| [Configurar secuencias de texto](configuring-text-streams.md)                                                                                       | Describe cómo configurar secuencias de texto.                                                    |
| [Configuración de secuencias arbitrarias personalizadas](configuring-custom-arbitrary-streams.md)                                                               | Describe cómo configurar secuencias para tipos de secuencia arbitrarios personalizados.                       |
| [Calcular la velocidad de bits y los valores de la ventana de búfer para flujos arbitrarios](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | Describe cómo calcular la velocidad de bits y la configuración de la ventana de búfer para una secuencia arbitraria. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Flujos arbitrarios**](arbitrary-streams.md)
</dt> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> </dl>

 

 




