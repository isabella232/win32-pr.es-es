---
title: Acerca de las direcciones URL de SAMI
description: Acerca de las direcciones URL de SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Reproductor de Windows Media,Synchronized Accessible Media Interchange (SAMI)
- Reproductor de Windows Media modelo de objetos, Intercambio multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio multimedia accesible sincronizado (SAMI)
- Reproductor de Windows Media Intercambio multimedia accesible móvil y sincronizado (SAMI)
- Reproductor de Windows Media ActiveX control,Intercambio multimedia accesible sincronizado (SAMI)
- Reproductor de Windows Media Control de ActiveX móviles, intercambio multimedia accesible sincronizado (SAMI)
- ActiveX control,Intercambio multimedia accesible sincronizado (SAMI)
- Intercambio multimedia accesible sincronizado (SAMI),files
- SAMI (intercambio multimedia accesible sincronizado), archivos
- Intercambio multimedia accesible sincronizado (SAMI), direcciones URL
- SAMI (intercambio de medios accesible sincronizado), direcciones URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a35976c6988ad4298c812005002da010730d5254bd7c010f24fe32741be393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956805"
---
# <a name="about-sami-urls"></a>Acerca de las direcciones URL de SAMI

Los archivos SAMI se pueden asociar a archivos multimedia digitales mediante una sola dirección URL. Esto se logra mediante el parámetro *sami* URL. El parámetro URL va precedido de la dirección URL base y un ? . Una dirección URL con *un parámetro sami* sigue esta sintaxis:

*¿Dirección URL?* *sami* = *captionsURL*.

El valor del parámetro URL sigue el nombre del parámetro y un signo igual, como en el ejemplo siguiente:


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



Esta sintaxis de dirección URL se usa normalmente en un hipervínculo o un metarchivo multimedia de Windows para vincular directamente a las ubicaciones del archivo multimedia digital y del archivo SAMI. Cuando el usuario hace clic en el hipervínculo, Reproductor de Windows Media se inicia en modo completo y reproduce el contenido multimedia digital.

Si no se especifica el parámetro *sami* URL, Reproductor de Windows Media buscará un archivo SAMI que se encuentra en la misma ubicación que el archivo multimedia digital y que tenga el mismo nombre de archivo, excepto la extensión de nombre de archivo, que debe ser .smi. Si este tipo de archivo está presente, se abrirá automáticamente si se ha habilitado la visualización de títulos en el reproductor.

Los títulos cerrados se habilitan  en Reproductor de Windows Media en el menú Reproducir, después en Títulos y **subtítulos** y, a continuación, en **En**. Si los títulos cerrados están habilitados, los títulos contenidos en el archivo SAMI se mostrarán mientras se reproduce el elemento multimedia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




