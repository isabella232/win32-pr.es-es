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
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360967"
---
# <a name="microsoft-windows-media-drm-client-functions"></a>Funciones de cliente drm Windows multimedia de Microsoft

Las siguientes funciones se implementan como parte de las API extendidas del cliente drm Windows Media de Microsoft.



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

 

 




