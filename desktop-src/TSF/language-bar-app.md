---
title: Barra de idioma (aplicaciones TSF)
description: Una aplicación no puede agregar elementos a la barra de idioma. solo un servicio de texto puede agregar elementos a la barra de idioma.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Marco de trabajo de servicios de texto (TSF), barra de idioma
- TSF (marco de trabajo de servicios de texto), barra de idioma
- Aplicaciones habilitadas para TSF, barra de idioma
- barra de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef227b29c8b481bfaefc4a218305ba8974fe54e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904968"
---
# <a name="language-bar-tsf-applications"></a>Barra de idioma (aplicaciones TSF)

Una aplicación no puede agregar elementos a la barra de idioma. solo un servicio de texto puede agregar elementos a la barra de idioma. Una aplicación puede afectar al modo en que se muestran determinados elementos de la barra de idioma.

El compartimiento de [ \_ \_ \_ DICTATIONSTAT del compartimiento de GUID](predefined-compartments.md) se usa para indicar el tipo de entrada de voz que la aplicación puede aceptar: entrada de texto directo (dictado) o comandos de voz. De forma predeterminada, el dictado está habilitado y el comando de voz está deshabilitado. Si la aplicación puede aceptar comandos de voz, debe establecer el valor de [comandos de TF \_ \_ habilitado](speech-recognition-constants.md) en el compartimiento del compartimiento de GUID \_ \_ \_ DICTATIONSTAT. Si la aplicación puede aceptar el dictado, debe establecer el \_ \_ valor de TF dict Enabled en el compartimiento del compartimiento de GUID \_ \_ \_ DICTATIONSTAT. Los \_ comandos TF Dictation \_ on o TF \_ en el \_ valor de este compartimiento determinan qué modo (dictación o comando) de entrada de voz está actualmente en.

Si la aplicación admite el almacenamiento persistente de datos de propiedades, debe establecer el compartimiento del [compartimiento de GUID \_ \_ PERSISTMENUENABLED](predefined-compartments.md) en un valor distinto de cero. Esto hace que el servicio de texto de voz habilite el elemento de menú **guardar datos de voz** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo configurar el marco de trabajo de servicios de texto](how-to-set-up-tsf.md)
</dt> <dt>

[Barra de idioma (servicios de texto)](language-bar.md)
</dt> </dl>

 

 




