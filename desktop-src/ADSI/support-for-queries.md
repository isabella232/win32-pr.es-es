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
# <a name="support-for-queries"></a><span data-ttu-id="7870e-104">Soporte técnico para consultas</span><span class="sxs-lookup"><span data-stu-id="7870e-104">Support for Queries</span></span>

<span data-ttu-id="7870e-105">Mediante la implementación de la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , los proveedores ADSI obtienen acceso a un subconjunto de OLE DB características de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7870e-105">By implementing the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, ADSI providers gain access to a subset of OLE DB read-only features.</span></span>

<span data-ttu-id="7870e-106">La implementación de ADSI de los métodos de [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) utiliza las interfaces OLE DB descritas en la versión 1,0 de ADSI, incluida la lista siguiente de objetos com:</span><span class="sxs-lookup"><span data-stu-id="7870e-106">The ADSI implementation of the methods of [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) itself uses the OLE DB interfaces described in ADSI Version 1.0, including the following list of COM objects:</span></span>

-   <span data-ttu-id="7870e-107">Objeto de origen de datos (el servicio de directorio), compatible con **IDBInitialize**, **IDBCreateSession**, **IDBProperties** y **IPersist**.</span><span class="sxs-lookup"><span data-stu-id="7870e-107">Data Source Object (the directory service), supporting **IDBInitialize**, **IDBCreateSession**, **IDBProperties**, and **IPersist**.</span></span>
-   <span data-ttu-id="7870e-108">Objeto DBSessions, compatible con **IOpenRowSet**, **ISessionProperties** y **ICreateCommand**.</span><span class="sxs-lookup"><span data-stu-id="7870e-108">DBSessions Object, supporting **IOpenRowSet**, **ISessionProperties**, and **ICreateCommand**.</span></span>
-   <span data-ttu-id="7870e-109">Objeto de comando, compatible con **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** y **IConvertType**.</span><span class="sxs-lookup"><span data-stu-id="7870e-109">Command Object, supporting **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText**, and **IConvertType**.</span></span>
-   <span data-ttu-id="7870e-110">Objeto de conjunto de filas, que admite **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** e **IRowsetInfo**.</span><span class="sxs-lookup"><span data-stu-id="7870e-110">Rowset Object, supporting **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset**, and **IRowsetInfo**.</span></span>

<span data-ttu-id="7870e-111">Para obtener más información acerca de OLE DB, vea la referencia del programador de OLE DB en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="7870e-111">For more information about OLE DB, see the OLE DB Programmer's Reference in the Platform Software Development Kit (SDK).</span></span>

 

 




