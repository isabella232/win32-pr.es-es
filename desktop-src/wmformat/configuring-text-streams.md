---
title: Configuración de text Secuencias
description: Configuración de text Secuencias
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- streams,configuring text streams
- códecs, configurar secuencias de texto
- flujos de texto, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251528"
---
# <a name="configuring-text-streams"></a>Configuración de text Secuencias

Las secuencias de texto son básicamente las mismas que las secuencias arbitrarias personalizadas. No hay información de configuración asociada a una secuencia de texto para identificar el tipo de codificación de texto, por lo que el objeto de escritor no puede comprobar los ejemplos.

Para configurar una secuencia de texto, debe asegurarse de que la estructura [**WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contiene un tipo de medio principal de WMMEDIATYPE \_ TEXT. También debe establecer una velocidad de bits y una ventana de búfer para la secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Calcular los valores de la velocidad de bits y de la ventana de búfer para las Secuencias**](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[**Configuración común a todas las Secuencias**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de tipos de secuencia arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Secuencias de texto**](text-streams.md)
</dt> </dl>

 

 




