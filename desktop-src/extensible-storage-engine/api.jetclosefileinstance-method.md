---
description: 'Más información sobre: API. JetCloseFileInstance (método)'
title: Método API. JetCloseFileInstance
TOCTitle: 'JetCloseFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosefileinstance(v=EXCHG.10)
ms:contentKeyID: 55100663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ac29dec4032d83197a57746789afc770d84ec30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714947"
---
# <a name="apijetclosefileinstance-method"></a><span data-ttu-id="4b610-103">Método API. JetCloseFileInstance</span><span class="sxs-lookup"><span data-stu-id="4b610-103">Api.JetCloseFileInstance method</span></span>

<span data-ttu-id="4b610-104">Cierra un archivo que se abrió con JetOpenFileInstance una vez extraídos los datos de ese archivo mediante JetReadFileInstance.</span><span class="sxs-lookup"><span data-stu-id="4b610-104">Closes a file that was opened with JetOpenFileInstance after the data from that file has been extracted using JetReadFileInstance.</span></span>

<span data-ttu-id="4b610-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4b610-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4b610-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4b610-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4b610-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b610-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseFileInstance ( _
    instance As JET_INSTANCE, _
    handle As JET_HANDLE _
)
'Usage
Dim instance As JET_INSTANCE
Dim handle As JET_HANDLEApi.JetCloseFileInstance(instance, _
    handle)
```

``` csharp
public static void JetCloseFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE handle
)
```

#### <a name="parameters"></a><span data-ttu-id="4b610-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b610-108">Parameters</span></span>

  - <span data-ttu-id="4b610-109">instance</span><span class="sxs-lookup"><span data-stu-id="4b610-109">instance</span></span>  
    <span data-ttu-id="4b610-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4b610-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="4b610-111">La instancia de que se utilizará.</span><span class="sxs-lookup"><span data-stu-id="4b610-111">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4b610-112">handle</span><span class="sxs-lookup"><span data-stu-id="4b610-112">handle</span></span>  
    <span data-ttu-id="4b610-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4b610-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="4b610-114">Identificador que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="4b610-114">The handle to close.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b610-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b610-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4b610-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="4b610-116">Reference</span></span>

[<span data-ttu-id="4b610-117">Clase de API</span><span class="sxs-lookup"><span data-stu-id="4b610-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4b610-118">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="4b610-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4b610-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4b610-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
