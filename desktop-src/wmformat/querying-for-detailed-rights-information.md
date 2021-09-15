---
title: Consulta de información detallada sobre los derechos
description: Consulta de información detallada sobre los derechos
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- Windows SDK de formato multimedia, consulta de derechos detallados
- Windows SDK de formato multimedia, consultas de derechos detalladas
- administración de derechos digitales (DRM), consulta de derechos detallados
- DRM (administración de derechos digitales), consulta de derechos detallados
- administración de derechos digitales (DRM), consultas de derechos detalladas
- DRM (administración de derechos digitales), consultas de derechos detalladas
- API extendidas de cliente DRM, consulta de derechos detallados
- API extendidas de cliente, consulta de derechos detallados
- API extendidas de cliente DRM, consultas de derechos detalladas
- API extendidas de cliente, consultas de derechos detalladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a21fa974f0289c4e4e8983ee6d4fd1757de824
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466685"
---
# <a name="querying-for-detailed-rights-information"></a>Consulta de información detallada sobre los derechos

Mediante el [**método IWMDRMLicenseQuery::QueryLicenseState,**](iwmdrmlicensequery-querylicensestate.md) puede obtener información detallada sobre los derechos concedidos por las licencias para un identificador de clave. La información que obtiene de este método se agrega de todas las licencias del almacén de licencias local que se aplican al identificador de clave especificado.

**QueryLicenseState usa** la estructura [**DRM LICENSE STATE \_ \_ \_ DATA**](drmdrm-license-state-data.md) para mostrar información agregada sobre todas las licencias para el identificador de clave especificado. Este uso es diferente del de otros objetos del SDK Windows Media Format.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Obtención de información de licencias en el almacén de licencias local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




