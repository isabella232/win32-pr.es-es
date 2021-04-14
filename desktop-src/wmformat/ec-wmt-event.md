---
title: EC_WMT_EVENT (Windows Media Format 11 SDK)
description: '\_evento WMT de EC \_'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- SDK de Windows Media Format, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- Administración de derechos digitales (DRM), EC_WMT_EVENT
- DRM (administración de derechos digitales), EC_WMT_EVENT
- Advanced Systems Format (ASF), EC_WMT_EVENT
- ASF (formato de sistemas avanzados), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488747"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a>EC_WMT_EVENT (Windows Media Format 11 SDK)

Lo envía el SDK de Windows Media Format cuando una aplicación usa el filtro de lector ASF para reproducir archivos ASF protegidos por la administración de derechos digitales (DRM).

Parámetros

*lParam1*

Puede ser uno de los siguientes valores de estado de WMT \_ .



| Mensaje de estado de WMT \_           | Descripción                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| \_sin \_ derechos de WMT               | El archivo está protegido con DRM versión 1 y la aplicación no tiene derechos para realizar la acción solicitada.                    |
| \_licencia de adquisición de WMT \_         | Se ha completado el proceso de adquisición de licencias. (Esto no significa necesariamente que se haya adquirido una licencia correctamente). |
| \_no hay \_ derechos de WMT \_ ex           | El archivo está protegido con DRM versión 7 y la aplicación no tiene derechos para realizar la acción solicitada.                    |
| WMT \_ necesita la \_ individualización | La licencia permite que solo las aplicaciones individuales realicen la acción solicitada.                                           |
| individual de WMT \_            | Ahora se está llevando a cabo el proceso de individualización o se ha completado.                                                    |



 

*lParam2*

Puntero a una estructura de **\_ \_ \_ datos de evento WMT de AM** que contiene información sobre el evento en el puntero de miembro de **pdata** , así como un código de estado **HRESULT** enviado por el SDK de Windows Media Format. El valor de *lParam2* depende del valor de *lParam1*, como se describe en la tabla siguiente. (Las estructuras "WM \_ " se definen en el SDK de Windows Media Format).



| Si lParam1 es...              | AM \_ \_ datos de evento WMT \_ . pdata es...                            |
|-------------------------------|-------------------------------------------------------------|
| \_sin \_ derechos de WMT               | Puntero a una cadena **WCHAR** que contiene una dirección URL de desafío. |
| \_licencia de adquisición de WMT \_         | Un puntero a una estructura de **datos de licencia de Get de WM \_ \_ \_** .        |
| \_no hay \_ derechos de WMT \_ ex           | Un puntero a una estructura de **datos de licencia de Get de WM \_ \_ \_** .        |
| WMT \_ necesita la \_ individualización | NULL.                                                       |
| individual de WMT \_            | Un puntero a una estructura de estado de la **\_ \_ individualización de WM** .     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Referencia de QASF de DirectShow**](directshow-qasf-reference.md)
</dt> <dt>

[**Habilitar la compatibilidad con DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




