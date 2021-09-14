---
description: La lista siguiente contiene los miembros de dirección de CMSP.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Miembros CMSPAddress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250286"
---
# <a name="cmspaddress-members"></a>Miembros CMSPAddress



| Tipos de miembro                    | Nombre                    | Descripción                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| Iunknown                        | \*m \_ pFTM               | Puntero al marshaller de subproceso libre.                                                         |
| HANDLE                          | m \_ htEvent              | Controle Tapi3.dll evento de la aplicación, que se usa para notificar a TAPI que el MSP quiere enviarle datos. |
| LIST \_ ENTRY                     | m \_ EventList            | Lista de eventos.                                                                                  |
| CMSPCritSection                 | m \_ EventDataLock        | Bloqueo que protege los datos relacionados con el control de eventos con TAPI.                             |
| ITTerminalManager               | \*m \_ pITTerminalManager | Puntero al objeto de Terminal Manager.                                                      |
| CMSPArray <ITTerminal \*> | m \_ Terminals            | Lista de terminales estáticos que se pueden usar en la dirección.                                    |
| BOOL                            | m \_ fTerminalsUpToDate   | Esta marca es **TRUE si** la lista de terminales está actualizada.                                        |
| CMSPCritSection                 | m \_ TerminalDataLock     | Bloqueo que protege los miembros de datos relacionados con el terminal.                                        |



 

 

 



