---
title: Crear licencias localmente
description: Crear licencias localmente
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- Windows SDK de formato multimedia, creación de licencias localmente
- Windows SDK de formato multimedia, licencias
- administración de derechos digitales (DRM), creación de licencias localmente
- DRM (administración de derechos digitales), creación de licencias localmente
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas de cliente DRM, creación de licencias localmente
- API extendidas de cliente, creación de licencias localmente
- licenses,creating licenses locally
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda1a889e83f093cbd60043b299b7174a6c963663962a66454c5707060e76232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433911"
---
# <a name="creating-licenses-locally"></a>Crear licencias localmente

En determinadas circunstancias, como durante la importación [de DRM,](drm-import.md)puede crear sus propias licencias. Windows Las licencias DRM de medios se pueden escribir de varias maneras diferentes, pero para crear su propia licencia, debe usar el esquema binario Extensible Media Rights (XMR). Para obtener más información, vea [Building an XMR License](building-an-xmr-license.md).

Al crear una licencia, puede agregarla al almacén de licencias local llamando al método [**IWMDRMLicenseManagement::StoreLicense.**](iwmdrmlicensemanagement-storelicense.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adquisición de licencias**](acquiring-licenses.md)
</dt> <dt>

[**Creación de una licencia XMR**](building-an-xmr-license.md)
</dt> </dl>

 

 




