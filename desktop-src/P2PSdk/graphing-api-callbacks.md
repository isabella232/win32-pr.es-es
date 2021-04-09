---
description: 'La API de gráficos usa las siguientes devoluciones de llamada:'
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: Devoluciones de llamada de la API de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11f4f559307e457822cd0e7ce18ef4b44119697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082656"
---
# <a name="graphing-api-callbacks"></a>Devoluciones de llamada de la API de gráficos

La API de gráficos usa las siguientes devoluciones de llamada:



| Devolución de llamada                                                          | Descripción                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*PFNPEER \_ \_ datos de seguridad gratuitos \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | Especifica la función a la que llama la infraestructura de gráficos del mismo nivel para liberar los datos devueltos por el [*\_ \_ registro seguro de PFNPEER*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) y PFNPEER validar las devoluciones de llamada de [*\_ \_ registro*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) . |
| [*\_registro seguro de PFNPEER \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | Especifica la función a la que llama la infraestructura de gráficos del mismo nivel para proteger los registros.                                                                                                                                        |
| [*PFNPEER \_ validar \_ registro*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | Especifica la función a la que llama la infraestructura de gráficos del mismo nivel para validar registros.                                                                                                                                      |



 

 

 



