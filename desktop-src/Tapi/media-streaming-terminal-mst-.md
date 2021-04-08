---
description: El terminal de transmisión por secuencias multimedia (MST) es un terminal dinámico basado en el uso de filtros de DirectShow. Un MSP escrito mediante las clases base de TAPI 3 MSP incorporará un MST, pero los autores de MSP pueden optar por implementarlo sin usar las clases base.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Terminal de streaming multimedia (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb9bb4b97d0e741aec96454b187beefe2d21eb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003370"
---
# <a name="media-streaming-terminal-mst"></a>Terminal de streaming multimedia (MST)

El terminal de transmisión por secuencias multimedia (MST) es un terminal dinámico basado en el uso de filtros de DirectShow. Un MSP escrito mediante las [clases base de TAPI 3 MSP](tapi-3-msp-base-classes.md) incorporará un MST, pero los autores de MSP pueden optar por implementarlo sin usar las clases base.

Para invocar la creación de MST, una aplicación realiza una llamada a [**ITTerminalSupport:: CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) con *PTERMINALCLASS* establecido en CLSID \_ MediaStreamTerminal.

A continuación, se exponen las interfaces [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) y [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) en el terminal, lo que permite a una aplicación optimizar el rendimiento de streaming. Estas interfaces se declaran en Tapi3. h.

La implementación y el uso de un MST requiere estar familiarizado con los filtros de DirectShow y la administración de gráficos de filtros. Consulte el material de DirectShow en el nodo gráficos y servicios multimedia del kit de desarrollo de software (SDK) de la plataforma. La referencia de streaming multimedia será especialmente útil para los autores de MSP.

 

 
