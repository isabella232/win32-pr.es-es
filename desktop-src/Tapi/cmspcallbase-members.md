---
description: La lista siguiente contiene los miembros de CMSPCAllBase.
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: Miembros de CMSPCallBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276990"
---
# <a name="cmspcallbase-members"></a>Miembros de CMSPCallBase



| Tipo de miembro                   | Nombre             | Descripción                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                      | \*m \_ pFTM        | Puntero al serializador de subprocesamiento libre.                                                                                                                                                                                                                                                                                                          |
| CMSPAddress\*                 | \*m \_ pMSPAddress | Puntero al objeto de dirección MSP. Se usa para obtener los terminales predeterminados si la aplicación no selecciona ninguno. También incluye un refcount (a través de [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), no AddRef), por lo que la dirección agregada no desaparecerá mientras la llamada está todavía activa, pero la dirección de TAPI 3 no es AddRef'ed. |
| identificador de MSP \_                   | \*m \_ htCall      | Identificador de la llamada a TAPI3's. Se usa para desencadenar eventos de llamada.                                                                                                                                                                                                                                                                                             |
| DWORD                         | m \_ dwMediaType   | Máscara de archivo de los tipos de medios en esta llamada.                                                                                                                                                                                                                                                                                                          |
| CMSPArray <ITStream \*> | \_flujos m       | Lista de objetos de secuencia de la llamada.                                                                                                                                                                                                                                                                                                           |
| CMSPCritSection               | \_bloqueo m          | El bloqueo que protege las listas de secuencias.                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



