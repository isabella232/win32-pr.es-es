---
description: En el diagrama siguiente se muestran los objetos principales implicados en los controles de directorio TAPI 3 Rendezvous. Las interfaces mostradas se hipervínculon a las páginas de referencia pertinentes.
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: Controles de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe884b524547bebf167c534b18ea46e74e1efe23078afab65c67a0a652c6f62d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945827"
---
# <a name="directory-controls"></a>Controles de directorio

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

En el diagrama siguiente se muestran los objetos principales implicados en los controles de directorio TAPI 3 Rendezvous. Las interfaces mostradas se hipervínculon a las páginas de referencia pertinentes.

![interfaces y objetos de control de directorios de encuentro](images/renddir.png)

La interfaz de control de directorio principal [**es ITRendezvous,**](/windows/desktop/api/Rend/nn-rend-itrendezvous)que se debe crear mediante una llamada **a CoCreateInstance**. El objeto Rendezvous expone métodos para obtener listas de directorios disponibles y para crear nuevos directorios u objetos de directorio.

Un directorio reside en un servidor y es una lista de objetos de directorio junto con información descriptiva. Los métodos asociados a [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) pueden obtener información asociada al directorio en su conjunto, por ejemplo, si se trata de un directorio ILS.

Un objeto de directorio puede representar una conferencia o un usuario. La [**interfaz ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) proporciona métodos que pueden recuperar o modificar información genérica para un objeto de directorio, como la dirección que se puede marcar.

La información de la conferencia y del usuario, como la dirección URL de una conferencia o el teléfono IP principal de un usuario, se manipula mediante los métodos proporcionados en las interfaces [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) e [**ITDirectoryObjectUser.**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)

 

 



