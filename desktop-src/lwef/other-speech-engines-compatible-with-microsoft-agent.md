---
title: Otros motores de voz compatibles con Microsoft Agent
description: Otros motores de voz compatibles con Microsoft Agent
ms.assetid: fa87c592-c819-4dea-a1d0-6ccb25cc0bcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521a236c08904c731035b709a808dc28b31bfb8e6664c07b0e6feb395dee469f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247136"
---
# <a name="other-speech-engines-compatible-with-microsoft-agent"></a>Otros motores de voz compatibles con Microsoft Agent

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Además de los motores de voz de Microsoft que se proporcionan con y admiten Microsoft Agent, varias empresas también ofrecen motores de voz con soporte técnico para Microsoft Agent. En esta página se proporciona una breve introducción a estos motores que pueden estar disponibles en inglés de EE. UU. y otros idiomas. Puede encontrar información sobre cómo instalar y acceder a ellos, así como licencias y redistribuciones de los motores en sus sitios web.

Al usar cualquier motor de voz de terceros, también debe instalar los archivos binarios en tiempo de ejecución de Microsoft SAPI 4.0a para que los motores se enumere correctamente. Desde la página web puede incluir la etiqueta siguiente para desencadenar una descarga automática de la Speech API:

``` syntax
<OBJECT WIDTH=0 HEIGHT=0
  CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
  CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

Para obtener más información sobre los archivos binarios del entorno de ejecución de SAPI, consulte el sitio web del [grupo de Voz de Microsoft](https://msdn.microsoft.com/library/ee705648.aspx). Microsoft Agent también instala los archivos binarios del entorno de ejecución de SAPI con el motor de reconocimiento de voz de Microsoft, el Panel de control voz y el Editor de caracteres del agente.

Tenga en cuenta que estos vínculos apuntan a servidores que no están bajo control de Microsoft. Lea la declaración oficial de Microsoft [sobre](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) otros servidores. Microsoft no aprueba el contenido ni el software proporcionado en estos sitios web. Todas las preguntas técnicas y de soporte técnico también deben dirigirse a los proveedores de los motores y no a Microsoft ni al equipo de Microsoft Agent.

**Motor digalo de texto a voz**

Digalo es un motor de TTS asequible diseñado para usuarios finales y desarrolladores. El motor se ofrece en varios idiomas: francés, alemán, portugués (Brasil), español, ruso e inglés de Reino Unido y Estados Unidos, con italiano, polaco y otros idiomas próximamente. También está disponible información para desarrolladores, así como detalles sobre el registro de usuarios finales y los programas afiliadas.

**Elan Speech Engine**

Elan Speech Engine usa la tecnología Text To Speech de Elan y está disponible en siete idiomas: francés, alemán, portugués (Brasil), español, ruso, reino unido e inglés de EE. UU.

**IBM ViaVoice Outloud**

IBM ha desarrollado varios caracteres de Microsoft Agent para su uso con ViaVoice Outloud. IBM ViaVoice Outloud es una tecnología de texto a voz (síntesis de voz) y está disponible en francés, alemán, italiano, español, inglés del Reino Unido e inglés de Estados Unidos. Cuando se combina con Microsoft Agent, puede crear aplicaciones dinámicas en muchos idiomas y ampliar sus oportunidades de ventas a nuevos mercados internacionales.

 

 




