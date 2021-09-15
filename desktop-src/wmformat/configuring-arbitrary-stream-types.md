---
title: Configuración de tipos de secuencia arbitrarios
description: Configuración de tipos de secuencia arbitrarios
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- streams,configuring arbitrary stream types
- códecs, configuración de tipos de secuencia arbitrarios
- streams,GenProfile
- codecs,GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e04751bd33da6599fd7ff3766c4dc8350889c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571268"
---
# <a name="configuring-arbitrary-stream-types"></a>Configuración de tipos de secuencia arbitrarios

La mayoría de los tipos de secuencia arbitrarios solo necesitan una velocidad de bits, una ventana de búfer y un tipo de medio principal adecuado en la [**estructura \_ WM MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Sin embargo, algunos tipos arbitrarios requieren una configuración adicional.

Si tiene problemas para configurar una secuencia, consulte la aplicación de ejemplo denominada GenProfile, que se incluye con este SDK. La biblioteca definida en GenProfile contiene código para incluir todos los tipos de secuencias. Para obtener más información sobre GenProfile y los otros ejemplos, vea [Aplicaciones de ejemplo](sample-applications.md).

En las secciones siguientes se describe cómo configurar tipos de secuencia arbitrarios.



| Sección                                                                                                                                        | Descripción                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Configuración de script Secuencias](configuring-script-streams.md)                                                                                   | Describe cómo configurar secuencias de scripts.                                                  |
| [Configuración de la transferencia de archivos Secuencias](configuring-file-transfer-streams.md)                                                                     | Describe cómo configurar flujos de transferencia de archivos.                                           |
| [Configuración de web Secuencias](configuring-web-streams.md)                                                                                         | Describe cómo configurar flujos web.                                                     |
| [Configuración de text Secuencias](configuring-text-streams.md)                                                                                       | Describe cómo configurar secuencias de texto.                                                    |
| [Configuración de parámetros arbitrarios personalizados Secuencias](configuring-custom-arbitrary-streams.md)                                                               | Describe cómo configurar secuencias para tipos de secuencia arbitrarios personalizados.                       |
| [Calcular los valores de la velocidad de bits y de la ventana de búfer para las Secuencias](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | Describe cómo calcular la velocidad de bits y la configuración de la ventana de búfer para una secuencia arbitraria. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Datos arbitrarios Secuencias**](arbitrary-streams.md)
</dt> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> </dl>

 

 




