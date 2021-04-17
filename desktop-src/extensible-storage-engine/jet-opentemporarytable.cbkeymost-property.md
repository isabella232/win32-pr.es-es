---
description: 'Más información acerca de: propiedad JET_OPENTEMPORARYTABLE. cbKeyMost'
title: Propiedad JET_OPENTEMPORARYTABLE. cbKeyMost (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e608d1419cd381c507874bf1f1c334d192ae2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716973"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a><span data-ttu-id="0c3aa-103">Propiedad JET_OPENTEMPORARYTABLE. cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="0c3aa-103">JET_OPENTEMPORARYTABLE.cbKeyMost property</span></span>

<span data-ttu-id="0c3aa-104">Obtiene o establece el tamaño máximo para una clave que representa una fila determinada.</span><span class="sxs-lookup"><span data-stu-id="0c3aa-104">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="0c3aa-105">Se puede establecer el tamaño máximo de la clave para controlar cómo se truncan las claves.</span><span class="sxs-lookup"><span data-stu-id="0c3aa-105">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="0c3aa-106">El truncamiento de claves es importante porque puede afectar a la diferencia entre las filas.</span><span class="sxs-lookup"><span data-stu-id="0c3aa-106">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="0c3aa-107">Si este parámetro se establece en 0 o 255, el tamaño de clave máximo y su semántica permanecerán idénticos al tamaño máximo de clave admitido por Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0c3aa-107">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="0c3aa-108">Este parámetro también se puede establecer en un valor mayor como una función del tamaño de página de la base de datos para la instancia [DatabasePageSize](./jet-param-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="0c3aa-108">This parameter may also be set to a larger value as a function of the database page size for the instance [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="0c3aa-109">Vea [KeyMost](./vistaparam.keymost-field.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0c3aa-109">See [KeyMost](./vistaparam.keymost-field.md) for more information.</span></span>

<span data-ttu-id="0c3aa-110">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c3aa-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="0c3aa-111">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c3aa-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c3aa-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c3aa-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="0c3aa-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0c3aa-113">Property value</span></span>

<span data-ttu-id="0c3aa-114">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0c3aa-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0c3aa-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c3aa-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c3aa-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="0c3aa-116">Reference</span></span>

[<span data-ttu-id="0c3aa-117">JET_OPENTEMPORARYTABLE (clase)</span><span class="sxs-lookup"><span data-stu-id="0c3aa-117">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="0c3aa-118">Miembros de JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="0c3aa-118">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="0c3aa-119">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="0c3aa-119">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
