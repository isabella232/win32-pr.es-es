---
description: El Terminal de streaming multimedia (MST) es un terminal dinámico basado en el uso de DirectShow filtros. Un MSP escrito con las clases base de MSP tapi 3 incorporará un MST, pero los autores de MSP pueden optar por implementarlo sin usar las clases base.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Terminal de streaming multimedia (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eeb9ad231c114ca18b4dea0926b861360ab5a359cd9ee8c48fd1c388a941a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002913"
---
# <a name="media-streaming-terminal-mst"></a>Terminal de streaming multimedia (MST)

El Terminal de streaming multimedia (MST) es un terminal dinámico basado en el uso de DirectShow filtros. Un MSP escrito con las clases [base msp tapi 3](tapi-3-msp-base-classes.md) incorporará un MST, pero los autores de MSP pueden optar por implementarlo sin usar las clases base.

Para invocar la creación de MST, una aplicación realiza una llamada a [**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) mediante *pTerminalClass* establecido en CLSID \_ MediaStreamTerminal.

A continuación, las interfaces [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) e [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) se exponen en el terminal, lo que permite a una aplicación optimizar el rendimiento de streaming. Estas interfaces se declaran en Tapi3.h.

La implementación y el uso de un MST requiere estar familiarizado con DirectShow filtros y la administración de gráficos de filtros. Consulte el material de DirectShow en el nodo Servicios gráficos y multimedia del Kit de desarrollo de software (SDK) de plataforma. La referencia de streaming multimedia será especialmente útil para los autores de MSP.

 

 
