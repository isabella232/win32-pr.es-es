---
title: Soporte técnico para consultas
description: Mediante la implementación de la interfaz IDirectorySearch, los proveedores ADSI obtienen acceso a un subconjunto de OLE DB características de solo lectura.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Compatibilidad con consultas ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1304dcabd9c008b0f645982e695554225f59bac9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656145"
---
# <a name="support-for-queries"></a>Soporte técnico para consultas

Mediante la implementación de la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , los proveedores ADSI obtienen acceso a un subconjunto de OLE DB características de solo lectura.

La implementación de ADSI de los métodos de [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) utiliza las interfaces OLE DB descritas en la versión 1,0 de ADSI, incluida la lista siguiente de objetos com:

-   Objeto de origen de datos (el servicio de directorio), compatible con **IDBInitialize**, **IDBCreateSession**, **IDBProperties** y **IPersist**.
-   Objeto DBSessions, compatible con **IOpenRowSet**, **ISessionProperties** y **ICreateCommand**.
-   Objeto de comando, compatible con **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** y **IConvertType**.
-   Objeto de conjunto de filas, que admite **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** e **IRowsetInfo**.

Para obtener más información acerca de OLE DB, vea la referencia del programador de OLE DB en el kit de desarrollo de software (SDK) de la plataforma.

 

 




