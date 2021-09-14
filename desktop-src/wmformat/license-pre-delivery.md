---
title: Entrega previa de licencias
description: Entrega previa de licencias
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- Windows SDK de formato multimedia, entrega previa de licencias
- Windows SDK de formato multimedia, licencias
- administración de derechos digitales (DRM), entrega previa de licencias
- DRM (administración de derechos digitales), entrega previa de licencias
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas de cliente DRM, entrega previa de licencias
- API extendidas de cliente, entrega previa de licencias
- entrega previa de licencias
- licencias, entrega previa de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267092"
---
# <a name="license-pre-delivery"></a>Entrega previa de licencias

La entrega previa de licencias es el proceso que se usa para extraer licencias a un equipo cliente de forma preferente. Un escenario común para usar la entrega previa es cuando un usuario se suscribe a un servicio de música. Sin entregar licencias antes de que se necesiten, el usuario tendría que esperar a la adquisición de licencias para cada canción nueva.

Dado que la entrega previa no se realiza como respuesta al intento de acceso, normalmente solo lo realiza el propietario del contenido. Es decir, solo puede entregar previamente licencias para el contenido que controla. El proceso de entrega previa es una coordinación entre un componente cliente y un servidor de licencias creado mediante los objetos de Windows Media Digital Rights Management SDK.

La entrega previa de licencias es similar a [la adquisición de licencias no silenciosas.](non-silent-license-acquisition.md) Siga los mismos pasos, salvo que no tiene un encabezado DRM para pasar a [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md). El método generará un desafío que no es específico del contenido que puede enviar al servidor de licencias.

Como alternativa, puede usar el [Windows Media Rights Manager para](/previous-versions//bb676133(v=technet.10)) entregar licencias previamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adquisición de licencias**](acquiring-licenses.md)
</dt> <dt>

[**Uso del modelo Media Foundation eventos**](using-the-media-foundation-model.md)
</dt> </dl>

 

 