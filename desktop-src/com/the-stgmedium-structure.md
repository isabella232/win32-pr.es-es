---
title: La estructura STGMEDIUM
description: La estructura STGMEDIUM
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da0adc98b5d774754bd2cbbccb415092d6498684a60189d6346afac82bd270a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992275"
---
# <a name="the-stgmedium-structure"></a>La estructura STGMEDIUM

Al igual que la estructura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) es una mejora del identificador de formato del Portapapeles de Windows, la estructura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) es una mejora del identificador de memoria global utilizado para transferir los datos. La estructura **STGMEDIUM** incluye un miembro, **tymed**, que indica el medio que se va a usar, y una unión que comprende punteros y un identificador para obtener el medio especificado en **tymed**.

La [**estructura STGMEDIUM permite**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) a los orígenes de datos y a los consumidores elegir el medio de intercambio más eficaz por representación. Si los datos son tan grandes que se deben mantener en el disco, el origen de datos puede indicar un medio basado en disco en su formato preferido, usando solo la memoria global como copia de seguridad si es el único medio que el consumidor entiende. Poder usar el mejor medio para los intercambios, ya que el valor predeterminado mejora el rendimiento general del intercambio de datos entre aplicaciones. Por ejemplo, si algunos de los datos que se transfieren ya están en el disco, la aplicación de origen puede moverlos o copiarlos en un nuevo destino, ya sea en la misma aplicación o en alguna otra, sin tener que cargar primero los datos en la memoria global. En el extremo receptor, el consumidor de los datos no tiene que volver a escribirlo en el disco.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formatos de datos y medios de transferencia](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




