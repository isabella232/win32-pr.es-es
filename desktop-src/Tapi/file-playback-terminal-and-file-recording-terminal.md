---
description: El terminal de reproducción de archivos y el terminal de grabación de archivos exponen las interfaces ITTerminal y ITMultiTrackTerminal. Estos objetos también exponen la interfaz ITMediaControl, que proporciona métodos para detener, iniciar y navegar por los elementos multimedia.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminal de reproducción de archivos y terminal de grabación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a73c788e3e1750e44298c1020a088cf8111bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001930"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>Terminal de reproducción de archivos y terminal de grabación de archivos

El terminal de reproducción de archivos y el terminal de grabación de archivos exponen las interfaces [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) y [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) . Estos objetos también exponen la interfaz [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) , que proporciona métodos para detener, iniciar y navegar por los elementos multimedia.

El terminal de reproducción de archivos expone la interfaz [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) , que tiene métodos específicos de reproducción.

El terminal de grabación de archivos expone la interfaz [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) , que proporciona métodos específicos del registro.

Como [terminales multipista](multitrack-terminals.md), el terminal de grabación de archivos y el terminal de reproducción de archivos administran una colección de [terminales de seguimiento](track-terminals.md).

 

 
