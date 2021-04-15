---
title: Consulta de información de derechos simples
description: Consulta de información de derechos simples
ms.assetid: 21ed3fb2-35b8-478a-a17e-f6b4da08d50d
keywords:
- SDK de Windows Media Format, consultando los derechos simples
- SDK de Windows Media Format, consultas de derechos simples
- Administración de derechos digitales (DRM), consulta de derechos simples
- DRM (administración de derechos digitales), consulta de derechos simples
- Administración de derechos digitales (DRM), consultas de derechos simples
- DRM (administración de derechos digitales), consultas de derechos simples
- API extendidas del cliente DRM, consultando derechos simples
- API extendidas del cliente, consultando derechos simples
- API extendidas del cliente DRM, consultas de derechos simples
- API extendidas de cliente, consultas de derechos simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d65929a369ad86753a0e549eb929ad344cdc368
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418716"
---
# <a name="querying-for-simple-rights-information"></a>Consulta de información de derechos simples

Las API extendidas del cliente DRM de Windows Media permiten obtener rápidamente información sencilla sobre si se puede tener acceso al contenido protegido para varias acciones.

El método [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) se puede usar para determinar rápidamente si una acción está permitida por una licencia en el almacén de licencias local. **QueryActionAllowed** se ha optimizado para que sea mucho más rápido que las consultas de información similar con los objetos del SDK de Windows Media Format. Sin embargo, este tipo de consulta agrega las licencias en el almacén de licencias local y solo se debe usar para características sencillas, como podría ser necesaria para los elementos de la interfaz de usuario, por ejemplo, para mostrar un indicador de permisos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Obtención de información de licencias en el almacén de licencias local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




