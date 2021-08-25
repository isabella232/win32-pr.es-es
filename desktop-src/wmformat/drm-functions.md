---
title: Funciones de cliente drm Windows multimedia de Microsoft
description: Funciones de cliente drm Windows multimedia de Microsoft
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows SDK de formato multimedia, funciones
- administración de derechos digitales (DRM), funciones
- DRM (administración de derechos digitales), funciones
- API extendidas de cliente DRM, funciones
- API extendidas de cliente, funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aaf5f3c536027801a85f8d38120e6e14c5d366a6d727498a5bc1d1200cb041
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931175"
---
# <a name="microsoft-windows-media-drm-client-functions"></a>Funciones de cliente drm Windows multimedia de Microsoft

Las siguientes funciones se implementan como parte de las API extendidas de cliente drm Windows Media de Microsoft.



| Función                                                             | Descripción                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMDRMCreateProvider**](wmdrmcreateprovider.md)                   | Crea un generador de clases que puede crear los demás objetos DRM. Esta función no requiere una biblioteca de código auxiliar de Microsoft y crea objetos que no admiten las características de DRM protegidas. |
| [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) | Crea un generador de clases que puede crear los demás objetos DRM. Esta función requiere una biblioteca de código auxiliar de Microsoft y crea objetos que admiten las características de DRM protegidas.                |
| [**WMDRMShutdown**](wmdrmshutdown.md)                               | Libera los recursos usados por las API.                                                                                                                                                            |
| [**WMDRMStartup**](wmdrmstartup.md)                                 | Inicializa los recursos usados por las API.                                                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](drm-programming-reference.md)
</dt> </dl>

 

 




