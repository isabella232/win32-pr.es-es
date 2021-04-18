---
description: La API de XAPO permite la creación de objetos de procesamiento de audio multiplataforma (XAPO) para su uso en XAudio2 en Windows y Xbox 360.
ms.assetid: 4fe88a0f-0234-462f-b575-e592f2c8401e
title: Información general de XAPO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31e2372790e26b7fcd3d15019797185ba180d668
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717139"
---
# <a name="xapo-overview"></a>Información general de XAPO

La API de XAPO permite la creación de objetos de procesamiento de audio multiplataforma (XAPO) para su uso en XAudio2 en Windows y Xbox 360. Un XAPO es un objeto que toma los datos de audio entrantes y realiza alguna operación en los datos antes de pasarlos. Puede usar un XAPO para realizar diversas tareas, como agregar la reverberación a una secuencia de audio y supervisar los niveles de volumen máximo.

## <a name="creating-new-xapos"></a>Crear nuevo XAPOs

La API de XAPO proporciona la interfaz [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) y la clase [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) para crear nuevos tipos XAPO. La interfaz **IXAPO** contiene todos los métodos que deben implementarse para crear un nuevo XAPO. La clase **CXAPOBase** proporciona una implementación básica de la interfaz **IXAPO** . **CXAPOBase** implementa todos los métodos de interfaz **IXAPO** , excepto el método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , que es único para cada XAPO.

Para obtener un ejemplo de cómo crear un nuevo XAPO, consulte [Cómo: crear un xapo](how-to--create-an-xapo.md).

Para obtener un ejemplo de cómo crear un XAPO que acepte parámetros en tiempo de ejecución, consulte [Cómo: agregar compatibilidad con parámetros en tiempo de ejecución a un xapo](how-to--add-run-time-parameter-support-to-an-xapo.md).

## <a name="xapos-and-com"></a>XAPOs y COM

XAPOs implementa la interfaz **IUnknown** . Las interfaces [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) y [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluyen los tres métodos **IUnknown** : **QueryInterface**, **AddRef** y **Release**. [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) proporciona implementaciones de los tres métodos IUnknown. Una nueva instancia de **CXAPOBase** tendrá un recuento de referencias de 1. Se destruirá cuando su recuento de referencias se convierta en 0. Las implementaciones de **IXAPO** y **IXAPOParameters** deben seguir el mismo patrón para permitir su administración adecuada cuando se usan con XAudio2.

Las instancias de XAPO se pasan a XAudio2 como interfaces **IUnknown** . XAudio2 usa **QueryInterface** para adquirir una interfaz [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) y detectar si el XAPO implementa la interfaz [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) . Las implementaciones de **IXAPO** deben aceptar solicitudes para **\_ \_ uuidof (IXAPO)**. Si se implementa **IXAPOParameters** , también debe aceptar solicitudes para **\_ \_ uuidof (IXAPOParameters)**.

## <a name="using-an-xapo-in-xaudio2"></a>Uso de un XAPO en XAudio2

Los XAPOs se usan en XAudio2 mediante su asociación a las voces. Cada voz de XAudio2 tiene una cadena de efectos que contiene cero o más efectos de audio. Los datos de audio enviados a una voz se pasan a través de cada efecto de la cadena antes de que se envíen a los destinos de salida de la voz. Los datos se pasan de la voz a cada efecto mediante el parámetro *pInputProcessParameters* del método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) . Después, se devuelve a la voz mediante el parámetro *pOutputProcessParameters* . La voz toma el resultado de cada efecto y lo alimenta en el siguiente efecto de la cadena hasta que no quede ningún efecto en la cadena.

Para más información sobre las cadenas de efectos de XAudio2, consulte [efectos de audio de xaudio2](xaudio2-audio-effects.md).

Para ver un ejemplo del uso de un XAPO en XAudio2, consulte [Cómo: usar un xapo en xaudio2](how-to--use-an-xapo-in-xaudio2.md).

## <a name="effect-libraries"></a>Bibliotecas de efectos

La biblioteca de efectos de XAPO contiene varios XAPOs y un método común para crear instancias de ellos. Consulte información [General sobre XAPOFX](xapofx-overview.md) para obtener información sobre XAPOFX. Además, XAudio2 tiene efectos de la reverberación y el medidor de volumen integrados. Consulte [efectos de audio de xaudio2](xaudio2-audio-effects.md) para más información sobre los efectos de xaudio2 integrados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos de audio](audio-effects.md)
</dt> <dt>

[Efectos de audio de XAudio2](xaudio2-audio-effects.md)
</dt> </dl>

 

 
