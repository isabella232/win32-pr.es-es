---
title: Entrega previa de licencias
description: Entrega previa de licencias
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- SDK de Windows Media Format, entrega previa de licencias
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), entrega previa de licencias
- DRM (administración de derechos digitales), entrega previa de licencias
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas del cliente DRM, entrega previa de licencias
- API extendidas de cliente, entrega previa de licencias
- entrega previa de licencias
- licencias, entrega previa de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656383"
---
# <a name="license-pre-delivery"></a>Entrega previa de licencias

La entrega previa de licencias es el proceso que se usa para extraer las licencias a un equipo cliente de forma preferente. Un escenario común para usar la entrega previa es cuando un usuario se suscribe a un servicio de música. Sin ofrecer licencias antes de que sean necesarias, el usuario tendría que esperar la adquisición de licencias para cada nueva canción.

Dado que la entrega previa no se realiza como respuesta al intento de acceso, normalmente solo la realiza el propietario del contenido. Es decir, solo puede proporcionar licencias previas para el contenido que usted controla. El proceso de preventa es una coordinación entre un componente de cliente y un servidor de licencias creado mediante los objetos del SDK de Rights Management digital de Windows Media.

La entrega previa de licencias es similar a [la adquisición de licencias no silenciosa](non-silent-license-acquisition.md). Siga los mismos pasos, excepto que no tiene un encabezado DRM para pasar a [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md). El método generará un desafío que no es específico del contenido y que puede enviar al servidor de licencias.

También puede usar el administrador de [derechos de Windows Media](/previous-versions//bb676133(v=technet.10)) para proporcionar licencias previamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adquisición de licencias**](acquiring-licenses.md)
</dt> <dt>

[**Usar el modelo de eventos Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 