---
description: Información general sobre el uso de gestos.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Usar gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001113"
---
# <a name="using-gestures"></a>Usar gestos

La plataforma de Tablet PC proporciona el reconocedor de gestos de Microsoft para admitir los gestos de aplicación. Para obtener una lista de los gestos admitidos por el reconocedor de gestos de Microsoft, consulte la tabla de gestos de aplicación en la enumeración [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) . Tablet PC también admite gestos del sistema. Para obtener una lista de los gestos del sistema compatibles con Tablet PC, vea la tabla de gestos del sistema en la enumeración [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .

## <a name="microsoft-gesture-recognizer"></a>Reconocedor de gestos de Microsoft

Puede emplear el reconocedor de gestos de Microsoft mediante la propiedad [**si CollectionMode es**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) del objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) . De forma predeterminada, al establecer la propiedad **si CollectionMode es** en modo mixto (**InkAndGesture**) o en modo de solo gesto (**GestureOnly**), se pasa la entrada manuscrita al reconocedor de gestos de Microsoft. Puede emplear el reconocedor de gestos de Microsoft con el control [InkEdit](inkedit-control-reference.md) si establece la propiedad [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) en **InkAndGesture**. También puede usar el reconocimiento de gestos con el objeto [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) agregando un objeto [**GestureRecognizer**](gesturerecognizer-class.md) a una de sus colecciones de complementos.

Sin embargo, si los gestos que quiere usar no son compatibles con la versión actual del reconocedor de gestos de Microsoft, puede crear su propio reconocedor y usarlo junto con el reconocedor de gestos de Microsoft. Esto permite la compatibilidad total con los gestos de la aplicación.

Tablet PC usa un lápiz para algunos o todos los datos de entrada. Esto facilita enormemente la escritura de tinta. La plataforma de Tablet PC ofrece una arquitectura para la entrada manuscrita que admite una estructura en capas de gestos. Los gestos y la asignación se definen para permitir que el usuario escriba e invoque gestos avanzados en nuevas superficies, al tiempo que se reservan gestos que invoquen los mensajes de mouse tradicionales de otras aplicaciones basadas en Windows.

La plataforma de Tablet PC presenta dos niveles de gestos: gestos del sistema, también conocidos como eventos del sistema y gestos de aplicación. La arquitectura del lápiz admite movimientos del sistema y de la aplicación. Se admiten los movimientos de aplicación de un solo trazo y de varios trazos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gestos de aplicación](application-gestures.md)
</dt> <dt>

[Gestos de gestos](flicks-gestures.md)
</dt> <dt>

[Gestos del sistema](system-gestures.md)
</dt> </dl>

 

 



