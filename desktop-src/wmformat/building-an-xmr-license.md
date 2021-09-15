---
title: Creación de una licencia XMR
description: Creación de una licencia XMR
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows SDK de formato multimedia, importación de DRM
- Windows SDK de formato multimedia, importar
- Windows SDK de formato multimedia, licencias XMR
- Windows SDK de formato multimedia, licencias
- Windows SDK de formato multimedia, derechos multimedia extensibles (XMR)
- digital rights management (DRM),import
- DRM (administración de derechos digitales),importar
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- administración de derechos digitales (DRM), licencias XMR
- DRM (administración de derechos digitales), licencias XMR
- digital rights management (DRM), Extensible Media Rights (XMR)
- DRM (administración de derechos digitales),Derechos multimedia extensibles (XMR)
- API extendidas de cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas de cliente DRM, licencias XMR
- API extendidas de cliente, licencias XMR
- API extendidas de cliente DRM, licencias
- API extendidas de cliente, licencias
- API extendidas de cliente DRM, derechos multimedia extensibles (XMR)
- API extendidas de cliente, derechos multimedia extensibles (XMR)
- licenses,XMR
- Derechos multimedia extensibles (XMR)
- XMR (Derechos multimedia extensibles)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc275419116362c08cabe4dc70aa227687705fdb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467100"
---
# <a name="building-an-xmr-license"></a>Creación de una licencia XMR

Para generar una licencia para Windows DRM de multimedia para procesar, debe usar el esquema binario extensible de derechos multimedia (XMR). XMR es un esquema para transmitir restricciones y derechos de uso multimedia y debe tener licencia por separado.

El material importante de una licencia se cifra mediante la clave pública de la colección de certificados DRM de Windows Media, por lo que solo es visible para el subsistema de API extendida del cliente drm de Windows Media. .

Es su responsabilidad asegurarse de que la estructura de licencias y la configuración de la directiva son válidas y coherentes con la intención del emisor de licencias, y que cumplen las reglas de cumplimiento.

Debe leer las reglas de Windows de cumplimiento de importación de DRM multimedia para obtener información sobre el conjunto completo de objetos XMR que deben estar presentes en la licencia.

Para pasar la licencia XMR al subsistema DRM, llame al [**método IWMDRMLicenseManagement::StoreLicense.**](iwmdrmlicensemanagement-storelicense.md) Use el formato siguiente para pasar la licencia en el *parámetro bstrLicenseResponse:*


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



Esta cadena debe estar en formato Unicode (UTF-16).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Importación de DRM**](drm-import.md)
</dt> </dl>

 

 




