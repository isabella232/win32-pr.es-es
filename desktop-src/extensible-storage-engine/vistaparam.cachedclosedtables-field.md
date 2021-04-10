---
description: 'Más información sobre: VistaParam. CachedClosedTables, campo'
title: Campo VistaParam. CachedClosedTables (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: CachedClosedTables field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55104337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff72925e34c731e57d11170753ecff13f4b96a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153762"
---
# <a name="vistaparamcachedclosedtables-field"></a><span data-ttu-id="b1d4d-103">VistaParam. CachedClosedTables, campo</span><span class="sxs-lookup"><span data-stu-id="b1d4d-103">VistaParam.CachedClosedTables field</span></span>

<span data-ttu-id="b1d4d-104">Este parámetro controla el número de recursos de árbol B + almacenados en memoria caché por la instancia de después de que la aplicación haya cerrado las tablas que representan.</span><span class="sxs-lookup"><span data-stu-id="b1d4d-104">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="b1d4d-105">Los valores grandes de este parámetro harán que el motor de base de datos use más memoria, pero aumentará la velocidad con la que la aplicación puede abrir aleatoriamente un gran número de tablas.</span><span class="sxs-lookup"><span data-stu-id="b1d4d-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="b1d4d-106">Esto resulta útil para las aplicaciones que tienen un esquema con un gran número de tablas.</span><span class="sxs-lookup"><span data-stu-id="b1d4d-106">This is useful for applications that have a schema with a very large number of tables.</span></span>

<span data-ttu-id="b1d4d-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b1d4d-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="b1d4d-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b1d4d-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b1d4d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1d4d-109">Syntax</span></span>

``` vb
'Declaration
Public Const CachedClosedTables As JET_param
'Usage
Dim value As JET_param

value = VistaParam.CachedClosedTables
```

``` csharp
public const JET_param CachedClosedTables
```

## <a name="see-also"></a><span data-ttu-id="b1d4d-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b1d4d-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b1d4d-111">Referencia</span><span class="sxs-lookup"><span data-stu-id="b1d4d-111">Reference</span></span>

[<span data-ttu-id="b1d4d-112">Clase VistaParam</span><span class="sxs-lookup"><span data-stu-id="b1d4d-112">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="b1d4d-113">Miembros de VistaParam</span><span class="sxs-lookup"><span data-stu-id="b1d4d-113">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="b1d4d-114">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="b1d4d-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
