---
title: Razones de inasequibilidad
description: En la tabla siguiente se muestran los valores constantes que indican por qué no se puede tener acceso a una interfaz.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078102"
---
# <a name="unreachability-reasons"></a>Razones de inasequibilidad

En la tabla siguiente se muestran los valores constantes que indican por qué no se puede tener acceso a una interfaz.



| Value                                       | Significado                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| Administrador de la interfaz de MPR \_ \_ \_ deshabilitado             | El administrador ha deshabilitado la interfaz.                                                  |
| error de conexión de la interfaz de MPR \_ \_ \_         | Error en el intento de conexión anterior. Busque el miembro **dwLastError** para el código de error. |
| \_restricción de \_ horas de \_ inactividad \_ de la interfaz de MPR | No se permite el acceso telefónico en el momento actual.                                                   |
| \_interfaz \_ de MPR \_ sin \_ recursos          | No hay puertos o dispositivos disponibles para su uso.                                                     |
| servicio de interfaz de MPR en \_ \_ \_ pausa             | El servicio está en pausa.                                                                         |
| interfaz de MPR \_ \_ sin \_ detección de medios \_            | El cable de red está desconectado de la tarjeta de red.                                       |
| interfaz de MPR \_ \_ sin \_ dispositivo                  | La tarjeta de red se ha quitado de la máquina.                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MPR ( \_ interfaz) \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[**Interfaz de MPR \_ \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[**MIB \_ IFROW**](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[**MIB \_ IFSTATUS**](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 