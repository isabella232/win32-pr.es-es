---
title: Consulta para obtener información detallada sobre los derechos
description: Consulta para obtener información detallada sobre los derechos
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- SDK de Windows Media Format, consultando los derechos detallados
- SDK de Windows Media Format, consultas de derechos detalladas
- Administración de derechos digitales (DRM), consulta de los derechos detallados
- DRM (administración de derechos digitales), consulta de los derechos detallados
- Administración de derechos digitales (DRM), consultas de derechos detalladas
- DRM (administración de derechos digitales), consultas de derechos detalladas
- API extendidas del cliente DRM, consultando los derechos detallados
- API extendidas del cliente, consultar los derechos detallados
- API extendidas del cliente DRM, consultas de derechos detalladas
- API extendidas de cliente, consultas de derechos detalladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a21fa974f0289c4e4e8983ee6d4fd1757de824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268875"
---
# <a name="querying-for-detailed-rights-information"></a>Consulta para obtener información detallada sobre los derechos

Mediante el método [**IWMDRMLicenseQuery:: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) , puede obtener información detallada sobre los derechos concedidos por las licencias para un identificador de clave. La información que se obtiene de este método se agrega desde todas las licencias del almacén de licencias local que se aplican al identificador de clave especificado.

**QueryLicenseState** usa la estructura de [**\_ datos de \_ estado \_**](drmdrm-license-state-data.md) de la licencia de DRM para mostrar información agregada sobre todas las licencias para el identificador de clave especificado. Este uso es diferente de otros objetos del SDK de Windows Media Format.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Obtención de información de licencias en el almacén de licencias local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




