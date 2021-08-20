---
title: Configuración de tipos de secuencia arbitrarios
description: Configuración de tipos de secuencia arbitrarios
ms.assetid: d745ec4b-9ce5-4288-bc24-0c1220c4d510
keywords:
- streams,configuring arbitrary stream types
- codecs,configuring arbitrary stream types
- streams,GenProfile
- codecs,GenProfile
- GenProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260219e408872dc21ecf82bd64b59b6c12b014c6e073a687a1b55957b290b76f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548055"
---
# <a name="configuring-arbitrary-stream-types"></a>Configuración de tipos de secuencia arbitrarios

La mayoría de los tipos de flujo arbitrarios solo necesitan una velocidad de bits, una ventana de búfer y un tipo de medio principal adecuado en la [**estructura \_ WM MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Sin embargo, algunos tipos arbitrarios requieren una configuración adicional.

Si tiene problemas para configurar una secuencia, consulte la aplicación de ejemplo denominada GenProfile, que se incluye con este SDK. La biblioteca definida en GenProfile contiene código para incluir todos los tipos de secuencias. Para obtener más información sobre GenProfile y otros ejemplos, vea [Aplicaciones de ejemplo.](sample-applications.md)

En las secciones siguientes se describe cómo configurar tipos de secuencia arbitrarios.



| Sección                                                                                                                                        | Descripción                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Configuración de scripts Secuencias](configuring-script-streams.md)                                                                                   | Describe cómo configurar secuencias de scripts.                                                  |
| [Configuración de la transferencia de archivos Secuencias](configuring-file-transfer-streams.md)                                                                     | Describe cómo configurar secuencias de transferencia de archivos.                                           |
| [Configuración de web Secuencias](configuring-web-streams.md)                                                                                         | Describe cómo configurar secuencias web.                                                     |
| [Configuración de text Secuencias](configuring-text-streams.md)                                                                                       | Describe cómo configurar secuencias de texto.                                                    |
| [Configuración de parámetros arbitrarios personalizados Secuencias](configuring-custom-arbitrary-streams.md)                                                               | Describe cómo configurar secuencias para tipos de secuencia arbitrarios personalizados.                       |
| [Calcular la velocidad de bits y los valores de la ventana de búfer para los valores Secuencias](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md) | Describe cómo calcular la velocidad de bits y la configuración de la ventana de búfer para una secuencia arbitraria. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Errores arbitrarios Secuencias**](arbitrary-streams.md)
</dt> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> </dl>

 

 




