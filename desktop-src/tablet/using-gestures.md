---
description: Información general sobre el uso de gestos.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Uso de gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c4748dbf2638a57e005562fdec735ea6e87c27757d46549b7577f3bed7741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449257"
---
# <a name="using-gestures"></a>Uso de gestos

La plataforma tablet PC proporciona el reconocedor de gestos de Microsoft para admitir gestos de aplicación. Para obtener una lista de los gestos admitidos por el reconocedor de gestos de Microsoft, consulte la tabla de gestos de aplicación en la [**enumeración ApplicationGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) Tablet PC también admite gestos del sistema. Para obtener una lista de los gestos del sistema admitidos por tablet PC, consulte la tabla de gestos del sistema en la [**enumeración SystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)

## <a name="microsoft-gesture-recognizer"></a>Reconocedor de gestos de Microsoft

Puede emplear el reconocedor de gestos de Microsoft mediante la propiedad [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) del objeto [**InkCollector,**](inkcollector-class.md) el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture.](inkpicture-control-reference.md) Al establecer **la propiedad CollectionMode** en modo mixto **(InkAndGesture)** o en modo de solo gesto **(GestureOnly)** se pasa la entrada de lápiz al reconocedor de gestos de Microsoft de forma predeterminada. Puede emplear el reconocedor de gestos de Microsoft con el control [InkEdit](inkedit-control-reference.md) estableciendo la [**propiedad InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) en **InkAndGesture**. También puede usar el reconocimiento de gestos con el objeto [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) agregando un objeto [**GestureRecognizer**](gesturerecognizer-class.md) a una de sus colecciones de complementos.

Sin embargo, si la versión actual del reconocedor de gestos de Microsoft no admite los gestos que quiere usar, puede crear su propio reconocedor y usarlo junto con el reconocedor de gestos de Microsoft. Esto permite la compatibilidad completa con los gestos de la aplicación.

Tablet PC usa un lápiz para algunas o todas las entradas. Esto facilita enormemente la escritura de la entrada de lápiz. La plataforma tablet PC ofrece arquitectura para la entrada de lápiz que admite una estructura en capas de gestos. Los gestos y la asignación se definen para permitir que el usuario escriba e invoque gestos avanzados en nuevas superficies, al tiempo que se reservan gestos que invocan mensajes tradicionales del mouse de otras aplicaciones basadas en Windows datos.

La plataforma tablet PC presenta dos niveles de gestos: gestos del sistema, también conocidos como eventos del sistema, y gestos de aplicación. La arquitectura de lápiz admite gestos del sistema y de la aplicación. Se admiten los gestos de aplicación de un solo trazo y de varios trazos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gestos de aplicación](application-gestures.md)
</dt> <dt>

[Gestos de gestos de gestos](flicks-gestures.md)
</dt> <dt>

[Gestos del sistema](system-gestures.md)
</dt> </dl>

 

 



