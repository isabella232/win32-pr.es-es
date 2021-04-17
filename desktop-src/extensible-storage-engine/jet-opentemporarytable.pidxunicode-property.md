---
description: 'Más información acerca de: propiedad JET_OPENTEMPORARYTABLE. pidxunicode'
title: Propiedad JET_OPENTEMPORARYTABLE. pidxunicode (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'pidxunicode property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.pidxunicode(v=EXCHG.10)
ms:contentKeyID: 55104227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98e5beb4f4523f5e6a6da37a999b6c0a2ab7b4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707197"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a><span data-ttu-id="35766-103">Propiedad JET_OPENTEMPORARYTABLE. pidxunicode</span><span class="sxs-lookup"><span data-stu-id="35766-103">JET_OPENTEMPORARYTABLE.pidxunicode property</span></span>

<span data-ttu-id="35766-104">Obtiene o establece el identificador de configuración regional y las marcas de normalización que se van a utilizar para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="35766-104">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="35766-105">Cuando este parámetro es null, se utilizará el LCID predeterminado para comparar las columnas de clave Unicode de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="35766-105">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="35766-106">El LCID predeterminado es la configuración regional en Inglés de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="35766-106">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="35766-107">Cuando este parámetro es null, se usarán las marcas de normalización predeterminadas para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="35766-107">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="35766-108">Las marcas de normalización predeterminadas son: NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="35766-108">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="35766-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="35766-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="35766-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="35766-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="35766-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35766-111">Syntax</span></span>

``` vb
'Declaration
Public Property pidxunicode As JET_UNICODEINDEX
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_UNICODEINDEX

value = instance.pidxunicode

instance.pidxunicode = value
```

``` csharp
public JET_UNICODEINDEX pidxunicode { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="35766-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="35766-112">Property value</span></span>

<span data-ttu-id="35766-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="35766-113">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="35766-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="35766-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="35766-115">Referencia</span><span class="sxs-lookup"><span data-stu-id="35766-115">Reference</span></span>

[<span data-ttu-id="35766-116">JET_OPENTEMPORARYTABLE (clase)</span><span class="sxs-lookup"><span data-stu-id="35766-116">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="35766-117">Miembros de JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="35766-117">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="35766-118">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="35766-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
