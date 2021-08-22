---
title: Soporte técnico para consultas
description: Al implementar la interfaz IDirectorySearch, los proveedores ADSI obtienen acceso a un subconjunto de OLE DB características de solo lectura.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Compatibilidad con ADSI de consultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ad1892cf7c0e619ef55b9c3e5af6885d4cbdc7ac68fbcbd206524128b283d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023233"
---
# <a name="support-for-queries"></a>Soporte técnico para consultas

Al implementar la interfaz [**IDirectorySearch,**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) los proveedores ADSI obtienen acceso a un subconjunto de OLE DB características de solo lectura.

La implementación ADSI de los métodos de [**IDirectorySearch usa**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) las interfaces OLE DB descritas en ADSI versión 1.0, incluida la siguiente lista de objetos COM:

-   Objeto de origen de datos (el servicio de directorio), que admite **IDBInitialize**, **IDBCreateSession,** **IDBProperties** e **IPersist**.
-   Objeto DBSessions, que admite **IOpenRowSet,** **ISessionProperties** e **ICreateCommand**.
-   Objeto Command, que admite **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties,** **ICommandText** e **IConvertType**.
-   Objeto de conjunto de filas que admite **IAccessor,** **IColumnsInfo,** **IConvertType,** **IRowset** e **IRowsetInfo**.

Para obtener más información OLE DB, consulte la referencia del programador de OLE DB en el Kit de desarrollo de software (SDK) de plataforma.

 

 




