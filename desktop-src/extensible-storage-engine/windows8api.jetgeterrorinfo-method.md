---
description: 'Más información sobre: Windows8Api. JetGetErrorInfo (método)'
title: Método Windows8Api. JetGetErrorInfo (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetGetErrorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo(Microsoft.Isam.Esent.Interop.JET_err,Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetgeterrorinfo(v=EXCHG.10)
ms:contentKeyID: 55104459
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c94e6594c2d52769f5034bdf1c7253bee838edaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705863"
---
# <a name="windows8apijetgeterrorinfo-method"></a><span data-ttu-id="3ee8d-103">Windows8Api. JetGetErrorInfo, método</span><span class="sxs-lookup"><span data-stu-id="3ee8d-103">Windows8Api.JetGetErrorInfo method</span></span>

<span data-ttu-id="3ee8d-104">Obtiene información extendida sobre un error.</span><span class="sxs-lookup"><span data-stu-id="3ee8d-104">Gets extended information about an error.</span></span>

<span data-ttu-id="3ee8d-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3ee8d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="3ee8d-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3ee8d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3ee8d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ee8d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetErrorInfo ( _
    error As JET_err, _
    <OutAttribute> ByRef errinfo As JET_ERRINFOBASIC _
)
'Usage
Dim error As JET_err
Dim errinfo As JET_ERRINFOBASICWindows8Api.JetGetErrorInfo(error, errinfo)
```

``` csharp
public static void JetGetErrorInfo(
    JET_err error,
    out JET_ERRINFOBASIC errinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="3ee8d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ee8d-108">Parameters</span></span>

  - <span data-ttu-id="3ee8d-109">error</span><span class="sxs-lookup"><span data-stu-id="3ee8d-109">error</span></span>  
    <span data-ttu-id="3ee8d-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3ee8d-110">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="3ee8d-111">Código de error sobre el que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="3ee8d-111">The error code about which to retrieve information.</span></span>

<!-- end list -->

  - <span data-ttu-id="3ee8d-112">errinfo</span><span class="sxs-lookup"><span data-stu-id="3ee8d-112">errinfo</span></span>  
    <span data-ttu-id="3ee8d-113">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)</span><span class="sxs-lookup"><span data-stu-id="3ee8d-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)</span></span>  
    
    <span data-ttu-id="3ee8d-114">Información sobre el código de error especificado.</span><span class="sxs-lookup"><span data-stu-id="3ee8d-114">Information about the specified error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ee8d-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ee8d-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3ee8d-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="3ee8d-116">Reference</span></span>

[<span data-ttu-id="3ee8d-117">Clase Windows8Api</span><span class="sxs-lookup"><span data-stu-id="3ee8d-117">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="3ee8d-118">Miembros de Windows8Api</span><span class="sxs-lookup"><span data-stu-id="3ee8d-118">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="3ee8d-119">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="3ee8d-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
