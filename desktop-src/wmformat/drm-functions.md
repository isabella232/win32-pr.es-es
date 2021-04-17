---
title: Funciones de cliente DRM de Microsoft Windows Media
description: Funciones de cliente DRM de Microsoft Windows Media
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Media Format SDK, funciones
- Administración de derechos digitales (DRM), funciones
- DRM (administración de derechos digitales), funciones
- API extendidas del cliente DRM, funciones
- API extendidas de cliente, funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705089"
---
# <a name="microsoft-windows-media-drm-client-functions"></a>Funciones de cliente DRM de Microsoft Windows Media

Las siguientes funciones se implementan como parte de las API extendidas del cliente DRM de Microsoft Windows Media.



| Función                                                             | Descripción                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMDRMCreateProvider**](wmdrmcreateprovider.md)                   | Crea un generador de clases que puede crear los demás objetos DRM. Esta función no requiere una biblioteca de código auxiliar de Microsoft y crea objetos que no admiten las características DRM protegidas. |
| [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) | Crea un generador de clases que puede crear los demás objetos DRM. Esta función requiere una biblioteca de código auxiliar de Microsoft y crea objetos que admiten las características DRM protegidas.                |
| [**WMDRMShutdown**](wmdrmshutdown.md)                               | Libera los recursos utilizados por las API.                                                                                                                                                            |
| [**WMDRMStartup**](wmdrmstartup.md)                                 | Inicializa los recursos utilizados por las API.                                                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](drm-programming-reference.md)
</dt> </dl>

 

 




