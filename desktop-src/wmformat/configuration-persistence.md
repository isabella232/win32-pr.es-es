---
title: Persistencia de configuración
description: Persistencia de configuración
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Media Format SDK, persistencia
- SDK de Windows Media Format, persistencia de configuración
- Advanced Systems Format (ASF), persistencia
- ASF (formato de sistemas avanzados), persistencia
- Advanced Systems Format (ASF), persistencia de configuración
- ASF (formato de sistemas avanzados), persistencia de configuración
- persistencia de configuración
- persistencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420319"
---
# <a name="configuration-persistence"></a>Persistencia de configuración

El SDK de Windows Media guarda ninguna de las propiedades habilitadas para escritura descritas en esta documentación. Cada aplicación que usa el SDK debe proporcionar sus propios procedimientos de persistencia según sea necesario e invocar el método de conjunto adecuado en cada instancia del SDK. De esta forma, los cambios de configuración realizados por una aplicación no afectan a otra aplicación. Por ejemplo, cambiar el tiempo de almacenamiento en búfer en un reproductor no afecta a otro reproductor.

La única excepción a esta regla es para la información de las credenciales. Si la aplicación indica, en su retorno de la llamada a **AcquireCredentials** , que la información de ID. de usuario y contraseña debe persistir, el SDK guarda esta información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de la funcionalidad de red**](implementing-network-functionality.md)
</dt> <dt>

[**Interfaz IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




