---
title: EC_WMT_EVENT (Windows SDK de formato multimedia 11)
description: EVENTO \_ WMT \_ DE EC
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- Windows SDK de formato multimedia, EC_WMT_EVENT
- DirectShow,EC_WMT_EVENT
- EC_WMT_EVENT
- administración de derechos digitales (DRM),EC_WMT_EVENT
- DRM (administración de derechos digitales), EC_WMT_EVENT
- Formato de sistemas avanzados (ASF),EC_WMT_EVENT
- ASF (formato de sistemas avanzados), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe0e53a759515914a352707550e281aca3aebe096f168352c36c1ff4200b2ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029224"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a>EC_WMT_EVENT (Windows SDK de formato multimedia 11)

Enviado por el SDK Windows Media Format cuando una aplicación usa el filtro lector de ASF para reproducir archivos ASF protegidos por administración de derechos digitales (DRM).

Parámetros

*lParam1*

Puede ser uno de los siguientes valores DE ESTADO \_ DE WMT.



| Mensaje DE \_ ESTADO DE WMT           | Descripción                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| WMT \_ NO \_ RIGHTS               | El archivo está protegido con DRM versión 1 y la aplicación no tiene derechos para realizar la acción solicitada.                    |
| ADQUISICIÓN DE LICENCIA DE WMT \_ \_         | Se ha completado el proceso de adquisición de licencias. (Esto no significa necesariamente que una licencia se adquirió correctamente). |
| WMT \_ NO \_ RIGHTS \_ EX           | El archivo está protegido con DRM versión 7 y la aplicación no tiene derechos para realizar la acción solicitada.                    |
| WMT \_ NECESITA \_ INDIVIDUALIZACIÓN | La licencia solo permite que las aplicaciones individualizadas realicen la acción solicitada.                                           |
| WMT \_ INDIVIDUALIZE            | El proceso de individualización se está realizando o se ha completado.                                                    |



 

*lParam2*

Puntero a una estructura DE DATOS DE EVENTOS **\_ DE AM \_ \_ WMT** que contiene información sobre el evento en el puntero de miembro **pData,** así como un código de estado **HRESULT** enviado por el SDK de formato multimedia de Windows. El valor de *lParam2* depende del valor de *lParam1*, como se describe en la tabla siguiente. (Las estructuras \_ "WM" se definen en el SDK Windows Media Format).



| Si lParam1 es...              | AM \_ WMT \_ EVENT \_ DATA.pData es...                            |
|-------------------------------|-------------------------------------------------------------|
| WMT \_ NO \_ RIGHTS               | Puntero a una **cadena WCHAR** que contiene una dirección URL de desafío. |
| ADQUISICIÓN DE LICENCIA DE WMT \_ \_         | Puntero a una **estructura WM GET LICENSE \_ \_ \_ DATA.**        |
| WMT \_ NO \_ RIGHTS \_ EX           | Puntero a una **estructura WM GET LICENSE \_ \_ \_ DATA.**        |
| WMT \_ NECESITA \_ INDIVIDUALIZACIÓN | NULL.                                                       |
| WMT \_ INDIVIDUALIZE            | Puntero a una estructura **WM \_ INDIVIDUALIZE \_ STATUS.**     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digitales**](digital-rights-management-features.md)
</dt> <dt>

[**DirectShow Referencia de QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Habilitación de la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




