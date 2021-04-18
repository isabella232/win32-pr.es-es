---
description: 'Más información sobre: InstanceParameters. AlternateDatabaseRecoveryDirectory (propiedad)'
title: Propiedad InstanceParameters. AlternateDatabaseRecoveryDirectory
TOCTitle: 'AlternateDatabaseRecoveryDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.alternatedatabaserecoverydirectory(v=EXCHG.10)
ms:contentKeyID: 55107440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_AlternateDatabaseRecoveryDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70e08c65027806990ab511ef8561b41551f0ac2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705819"
---
# <a name="instanceparametersalternatedatabaserecoverydirectory-property"></a><span data-ttu-id="97f0c-103">Propiedad InstanceParameters. AlternateDatabaseRecoveryDirectory</span><span class="sxs-lookup"><span data-stu-id="97f0c-103">InstanceParameters.AlternateDatabaseRecoveryDirectory property</span></span>

<span data-ttu-id="97f0c-104">Obtiene o establece la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta en la que la recuperación tras bloqueo o una operación de restauración pueden encontrar las bases de datos a las que se hace referencia en el registro de transacciones de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="97f0c-104">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span>

<span data-ttu-id="97f0c-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="97f0c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="97f0c-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="97f0c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="97f0c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97f0c-107">Syntax</span></span>

``` vb
'Declaration
Public Property AlternateDatabaseRecoveryDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.AlternateDatabaseRecoveryDirectory

instance.AlternateDatabaseRecoveryDirectory = value
```

``` csharp
public string AlternateDatabaseRecoveryDirectory { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="97f0c-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="97f0c-108">Property value</span></span>

<span data-ttu-id="97f0c-109">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="97f0c-109">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="remarks"></a><span data-ttu-id="97f0c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97f0c-110">Remarks</span></span>

<span data-ttu-id="97f0c-111">Este parámetro se omite en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="97f0c-111">This parameter is ignored on Windows XP.</span></span>

## <a name="see-also"></a><span data-ttu-id="97f0c-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="97f0c-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97f0c-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="97f0c-113">Reference</span></span>

[<span data-ttu-id="97f0c-114">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="97f0c-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="97f0c-115">Miembros de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="97f0c-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="97f0c-116">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="97f0c-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
