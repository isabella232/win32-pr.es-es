---
description: La lista siguiente contiene los miembros de la dirección CMSP.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Miembros de CMSPAddress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913818"
---
# <a name="cmspaddress-members"></a>Miembros de CMSPAddress



| Tipos de miembro                    | Nombre                    | Descripción                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| Iunknown                        | \*m \_ pFTM               | Puntero al serializador de subprocesamiento libre.                                                         |
| HANDLE                          | m \_ htEvent              | Identificador del evento de Tapi3.dll, que se usa para notificar a TAPI que el MSP quiere enviar datos a él. |
| entrada de lista \_                     | EventList de m \_            | Lista de eventos.                                                                                  |
| CMSPCritSection                 | m \_ EventDataLock        | El bloqueo que protege los datos relacionados con el control de eventos con TAPI.                             |
| ITTerminalManager               | \*m \_ pITTerminalManager | Puntero al objeto de administrador de Terminal Server.                                                      |
| CMSPArray <ITTerminal \*> | m \_ terminales            | Lista de los terminales estáticos que se pueden usar en la dirección.                                    |
| BOOL                            | m \_ fTerminalsUpToDate   | Esta marca es **true** si la lista de terminales está actualizada.                                        |
| CMSPCritSection                 | m \_ TerminalDataLock     | El bloqueo que protege los miembros de datos relacionados con terminal.                                        |



 

 

 



