---
title: Interfaces de consulta
description: Se pueden usar tres tipos de interfaces ADSI para realizar búsquedas en el directorio. El entorno de la aplicación y otros requisitos pueden indicar qué interfaz se utiliza.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Interfaces de consulta ADSI
- Consultas ADSI, interfaces de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903032"
---
# <a name="query-interfaces"></a>Interfaces de consulta

Se pueden usar tres tipos de interfaces ADSI para realizar búsquedas en el directorio. El entorno de la aplicación y otros requisitos pueden indicar qué interfaz se utiliza.

-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). **IDirectorySearch** es una interfaz com básica que solo está disponible para los programadores de C/C++. Para obtener más información, consulte [búsqueda con la interfaz IDirectorySearch](searching-with-idirectorysearch.md).
-   ADO. Las interfaces de objetos de datos ActiveX (ADO) son interfaces de automatización que utilizan OLE DB. Utilice ADO para las consultas dentro de las aplicaciones que se basan en la automatización. Entre ellas se incluyen Visual Basic aplicaciones, Active Server páginas, etc. Para obtener más información, vea [Buscar con objetos de datos ActiveX](searching-with-activex-data-objects-ado.md).
-   OLE DB. OLE DB es un conjunto de interfaces de C/C++ que se usan para consultar bases de datos. Al admitir estas interfaces, los proveedores ADSI pueden implementar características avanzadas de OLE DB, como consultas distribuidas con otros proveedores de OLE DB. Para obtener más información, vea [Buscar con OLE DB](searching-with-ole-db.md).

 

 




