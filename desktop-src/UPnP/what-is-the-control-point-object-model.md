---
title: ¿Qué es el modelo de objetos de punto de control?
description: En la ilustración siguiente se muestra el modelo de objetos de punto de control básico.
ms.assetid: 6c5a32a1-932e-4868-b4c6-8701e90a7c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06fa7e9cd8fa2bd2e038002414260bf2468f8d951c24da42bdd7a687af06bc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007974"
---
# <a name="what-is-the-control-point-object-model"></a>¿Qué es el modelo de objetos de punto de control?

En la ilustración siguiente se muestra el modelo de objetos de punto de control básico.

![modelo de objetos de punto de control](images/upnp-object-model.png)

La búsqueda de dispositivos con la interfaz Device Finder crea una colección Dispositivos. Una colección Dispositivos contiene cero o más objetos Device. Las aplicaciones pueden usar los distintos métodos de recopilación devices para acceder a objetos device individuales.

Los objetos de dispositivo siempre contienen una colección de servicios que contiene uno o varios objetos Service. Estas aplicaciones usan estos objetos de servicio para comunicarse con los dispositivos y controlarlo.

 

 




