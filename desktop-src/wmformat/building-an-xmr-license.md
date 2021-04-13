---
title: Creación de una licencia de XMR
description: Creación de una licencia de XMR
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- SDK de Windows Media Format, importación de DRM
- SDK de Windows Media Format, importar
- SDK de Windows Media Format, licencias de XMR
- SDK de Windows Media Format, licencias
- SDK de Windows Media Format, derechos de medios extensibles (XMR)
- Administración de derechos digitales (DRM), importar
- DRM (administración de derechos digitales), importar
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), licencias de XMR
- DRM (administración de derechos digitales), licencias de XMR
- Administración de derechos digitales (DRM), derechos de medios extensibles (XMR)
- DRM (administración de derechos digitales), derechos multimedia extensibles (XMR)
- API extendidas del cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas del cliente DRM, licencias de XMR
- API extendidas de cliente, licencias de XMR
- API extendidas del cliente DRM, licencias
- API extendidas del cliente, licencias
- API extendidas del cliente DRM, derechos multimedia extensibles (XMR)
- API extendidas de cliente, derechos multimedia extensibles (XMR)
- licencias, XMR
- Derechos de medios extensibles (XMR)
- XMR (derechos multimedia extensible)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc275419116362c08cabe4dc70aa227687705fdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418372"
---
# <a name="building-an-xmr-license"></a>Creación de una licencia de XMR

Para generar una licencia para el procesamiento de DRM de Windows Media, debe usar el esquema binario de manextensible Media Rights (XMR). XMR es un esquema para transmitir derechos y restricciones de uso de medios y debe tener licencia por separado.

El material importante de una licencia se cifra mediante la clave pública de la colección de certificados DRM de Windows Media, por lo que solo es visible para el subsistema de API extendida del cliente DRM de Windows Media. .

Es responsabilidad suya asegurarse de que la configuración de la Directiva y la estructura de licencias son válidas y coherentes con la intención del emisor de la licencia y que se ajustan a las reglas de cumplimiento.

Debe leer las reglas de cumplimiento de importación de DRM de Windows Media para obtener información sobre el conjunto completo de objetos XMR que deben estar presentes en la licencia.

Para pasar la licencia de XMR al subsistema DRM, llame al método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) . Use el formato siguiente para pasar la licencia en el parámetro *bstrLicenseResponse* :


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



Esta cadena debe tener el formato Unicode (UTF-16).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Importación de DRM**](drm-import.md)
</dt> </dl>

 

 




