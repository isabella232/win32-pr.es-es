---
title: Acciones y derechos
description: Acciones y derechos
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- Windows SDK de formato multimedia, administración de derechos digitales (DRM)
- Windows SDK de formato multimedia, licencias DRM
- Windows SDK de formato multimedia, licencias para DRM
- administración de derechos digitales (DRM), acciones
- DRM (administración de derechos digitales), acciones
- administración de derechos digitales (DRM), derechos
- DRM (administración de derechos digitales), derechos
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- licencias, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b822c0350af12c5e266570a031ca0d3eda7c99b4b8451b751786a60a4a0908d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089775"
---
# <a name="actions-and-rights"></a>Acciones y derechos

Cuando un archivo está protegido mediante drm Windows multimedia, su uso está completamente restringido. Se pueden emitir licencias para permitir que un usuario use el contenido de maneras específicas. Cada forma en que un usuario puede usar el contenido se describe mediante una acción. Por ejemplo, reproducir un archivo en un equipo es una acción.

Se dice que una licencia que habilita una acción determinada concede un derecho. Por ejemplo, una licencia puede conceder el derecho a reproducir contenido en un equipo.

Las acciones y los derechos hacen referencia a las mismas formas de usar contenido. La diferencia es que la acción hace referencia al uso, mientras que el derecho hace referencia al permiso. A pesar de esta distinción, las palabras acción y derecho se suelen usar indistintamente en esta documentación y en otros documentos que describen Windows DRM multimedia.

Las acciones que se rigen por Windows derechos DRM de multimedia se enumeran en la sección [Constantes de](rights-constants.md) derechos de esta documentación.

Determinados métodos de Windows API extendidas de cliente DRM multimedia usan constantes diferentes para hacer referencia a los derechos drm básicos. Por ejemplo, el [**método IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) usa un conjunto de cadenas específicas de los estados de licencia. Aunque estas constantes definen cadenas diferentes de las constantes de derechos básicos, hacen referencia a los mismos derechos en la licencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](drmconcepts.md)
</dt> </dl>

 

 




