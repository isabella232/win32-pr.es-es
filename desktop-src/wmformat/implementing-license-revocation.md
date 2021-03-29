---
title: Implementación de la revocación de licencias
description: Implementación de la revocación de licencias
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- SDK de Windows Media Format, implementar la revocación de licencias
- SDK de Windows Media Format, revocación de licencia
- SDK de Windows Media Format, revocación de licencias
- Advanced Systems Format (ASF), implementación de la revocación de licencias
- ASF (formato de sistemas avanzados), implementación de la revocación de licencias
- Advanced Systems Format (ASF), revocación de licencia
- ASF (formato de sistemas avanzados), revocación de licencia
- Advanced Systems Format (ASF), revocación de licencias
- ASF (formato de sistemas avanzados), revocación de licencias
- Administración de derechos digitales (DRM), implementación de la revocación de licencias
- DRM (administración de derechos digitales), implementación de la revocación de licencias
- Administración de derechos digitales (DRM), revocación de licencia
- DRM (administración de derechos digitales), revocación de licencia
- Administración de derechos digitales (DRM), revocación de licencias
- DRM (administración de derechos digitales), revocación de licencias
- revocación de licencias, implementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83bfb1a512b031f5b7c297ecede4ed33fba8f2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788817"
---
# <a name="implementing-license-revocation"></a>Implementación de la revocación de licencias

El SDK de Windows Media Rights Manager 10 incluye una característica denominada revocación de licencia. Esta característica permite que los servidores de licencias soliciten que se quiten las licencias del equipo cliente. El SDK de Windows Media Format proporciona métodos que procesan los mensajes de revocación y quitan las licencias del almacén de licencias local.

Un servicio proporcionado por el emisor de la licencia inicia el proceso de revocación de licencias. La aplicación puede hospedar este servicio o puede ser una aplicación Web. En cualquier caso, la aplicación debe ser capaz de recibir un desafío de licencia creado por el servicio.

Para quitar licencias del almacén de licencias, realice los pasos siguientes:

1.  Tras recibir un desafío de licencia del emisor de la licencia, llame a la función [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) para crear un objeto de agente de revocación de licencias y obtener un puntero a la interfaz [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .
2.  Llame al método [**IWMLicenseRevocationAgent:: GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) para generar la respuesta de desafío.
3.  Vuelva a enviar la respuesta de desafío al componente del servicio de licencias desde el que recibió el desafío.
4.  El componente del servicio de licencias envía un BLOB de revocación de licencia (LRB) firmado a la aplicación. Cuando lo reciba, llame al método [**IWMLicenseRevocationAgent::P rocesslrb**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) . **ProcessLRB** crea un mensaje de confirmación que debe devolver al servicio de licencias para comprobar que se han quitado las licencias.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interfaz IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




