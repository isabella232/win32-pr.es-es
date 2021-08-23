---
description: La API de XAPO permite la creación de objetos de procesamiento de audio (XAPO) multiplataforma para su uso en XAudio2 tanto en Windows como Xbox 360.
ms.assetid: 4fe88a0f-0234-462f-b575-e592f2c8401e
title: Información general de XAPO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9ee64e865c8e3ef3cdac026274b922db438a54979dcb30d855a92b96e4e0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589915"
---
# <a name="xapo-overview"></a>Información general de XAPO

La API de XAPO permite la creación de objetos de procesamiento de audio (XAPO) multiplataforma para su uso en XAudio2 tanto en Windows como Xbox 360. Un XAPO es un objeto que toma datos de audio entrantes y realiza alguna operación en los datos antes de pasarlo. Puede usar un XAPO para realizar diversas tareas, como agregar reverberación a una secuencia de audio y supervisar los niveles de volumen máximo.

## <a name="creating-new-xapos"></a>Creación de nuevos XAPOs

La API de XAPO proporciona la [**interfaz IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) y la [**clase CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) para crear nuevos tipos XAPO. La **interfaz IXAPO** contiene todos los métodos que deben implementarse para crear un nuevo XAPO. La **clase CXAPOBase** proporciona una implementación básica de la **interfaz IXAPO.** **CXAPOBase** implementa todos los métodos de interfaz **IXAPO,** excepto el método [**IXAPO::P rocess,**](/windows/win32/api/xapo/nf-xapo-ixapo-process) que es único para cada XAPO.

Para obtener un ejemplo de cómo crear un nuevo XAPO, [vea Cómo: Crear un XAPO.](how-to--create-an-xapo.md)

Para obtener un ejemplo de creación de un XAPO que acepta parámetros en tiempo de ejecución, vea Cómo: Agregar compatibilidad con parámetros en tiempo de ejecución [a un XAPO.](how-to--add-run-time-parameter-support-to-an-xapo.md)

## <a name="xapos-and-com"></a>XAPOs y COM

Los XAPO implementan **la interfaz IUnknown.** Las [**interfaces IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluyen los tres métodos **IUnknown:** **QueryInterface,** **AddRef** y **Release.** [**CXAPOBase proporciona**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) implementaciones de los tres métodos IUnknown. Una nueva instancia de **CXAPOBase** tendrá un recuento de referencias de 1. Se destruirá cuando su recuento de referencias se convierta en 0. Las implementaciones **de IXAPO** e **IXAPOParameters** deben seguir el mismo patrón para permitir su administración adecuada cuando se usa con XAudio2.

Las instancias de XAPO se pasan a XAudio2 como interfaces **IUnknown.** XAudio2 usa **QueryInterface para** adquirir una [**interfaz IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) y detectar si XAPO implementa la [**interfaz IXAPOParameters.**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) Las implementaciones **de IXAPO** deben aceptar solicitudes **\_ \_ para uuidof(IXAPO).** Si **se implementa IXAPOParameters,** también debe aceptar solicitudes para **\_ \_ uuidof(IXAPOParameters).**

## <a name="using-an-xapo-in-xaudio2"></a>Uso de un XAPO en XAudio2

Los XAPO se usan en XAudio2 asociándolos a voces. Cada voz XAudio2 tiene una cadena de efectos que contiene cero o más efectos de audio. Los datos de audio enviados a una voz se pasan a través de cada efecto de la cadena antes de que se envíen a los destinos de salida de la voz. Los datos se pasan de la voz a cada efecto mediante el parámetro *pInputProcessParameters* del [**método IXAPO::P rocess.**](/windows/win32/api/xapo/nf-xapo-ixapo-process) A continuación, se devuelve a la voz mediante *el parámetro pOutputProcessParameters.* La voz toma la salida de cada efecto y la alimenta al siguiente efecto de la cadena hasta que no se deja ningún efecto en la cadena.

Para obtener más información sobre las cadenas de efectos de XAudio2, vea [Efectos de audio XAudio2](xaudio2-audio-effects.md).

Para obtener un ejemplo del uso de un XAPO en XAudio2, vea Cómo: Usar un [XAPO en XAudio2.](how-to--use-an-xapo-in-xaudio2.md)

## <a name="effect-libraries"></a>Bibliotecas de efectos

La biblioteca de efectos XAPO contiene varios XAPO y un método común para crear instancias de ellos. Consulte [Información general de XAPOFX](xapofx-overview.md) para obtener información sobre XAPOFX. Además, XAudio2 tiene efectos integrados de reverberación y medidor de volumen. Consulte [Efectos de audio XAudio2](xaudio2-audio-effects.md) para obtener más información sobre los efectos integrados de XAudio2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Efectos de audio de XAudio2](xaudio2-audio-effects.md)
</dt> </dl>

 

 
