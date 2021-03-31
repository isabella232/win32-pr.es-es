---
description: 'Más información sobre: InstanceParameters. CleanupMismatchedLogFiles (propiedad)'
title: Propiedad InstanceParameters. CleanupMismatchedLogFiles
TOCTitle: 'CleanupMismatchedLogFiles property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cleanupmismatchedlogfiles(v=EXCHG.10)
ms:contentKeyID: 55103296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e80bb8877335e26cb233a09b2fa3ec3a6f12615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155404"
---
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a><span data-ttu-id="17e6d-103">Propiedad InstanceParameters. CleanupMismatchedLogFiles</span><span class="sxs-lookup"><span data-stu-id="17e6d-103">InstanceParameters.CleanupMismatchedLogFiles property</span></span>

<span data-ttu-id="17e6d-104">Obtiene o establece un valor que indica si se produce un error en JetInit cuando el motor de base de datos está configurado para empezar a usar archivos de registro de transacciones en un disco con un tamaño diferente del configurado.</span><span class="sxs-lookup"><span data-stu-id="17e6d-104">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="17e6d-105">Normalmente, [JetInit (JET_INSTANCE)](./api.jetinit-method.md) recuperará correctamente las bases de datos, pero producirá un error con [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) para indicar que el tamaño del archivo de registro está mal configurado.</span><span class="sxs-lookup"><span data-stu-id="17e6d-105">Normally, [JetInit(JET_INSTANCE)](./api.jetinit-method.md) will successfully recover the databases but will fail with [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="17e6d-106">Sin embargo, cuando este parámetro se establece en true, el motor de base de datos eliminará silenciosamente todos los archivos de registro antiguos, iniciará un nuevo conjunto de archivos de registro de transacciones con el tamaño del archivo de registro configurado.</span><span class="sxs-lookup"><span data-stu-id="17e6d-106">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="17e6d-107">Este parámetro es útil cuando la aplicación desea cambiar de forma transparente el tamaño del archivo de registro de transacciones todavía funciona de forma transparente en los escenarios de actualización y restauración.</span><span class="sxs-lookup"><span data-stu-id="17e6d-107">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<span data-ttu-id="17e6d-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="17e6d-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="17e6d-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="17e6d-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="17e6d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17e6d-110">Syntax</span></span>

``` vb
'Declaration
Public Property CleanupMismatchedLogFiles As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CleanupMismatchedLogFiles

instance.CleanupMismatchedLogFiles = value
```

``` csharp
public bool CleanupMismatchedLogFiles { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="17e6d-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="17e6d-111">Property value</span></span>

<span data-ttu-id="17e6d-112">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="17e6d-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="17e6d-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="17e6d-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="17e6d-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="17e6d-114">Reference</span></span>

[<span data-ttu-id="17e6d-115">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="17e6d-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="17e6d-116">Miembros de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="17e6d-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="17e6d-117">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="17e6d-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
