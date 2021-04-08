---
description: Las clases RealTimeStylus, GestureRecognizer y DynamicRenderer se implementan como contenedores COM y solo están disponibles en código administrado.
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: Notas de implementación para las API de StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47150d6a9aff5495e89f30d29929fd7d604f9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000979"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a>Notas de implementación para las API de StylusInput

Las clases [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))y [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) se implementan como contenedores com y solo están disponibles en código administrado.

Cuando el objeto [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100))o [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) se agrega como un complemento a un objeto **RealTimeStylus** , los objetos com subyacentes interactúan en el nivel com. Por lo tanto, no se admite la llamada directa a los métodos de las interfaces [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) o [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) . Agregar el objeto **RealTimeStylus**, GestureRecognizer o DynamicRenderer al objeto **RealTimeStylus** es la única manera de tener acceso a estas características.

 

 
