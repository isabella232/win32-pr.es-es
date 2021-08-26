---
description: El terminal de reproducción de archivos y el terminal de grabación de archivos exponen las interfaces ITTerminal e ITMultiTrackTerminal. Estos objetos también exponen la interfaz ITMediaControl, que proporciona métodos para detener, iniciar y navegar por los medios.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminal de reproducción de archivos y terminal de grabación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad07ea46e2abf13465ac3344e69f586673c3b29463eac8bdd324966fb838368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100595"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>Terminal de reproducción de archivos y terminal de grabación de archivos

El terminal de reproducción de archivos y el terminal de grabación de archivos exponen las interfaces [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) e [**ITMultiTrackTerminal.**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) Estos objetos también exponen la [**interfaz ITMediaControl,**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) que proporciona métodos para detener, iniciar y navegar por los medios.

El Terminal de reproducción de archivos expone la [**interfaz ITMediaPlayback,**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) que tiene métodos específicos de reproducción.

El Terminal de grabación de archivos expone la [**interfaz ITMediaRecord,**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) que proporciona métodos específicos de la grabación.

Como [terminales multipista,](multitrack-terminals.md)el terminal de grabación de archivos y el terminal de reproducción de archivos administran una colección de [terminales de seguimiento.](track-terminals.md)

 

 
