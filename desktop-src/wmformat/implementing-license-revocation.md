---
title: Implementación de la revocación de licencias
description: Implementación de la revocación de licencias
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- Windows SDK de formato multimedia, implementación de revocación de licencias
- Windows SDK de formato multimedia, revocación de licencias
- Windows SDK de formato multimedia, revocación de licencias
- Formato de sistemas avanzados (ASF), implementación de la revocación de licencias
- ASF (formato de sistemas avanzados), implementación de la revocación de licencias
- Formato de sistemas avanzados (ASF), revocación de licencias
- ASF (formato de sistemas avanzados), revocación de licencias
- Formato de sistemas avanzados (ASF), revocación de licencias
- ASF (formato de sistemas avanzados), revocación de licencias
- administración de derechos digitales (DRM), implementación de la revocación de licencias
- DRM (administración de derechos digitales), implementación de la revocación de licencias
- administración de derechos digitales (DRM), revocación de licencias
- DRM (administración de derechos digitales), revocación de licencias
- administración de derechos digitales (DRM), revocación de licencias
- DRM (administración de derechos digitales), revocación de licencias
- revocación de licencias, implementación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c73d0204e83c941600eefb53579b19ef72217055080c6ef4603d8eac28e08caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809135"
---
# <a name="implementing-license-revocation"></a>Implementación de la revocación de licencias

El SDK Windows Media Rights Manager 10 incluye una característica denominada revocación de licencias. Esta característica permite a los servidores de licencias solicitar que se quiten las licencias del equipo cliente. El SDK Windows Media Format proporciona métodos que procesan mensajes de revocación y quitan las licencias del almacén de licencias local.

Un servicio proporcionado por el emisor de la licencia inicia el proceso de revocación de licencias. La aplicación puede hospedar este servicio o puede ser una aplicación web. En cualquier caso, la aplicación debe poder recibir un desafío de licencia creado por el servicio.

Para quitar licencias del almacén de licencias, realice los pasos siguientes:

1.  Tras recibir un desafío de licencia del emisor de licencias, llame a la función [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) para crear un objeto de agente de revocación de licencias y obtener un puntero a la interfaz [**IWMLicenseRevocationAgent.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
2.  Llame al [**método IWMLicenseRevocationAgent::GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) para generar la respuesta del desafío.
3.  Envíe la respuesta del desafío de vuelta al componente del servicio de licencia desde el que recibió el desafío.
4.  El componente de servicio de licencia envía un blob de revocación de licencias (LRB) firmado a la aplicación. Cuando lo reciba, llame al [**método IWMLicenseRevocationAgent::P rocessLRB.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) **ProcessLRB crea** un mensaje de confirmación que debe devolver al servicio de licencias para comprobar que se han quitado las licencias.

> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> <dt>

[**IWMLicenseRevocationAgent (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




