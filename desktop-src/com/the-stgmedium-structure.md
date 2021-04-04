---
title: La estructura STGMEDIUM
description: La estructura STGMEDIUM
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104078586"
---
# <a name="the-stgmedium-structure"></a>La estructura STGMEDIUM

Del mismo modo que la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) es una mejora del identificador de formato del portapapeles de Windows, por lo que la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) es una mejora del identificador de memoria global que se usa para transferir los datos. La estructura **STGMEDIUM** incluye un miembro, **tymed**, que indica el medio que se va a usar y una Unión que incluye punteros y un identificador para obtener el medio especificado en **tymed**.

La estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) permite a los orígenes de datos y a los consumidores elegir el medio de Exchange más eficaz para cada representación. Si los datos son tan grandes que deben mantenerse en el disco, el origen de datos puede indicar un medio basado en disco en su formato preferido, usando solo la memoria global como copia de seguridad si ese es el único medio que entiende el consumidor. Poder usar el mejor medio para los intercambios como valor predeterminado mejora el rendimiento general del intercambio de datos entre aplicaciones. Por ejemplo, si algunos de los datos que se van a transferir ya están en el disco, la aplicación de origen puede moverla o copiarlos en un nuevo destino, ya sea en la misma aplicación o en otros, sin tener que cargar primero los datos en la memoria global. En el extremo receptor, el consumidor de los datos no tiene que volver a escribirlo en el disco.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos de datos y medios de transferencia](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




