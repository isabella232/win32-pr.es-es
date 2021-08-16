---
title: Barra de lenguaje (aplicaciones de TSF)
description: Una aplicación no puede agregar elementos a la barra de idioma; solo un servicio de texto puede agregar elementos a la barra de idioma.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Text Services Framework (TSF),barra de idioma
- TSF (Text Services Framework),barra de idioma
- Aplicaciones habilitadas para TSF, barra de lenguaje
- barra de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0adeacdfe105700efba761b0622432f4ac382d147bd82145242be9fdd71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952113"
---
# <a name="language-bar-tsf-applications"></a>Barra de lenguaje (aplicaciones de TSF)

Una aplicación no puede agregar elementos a la barra de idioma; solo un servicio de texto puede agregar elementos a la barra de idioma. Una aplicación puede afectar al modo en que aparecen determinados elementos de la barra de idioma.

El [compartimiento GUID COMPARTMENT SPEECH \_ \_ \_ DICTATIONSTAT](predefined-compartments.md) se usa para indicar el tipo de entrada de voz que la aplicación puede aceptar: entrada de texto directo (dictado) o comandos de voz. De forma predeterminada, el dictado está habilitado y el comando de voz está deshabilitado. Si la aplicación puede aceptar comandos de voz, debe establecer el valor [TF \_ COMMANDING \_ ENABLED](speech-recognition-constants.md) en el compartimiento GUID \_ COMPARTMENT SPEECH \_ \_ DICTATIONSTAT. Si la aplicación puede aceptar dictado, debe establecer el valor TF DICTATION ENABLED en el compartimiento \_ \_ GUID COMPARTMENT SPEECH \_ \_ \_ DICTATIONSTAT. El valor TF DICTATION ON o TF COMMANDING ON de este compartimiento determina en qué modo (dictado o comando) se encuentra actualmente \_ \_ la entrada de \_ \_ voz.

Si la aplicación admite el almacenamiento persistente de datos de propiedad, debe establecer el compartimiento [ \_ GUID COMPARTMENT \_ PERSISTMENUENABLED](predefined-compartments.md) en un valor distinto de cero. Esto hace que el servicio de texto de voz habilite el **elemento de menú Guardar** datos de voz.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de Text Services Framework](how-to-set-up-tsf.md)
</dt> <dt>

[Barra de idioma (Text Services)](language-bar.md)
</dt> </dl>

 

 




