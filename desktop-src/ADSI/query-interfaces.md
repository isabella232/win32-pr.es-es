---
title: Interfaces de consulta
description: Se pueden usar tres tipos de interfaces ADSI para realizar búsquedas de directorios. El entorno de la aplicación y otros requisitos pueden indicar qué interfaz se usa.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- ADSI de interfaces de consulta
- Consultas ADSI, interfaces de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967f111107549fd0e6352f0e93d3a747b287c040ea7d5e6cee48415aa7f7925f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637725"
---
# <a name="query-interfaces"></a>Interfaces de consulta

Se pueden usar tres tipos de interfaces ADSI para realizar búsquedas de directorios. El entorno de la aplicación y otros requisitos pueden indicar qué interfaz se usa.

-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). **IDirectorySearch es** una interfaz COM básica que solo está disponible para los programadores de C/C++. Para obtener más información, [vea Buscar con la interfaz IDirectorySearch](searching-with-idirectorysearch.md).
-   Ado. Las ActiveX data object (ADO) son interfaces de Automation que usan OLE DB. Use ADO para las consultas dentro de aplicaciones que dependen de Automation. Estas incluyen Visual Basic aplicaciones, Active Server Pages, y así sucesivamente. Para obtener más información, vea [Buscar con ActiveX objetos de datos](searching-with-activex-data-objects-ado.md).
-   OLE DB. OLE DB es un conjunto de interfaces de C/C++ que se usan para consultar bases de datos. Al admitir estas interfaces, los proveedores adsi pueden implementar características avanzadas de OLE DB, como consultas distribuidas con otros proveedores de OLE DB cliente. Para obtener más información, vea [Buscar con OLE DB](searching-with-ole-db.md).

 

 




