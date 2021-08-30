---
title: Entrega previa de la licencia
description: Entrega previa de la licencia
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- Windows SDK de formato multimedia, entrega previa de licencias
- Windows SDK de formato multimedia, licencias
- administración de derechos digitales (DRM), entrega previa de licencias
- DRM (administración de derechos digitales), entrega previa de licencias
- administración de derechos digitales (DRM),licencias
- DRM (administración de derechos digitales), licencias
- API extendidas de cliente DRM, entrega previa de licencias
- API extendidas de cliente, entrega previa de licencias
- entrega previa de licencias
- licencias, entrega previa de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35064bf6fe69ca5586c27c3cb8d3d907e2dbff77e8f9ad34bb28ef2718fb7f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808295"
---
# <a name="license-pre-delivery"></a>Entrega previa de la licencia

La entrega previa de licencias es el proceso que se usa para extraer licencias a un equipo cliente de forma preferente. Un escenario común para usar la entrega previa es cuando un usuario se suscribe a un servicio de música. Sin entregar licencias antes de que se necesiten, el usuario tendría que esperar a la adquisición de licencias para cada canción nueva.

Dado que la entrega previa no se realiza como respuesta al intento de acceso, normalmente solo lo realiza el propietario del contenido. Es decir, solo puede entregar previamente licencias para el contenido que controle. El proceso de entrega previa es una coordinación entre un componente cliente y un servidor de licencias creado mediante los objetos del SDK de Windows Media Digital Rights Management.

La entrega previa de la licencia es similar a [la adquisición de licencias no silenciosa.](non-silent-license-acquisition.md) Siga los mismos pasos, salvo que no tiene un encabezado DRM para pasar a [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md). El método generará un desafío que no es específico del contenido que puede enviar al servidor de licencias.

Como alternativa, puede usar el [Windows Media Rights Manager para](/previous-versions//bb676133(v=technet.10)) entregar licencias previamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adquisición de licencias**](acquiring-licenses.md)
</dt> <dt>

[**Uso del modelo Media Foundation eventos**](using-the-media-foundation-model.md)
</dt> </dl>

 

 