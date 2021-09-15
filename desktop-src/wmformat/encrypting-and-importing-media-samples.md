---
title: Ejemplos de cifrado e importación de medios
description: Ejemplos de cifrado e importación de medios
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows SDK de formato multimedia, importación de DRM
- Windows SDK de formato multimedia, importar
- Windows SDK de formato multimedia, ejemplos de cifrado de medios
- administración de derechos digitales (DRM),importar
- DRM (administración de derechos digitales),importar
- administración de derechos digitales (DRM), cifrar ejemplos de medios
- DRM (administración de derechos digitales), cifrado de ejemplos de medios
- API extendidas de cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas de cliente DRM, ejemplos de cifrado de medios
- API extendidas de cliente, ejemplos de medios de cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466863"
---
# <a name="encrypting-and-importing-media-samples"></a>Ejemplos de cifrado e importación de medios

Para cada ejemplo multimedia que cifre mediante Windows DRM multimedia, debe generar un valor sal que sea estrictamente mayor que el anterior (aumento monótono). Use el nuevo valor salt para crear una clave de cifrado transitorio aplicando el algoritmo de cifrado SHA-1 al vector de inicialización concatenado con el valor salt.

A continuación, cifre el ejemplo según el algoritmo RC4 mediante la clave transitoria generada. Antes de pasar el ejemplo al SDK, la aplicación debe asociar el valor salt al ejemplo estableciendo un atributo de extensión.

Estos son los pasos para cifrar ejemplos de medios:

1.  Llame al **método QueryInterface** del objeto de ejemplo para obtener la [**interfaz INSSBuffer3.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
2.  Incremente el valor de sal.
3.  Cifre el ejemplo mediante un algoritmo de cifrado RC1. Para el cifrado, cree una clave concatenando el vector de inicialización y el valor salt.
4.  Proporcione el valor salt al SDK mediante una llamada a [**INSSBuffer::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Importación de DRM**](drm-import.md)
</dt> <dt>

[**Ejemplo de cifrado de ejemplo de medios**](media-sample-encryption-example.md)
</dt> </dl>

 

 




