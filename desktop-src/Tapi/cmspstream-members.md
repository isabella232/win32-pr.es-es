---
description: La lista siguiente contiene los miembros de CMSPStream.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: Miembros de CMSPStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156565"
---
# <a name="cmspstream-members"></a>Miembros de CMSPStream



| Tipo de miembro                     | Nombre                | Descripción                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                        | \*m \_ pFTM           | Puntero al serializador de subprocesamiento libre.                                                                                                   |
| DWORD                           | m \_ dwState          | Estado actual de la secuencia.                                                                                                           |
| HANDLE                          | m \_ hAddress         | Dirección en la que se usa esta secuencia.                                                                                            |
| DWORD                           | m \_ dwMediaType      | El [**tipo de medio**](tapimediatype--constants.md) de este flujo (audio, vídeo, etc.).                                                    |
| Dirección del TERMINAL \_             | \_Dirección m        | [**Dirección**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) de este flujo (entrante o saliente).                                                         |
| CMSPCallBase                    | \*m \_ pMSPCall       | Puntero al objeto de llamada.                                                                                                                |
| IGraphBuilder                   | \*m \_ pIGraphBuilder | Puntero a las interfaces del objeto de gráfico.                                                                                                        |
| IMediaControl                   | \*m \_ pIMediaControl | Puntero a la interfaz de control de medios.                                                                                                    |
| CMSPArray <ITTerminal \*> | m \_ terminales        | Lista de terminales del flujo.                                                                                                       |
| CMSPCritSection                 | \_bloqueo m             | El bloqueo que protege el objeto de secuencia. El objeto de secuencia nunca debe adquirir el bloqueo y llamar a un método MSPCall que podría bloquearse. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



