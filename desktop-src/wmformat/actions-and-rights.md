---
title: Acciones y derechos
description: Acciones y derechos
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- Administración de derechos digitales (DRM), acciones
- DRM (administración de derechos digitales), acciones
- Administración de derechos digitales (DRM), derechos
- DRM (administración de derechos digitales), derechos
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- licencias, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075190"
---
# <a name="actions-and-rights"></a>Acciones y derechos

Cuando un archivo está protegido mediante DRM de Windows Media, su uso está completamente restringido. Se pueden emitir licencias para permitir que los usuarios usen el contenido de maneras específicas. Cada una de las formas en que un usuario puede usar el contenido se describe mediante una acción. Por ejemplo, la reproducción de un archivo en un equipo es una acción.

Se dice que una licencia que habilita una determinada acción concede un derecho. Por ejemplo, una licencia puede conceder el derecho a reproducir contenido en un equipo.

Las acciones y los derechos hacen referencia a las mismas maneras de usar el contenido. La diferencia es que la acción hace referencia al uso mientras el derecho hace referencia al permiso. A pesar de esta distinción, las palabras acción y derecha se usan a menudo indistintamente en esta documentación y en otros documentos que describen Windows Media DRM.

Las acciones controladas por los derechos de DRM de Windows Media se enumeran en la sección de [constantes derechos](rights-constants.md) de esta documentación.

Ciertos métodos de las API extendidas del cliente DRM de Windows Media usan diferentes constantes para hacer referencia a los derechos básicos de DRM. Por ejemplo, el método [**IWMDRMLicenseQuery:: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) usa un conjunto de cadenas específicas de los Estados de licencia. Aunque estas constantes definen cadenas diferentes de las constantes de derechos básicas, hacen referencia a los mismos derechos de la licencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](drmconcepts.md)
</dt> </dl>

 

 




