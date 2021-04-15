---
title: Configurar secuencias de texto
description: Configurar secuencias de texto
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- flujos, configurar secuencias de texto
- códecs, configurar secuencias de texto
- secuencias de texto, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486814"
---
# <a name="configuring-text-streams"></a>Configurar secuencias de texto

Los flujos de texto son esencialmente los mismos que los flujos arbitrarios personalizados. No hay información de configuración asociada a una secuencia de texto para identificar el tipo de codificación de texto, por lo que el objeto de escritor no puede comprobar los ejemplos.

Para configurar una secuencia de texto, debe asegurarse de que la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contiene un tipo de medio principal de texto WMMEDIATYPE \_ . También debe establecer una velocidad de bits y una ventana de búfer para la secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Calcular la velocidad de bits y los valores de la ventana de búfer para flujos arbitrarios**](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[**Configuración común para todos los flujos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de tipos de flujo arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Secuencias de texto**](text-streams.md)
</dt> </dl>

 

 




