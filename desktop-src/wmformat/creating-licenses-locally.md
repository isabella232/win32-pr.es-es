---
title: Crear licencias localmente
description: Crear licencias localmente
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- SDK de Windows Media Format, crear licencias localmente
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), creación de licencias localmente
- DRM (administración de derechos digitales), crear licencias localmente
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas del cliente DRM, creación de licencias localmente
- API extendidas del cliente, crear licencias localmente
- licencias, crear licencias localmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fc4305c77be2132611df925ae08458fe2bb4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076341"
---
# <a name="creating-licenses-locally"></a>Crear licencias localmente

En determinadas circunstancias, como durante la [importación de DRM](drm-import.md), puede crear sus propias licencias. Las licencias de DRM de Windows Media se pueden escribir de varias maneras diferentes, pero para crear su propia licencia debe usar el esquema binario de derechos de multimedia extensible (XMR). Para obtener más información, consulte [Building a XMR License](building-an-xmr-license.md).

Al crear una licencia, puede agregarla al almacén de licencias local llamando al método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adquisición de licencias**](acquiring-licenses.md)
</dt> <dt>

[**Creación de una licencia de XMR**](building-an-xmr-license.md)
</dt> </dl>

 

 




