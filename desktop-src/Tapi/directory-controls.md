---
description: En el diagrama siguiente se muestran los objetos principales implicados en los controles de directorio TAPI 3 Rendezvous. Las interfaces que se muestran se hipervinculan en las páginas de referencia pertinentes.
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: Controles de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87a7b9c0b11c76aac6067e1a3f67c3899552f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677384"
---
# <a name="directory-controls"></a>Controles de directorio

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

En el diagrama siguiente se muestran los objetos principales implicados en los controles de directorio TAPI 3 Rendezvous. Las interfaces que se muestran se hipervinculan en las páginas de referencia pertinentes.

![objetos e interfaces del control de directorio Rendezvous](images/renddir.png)

La interfaz principal de control de directorios es [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), que se debe crear mediante una llamada a **CoCreateInstance**. El objeto Rendezvous expone métodos para obtener listas de directorios disponibles y para crear nuevos directorios o objetos de directorio.

Un directorio reside en un servidor y es una lista de objetos de directorio junto con información descriptiva. Los métodos asociados a [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) pueden obtener información asociada al directorio como un todo, por ejemplo, si se trata de un directorio ILS.

Un objeto de directorio puede representar una conferencia o un usuario. La interfaz [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) proporciona métodos que pueden recuperar o modificar información genérica de un objeto de directorio, como la dirección de marcado.

La información de conferencia y usuario, como la dirección URL de una conferencia o el teléfono IP principal de un usuario, se manipula mediante métodos proporcionados en las interfaces [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) y [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) .

 

 



