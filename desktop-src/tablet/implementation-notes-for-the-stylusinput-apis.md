---
description: Las clases RealTimeStylus, GestureRecognizer y DynamicRenderer se implementan como contenedores COM y solo están disponibles en código administrado.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Notas de implementación de las API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c106dd0e940cf6fd9e54235af43901d14e511ead5e8908be56b464c483335b74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032383"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a>Notas de implementación de las API StylusInput

Las [**clases RealTimeStylus,**](realtimestylus-class.md) [GestureRecognizer](/previous-versions/ms575185(v=vs.100))y [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) se implementan como contenedores COM y solo están disponibles en código administrado.

Cuando se agrega el objeto [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))o [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) como complemento a un objeto **RealTimeStylus,** los objetos COM subyacentes interactúan en el nivel COM. Por lo tanto, no se admite la llamada directa a los métodos de las interfaces [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) o [IStylusAsyncPlugin.](/previous-versions/ms575194(v=vs.100)) Agregar el **objeto RealTimeStylus,** GestureRecognizer o DynamicRenderer al objeto **RealTimeStylus** es la única manera de acceder a estas características.

 

 
