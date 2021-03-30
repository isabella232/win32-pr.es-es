---
description: El objeto CallHub representa una vista de terceros de una llamada entre partes.
ms.assetid: ea23ae25-2fbb-4060-8273-cd7921d49e52
title: Objeto CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d43594db13c9175490b4cbb0941d1fb4e45b2ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002320"
---
# <a name="callhub-object"></a>Objeto CallHub

El objeto CallHub representa una vista de terceros de una llamada entre partes. Las interfaces y los métodos asociados obtienen y establecen información relacionada con el concentrador, como, por ejemplo, si está activo. Con el objeto CallHub, un usuario con la seguridad necesaria puede detectar y potencialmente controlar a otros participantes en una llamada.

Una aplicación no puede crear directamente un objeto CallHub. Un objeto CallHub se crea indirectamente cuando se recibe una llamada entrante a través de TAPI 3.

TAPI 3 se basa en los proveedores de servicios TAPI para proporcionar la información necesaria sobre las llamadas para implementar mediante el objeto CallHub. Dado que no todos los proveedores de servicios proporcionan esta información y no todo el hardware admite el seguimiento del centro de llamadas, la información disponible sobre los demás usuarios de la conexión puede ser limitada o inexistente.

En el ejemplo de creación de un código de [Conferencia simple](create-a-simple-conference.md) se muestra el uso de un objeto CallHub.

Vea [interfaces del objeto CallHub](callhub-object-interfaces.md) para obtener una lista de todas las interfaces asociadas al objeto CallHub.

 

 



