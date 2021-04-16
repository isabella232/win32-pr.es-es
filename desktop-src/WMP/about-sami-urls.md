---
title: Acerca de las direcciones URL de SAMI
description: Acerca de las direcciones URL de SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Modelo de objetos de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio de multimedia accesible sincronizado (SAMI)
- Windows Media Player Mobile, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX de Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX móvil de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- Control ActiveX, intercambio de multimedia accesible sincronizado (SAMI)
- Intercambio de contenido multimedia accesible sincronizado (SAMI), archivos
- SAMI (intercambio de multimedia accesible sincronizado), archivos
- Intercambio de multimedia accesible sincronizado (SAMI), direcciones URL
- SAMI (intercambio de multimedia accesible sincronizado), direcciones URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268591"
---
# <a name="about-sami-urls"></a>Acerca de las direcciones URL de SAMI

Los archivos SAMI se pueden asociar a archivos multimedia digitales mediante una sola dirección URL. Esto se logra mediante *el parámetro de* dirección URL Sami. El parámetro de dirección URL está precedido por la dirección URL base y un signo? . Una dirección URL con un parámetro *Sami* sigue esta sintaxis:

¿ *Dirección URL*? *Sami* = *captionsURL*.

El valor del parámetro URL sigue el nombre del parámetro y un signo igual, como en el ejemplo siguiente:


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



Esta sintaxis de URL se usa normalmente en un hipervínculo o un metarchivo de Windows Media para vincular directamente a las ubicaciones del archivo multimedia digital y del archivo SAMI. Cuando el usuario hace clic en el hipervínculo, Windows Media Player se inicia en modo completo y reproduce el contenido multimedia digital.

Si no se especifica el parámetro de dirección URL *Sami* , Windows Media Player buscará un archivo Sami que esté en la misma ubicación que el archivo multimedia digital y que tenga el mismo nombre de archivo, excepto la extensión de nombre de archivo, que debe ser. SMI. Si este tipo de archivo está presente, se abrirá automáticamente si se ha habilitado la presentación de títulos en el reproductor.

Para habilitar los subtítulos en Windows Media Player, haga clic en el menú **reproducir** , haga clic en **subtítulos y subtítulos optativos** y, a continuación, haga clic **en activado**. Si los subtítulos están habilitados, se mostrarán los títulos contenidos en el archivo SAMI mientras se reproduce el elemento multimedia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




