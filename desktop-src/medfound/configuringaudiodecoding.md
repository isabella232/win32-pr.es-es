---
description: Configuración de la decodificación de audio
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Configuración de la decodificación de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee274fd714065a1c89c9d634dd80de4d59c9eb567d67ed8045d2b89bece87d74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664655"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a>Configuración de la decodificación de audio (Microsoft Media Foundation)

La codificación Windows contenido de Audio multimedia es mucho más fácil que codificar. Después de crear un objeto descodificador de audio, establezca el tipo de entrada mediante el método **IMediaObject::SetInputType** o **IMFTransform::SetInputType.** El tipo de medio que se usa para la entrada del descodificador debe coincidir con el tipo de salida que se usó cuando se codifica el contenido. Esto incluye los datos de formato extendido anexados a la **estructura DESATEX.** Debe asegurarse de que estos datos son correctos, ya que el descodificador no puede procesar muestras sin ellos.

Después de establecer el tipo de entrada, puede configurar las características de descodificador que quiera usar. Las características de descodificador, como las que se usan para la codificación, se establecen mediante los métodos **de IPropertyBag** **o IPropertyStore.**

Una vez establecido el tipo de entrada y configuradas todas las características del descodificador, puede enumerar los tipos de salida admitidos por el descodificador mediante llamadas a **IMediaObject::GetOutputType** o **ATRANSFORMTransform::GetOutputType.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con audio](workingwithaudio.md)
</dt> </dl>

 

 



