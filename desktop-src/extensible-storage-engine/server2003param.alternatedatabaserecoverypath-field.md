---
description: 'Más información sobre: Server2003Param. AlternateDatabaseRecoveryPath, campo'
title: Campo Server2003Param. AlternateDatabaseRecoveryPath (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: AlternateDatabaseRecoveryPath field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003param.alternatedatabaserecoverypath(v=EXCHG.10)
ms:contentKeyID: 55104217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 770ac27596b4385d0012cb65847754b4deb7e9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648231"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a><span data-ttu-id="5b3f6-103">Server2003Param. AlternateDatabaseRecoveryPath, campo</span><span class="sxs-lookup"><span data-stu-id="5b3f6-103">Server2003Param.AlternateDatabaseRecoveryPath field</span></span>

<span data-ttu-id="5b3f6-104">La ruta de acceso completa a cada base de datos se conserva en los registros de transacciones en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5b3f6-104">The full path to each database is persisted in the transaction logs at run time.</span></span> <span data-ttu-id="5b3f6-105">Normalmente, estas bases de datos deben permanecer en la ubicación original para que la reproducción de transacciones funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="5b3f6-105">Ordinarily, these databases must remain at the original location for transaction replay to function correctly.</span></span> <span data-ttu-id="5b3f6-106">Este parámetro se puede usar para forzar la recuperación tras bloqueo o una operación de restauración para buscar las bases de datos a las que se hace referencia en el registro de transacciones en la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="5b3f6-106">This parameter can be used to force crash recovery or a restore operation to look for the databases referenced in the transaction log in the specified folder.</span></span>

<span data-ttu-id="5b3f6-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5b3f6-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="5b3f6-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5b3f6-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3f6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b3f6-109">Syntax</span></span>

``` vb
'Declaration
Public Const AlternateDatabaseRecoveryPath As JET_param
'Usage
Dim value As JET_param

value = Server2003Param.AlternateDatabaseRecoveryPath
```

``` csharp
public const JET_param AlternateDatabaseRecoveryPath
```

## <a name="see-also"></a><span data-ttu-id="5b3f6-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5b3f6-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5b3f6-111">Referencia</span><span class="sxs-lookup"><span data-stu-id="5b3f6-111">Reference</span></span>

[<span data-ttu-id="5b3f6-112">Clase Server2003Param</span><span class="sxs-lookup"><span data-stu-id="5b3f6-112">Server2003Param class</span></span>](./server2003param-class.md)

[<span data-ttu-id="5b3f6-113">Miembros de Server2003Param</span><span class="sxs-lookup"><span data-stu-id="5b3f6-113">Server2003Param members</span></span>](./server2003param-members.md)

[<span data-ttu-id="5b3f6-114">Espacio de nombres Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="5b3f6-114">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
