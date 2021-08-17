---
description: Puede usar un reconocedor de gestos personalizado de forma independiente, o además de GestureRecognizer.Cree el reconocedor de gestos personalizado como IStylusSyncPlugin, haga que cree CustomStylusData e incluya el complemento en el mismo StylusSyncPluginCollection que GestureRecognizer. En IStylusSyncPlugin, combine las notificaciones de gestos de ambos reconocedores en notificaciones que una aplicación va a consumir.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Uso de un reconocedor de gestos personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa4c58dd93bdb19f1f930be38e40f0068fa02239f09603035b572559d1f8a916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091334"
---
# <a name="using-a-custom-gesture-recognizer"></a>Uso de un reconocedor de gestos personalizado

Puede usar un reconocedor de gestos personalizado de forma independiente o además de [**GestureRecognizer**](gesturerecognizer-class.md).

Cree el reconocedor de gestos personalizado como [**IStylusSyncPlugin,**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)haga que cree [CustomStylusData](/previous-versions/ms575208(v=vs.100))e incluya el complemento en el mismo [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) que [**GestureRecognizer.**](gesturerecognizer-class.md) En **IStylusSyncPlugin,** combine las notificaciones de gestos de ambos reconocedores en notificaciones que una aplicación va a consumir.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso y manipulación de la entrada de lápiz óptico](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
