---
title: Cifrado e importación de ejemplos de medios
description: Cifrado e importación de ejemplos de medios
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- SDK de Windows Media Format, importación de DRM
- SDK de Windows Media Format, importar
- SDK de Windows Media Format, cifrado de ejemplos de medios
- Administración de derechos digitales (DRM), importar
- DRM (administración de derechos digitales), importar
- Administración de derechos digitales (DRM), cifrado de muestras de medios
- DRM (administración de derechos digitales), cifrar ejemplos de medios
- API extendidas del cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas del cliente DRM, cifrado de ejemplos de medios
- API extendidas de cliente, cifrado de ejemplos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420256"
---
# <a name="encrypting-and-importing-media-samples"></a>Cifrado e importación de ejemplos de medios

Para cada ejemplo multimedia que cifre con DRM de Windows Media, debe generar un valor Salt que sea estrictamente mayor que el anterior (aumentando de forma continua). Use el nuevo valor Salt para crear una clave de cifrado transitoria aplicando el algoritmo de cifrado SHA-1 al vector de inicialización concatenado con el valor Salt.

A continuación, Cifre el ejemplo según el algoritmo RC4 mediante la clave transitoria generada. Antes de pasar el ejemplo al SDK, la aplicación debe asociar el valor Salt al ejemplo estableciendo un atributo de extensión.

Estos son los pasos para cifrar ejemplos de medios:

1.  Llame al método **QueryInterface** del objeto de ejemplo para obtener la interfaz [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .
2.  Incremente el valor Salt.
3.  Cifre el ejemplo con un algoritmo de cifrado RC1. Para el cifrado, cree una clave concatenando el vector de inicialización y el valor Salt.
4.  Proporcione el valor Salt al SDK llamando a [**INSSBuffer:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Importación de DRM**](drm-import.md)
</dt> <dt>

[**Ejemplo de cifrado de ejemplo multimedia**](media-sample-encryption-example.md)
</dt> </dl>

 

 




