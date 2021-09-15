---
title: Persistencia de configuración
description: Persistencia de configuración
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows SDK de formato multimedia, persistencia
- Windows SDK de formato multimedia, persistencia de configuración
- Formato de sistemas avanzados (ASF), persistencia
- ASF (formato de sistemas avanzados), persistencia
- Formato de sistemas avanzados (ASF), persistencia de configuración
- ASF (formato de sistemas avanzados), persistencia de configuración
- persistencia de configuración
- persistencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571265"
---
# <a name="configuration-persistence"></a>Persistencia de configuración

El SDK de media no guarda ninguna de las propiedades habilitadas para escritura descritas en Windows esta documentación. Cada aplicación que usa el SDK debe proporcionar sus propios procedimientos de persistencia según sea necesario e invocar el método set adecuado en cada instancia del SDK. De esta manera, los cambios de configuración realizados por una aplicación no afectan a otra aplicación. Por ejemplo, cambiar el tiempo de almacenamiento en búfer en un reproductor no afecta a otro jugador.

La única excepción a esta regla es para la información de credenciales. Si la aplicación indica, en su devolución de la llamada **a AcquireCredentials,** que se debe conservar la información del identificador de usuario y la contraseña, el SDK guarda esta información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de la funcionalidad de red**](implementing-network-functionality.md)
</dt> <dt>

[**IWMCredentialCallback (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




