---
title: Motivos de no repetibilidad
description: En la tabla siguiente se enumeran los valores constantes que indican por qué no se puede acceder a una interfaz.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cb833409d9d2ba31adedbc2942d39399c0a5763ad4d65dc7cdcaf234f97efb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025415"
---
# <a name="unreachability-reasons"></a>Motivos de no repetibilidad

En la tabla siguiente se enumeran los valores constantes que indican por qué no se puede acceder a una interfaz.



| Value                                       | Significado                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| ADMINISTRADOR DE LA INTERFAZ DE MPR \_ \_ \_ DESHABILITADO             | El administrador ha deshabilitado la interfaz.                                                  |
| ERROR DE CONEXIÓN \_ DE LA \_ INTERFAZ MPR \_         | Error en el intento de conexión anterior. Busque el código de error en el miembro **dwLastError.** |
| RESTRICCIÓN DE HORAS DE \_ ACCESO TELEFÓNICO DE LA \_ \_ INTERFAZ \_ MPR | No se permite el acceso telefónico en el momento actual.                                                   |
| INTERFAZ MPR \_ \_ FUERA DE \_ \_ RECURSOS          | No hay puertos ni dispositivos disponibles para su uso.                                                     |
| SERVICIO DE \_ INTERFAZ \_ MPR \_ EN PAUSA             | El servicio está en pausa.                                                                         |
| INTERFAZ MPR \_ \_ SIN SENTIDO \_ \_ MULTIMEDIA            | El cable de red está desconectado de la tarjeta de red.                                       |
| INTERFAZ MPR \_ \_ SIN \_ DISPOSITIVO                  | La tarjeta de red se ha quitado de la máquina.                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MPR \_ INTERFACE \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[**INTERFAZ DE MPR \_ \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[**MIB \_ IFROW**](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[**MIB \_ IFSTATUS**](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 