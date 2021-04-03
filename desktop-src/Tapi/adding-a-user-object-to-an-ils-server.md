---
description: El siguiente fragmento de código muestra la publicación de un objeto de usuario en un servidor ILS. Una vez publicado un objeto de usuario, los usuarios remotos pueden utilizar el objeto de usuario para realizar llamadas al usuario especificado.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Agregar un objeto de usuario a un servidor ILS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809236"
---
# <a name="adding-a-user-object-to-an-ils-server"></a>Agregar un objeto de usuario a un servidor ILS

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El siguiente fragmento de código muestra la publicación de un objeto de usuario en un servidor ILS. Una vez publicado un objeto de usuario, los usuarios remotos pueden utilizar el objeto de usuario para realizar llamadas al usuario especificado.

Este fragmento supone que ya se ha realizado la [conexión a un servidor ILS](connecting-to-an-ils-server.md) .


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



