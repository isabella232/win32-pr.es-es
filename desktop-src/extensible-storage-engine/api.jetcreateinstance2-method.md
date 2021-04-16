---
description: 'Más información sobre: API. JetCreateInstance2 (método)'
title: Método API. JetCreateInstance2
TOCTitle: 'JetCreateInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String,System.String,Microsoft.Isam.Esent.Interop.CreateInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance2(v=EXCHG.10)
ms:contentKeyID: 55100675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d21974d5c3bd5ca6dfbab2ac493d19b202ca6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705519"
---
# <a name="apijetcreateinstance2-method"></a><span data-ttu-id="7446c-103">Método API. JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="7446c-103">Api.JetCreateInstance2 method</span></span>

<span data-ttu-id="7446c-104">Asignar una nueva instancia del motor de base de datos para su uso en un único proceso, con un nombre para mostrar especificado.</span><span class="sxs-lookup"><span data-stu-id="7446c-104">Allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="7446c-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7446c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7446c-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7446c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7446c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7446c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance2 ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String, _
    displayName As String, _
    grbit As CreateInstanceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As String
Dim displayName As String
Dim grbit As CreateInstanceGrbitApi.JetCreateInstance2(instance, _
    name, displayName, grbit)
```

``` csharp
public static void JetCreateInstance2(
    out JET_INSTANCE instance,
    string name,
    string displayName,
    CreateInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7446c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7446c-108">Parameters</span></span>

  - <span data-ttu-id="7446c-109">instance</span><span class="sxs-lookup"><span data-stu-id="7446c-109">instance</span></span>  
    <span data-ttu-id="7446c-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7446c-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7446c-111">Devuelve la instancia que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="7446c-111">Returns the newly create instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="7446c-112">name</span><span class="sxs-lookup"><span data-stu-id="7446c-112">name</span></span>  
    <span data-ttu-id="7446c-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7446c-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7446c-114">Especifica un identificador de cadena único para la instancia que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="7446c-114">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="7446c-115">Esta cadena debe ser única dentro de un proceso determinado que hospede el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="7446c-115">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="7446c-116">DisplayName</span><span class="sxs-lookup"><span data-stu-id="7446c-116">displayName</span></span>  
    <span data-ttu-id="7446c-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7446c-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7446c-118">Nombre para mostrar de la instancia de que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="7446c-118">A display name for the instance to be created.</span></span> <span data-ttu-id="7446c-119">Se utilizará en las entradas del registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="7446c-119">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="7446c-120">grbit</span><span class="sxs-lookup"><span data-stu-id="7446c-120">grbit</span></span>  
    <span data-ttu-id="7446c-121">Tipo: [Microsoft. ISAM. esent. Interop. CreateInstanceGrbit](./createinstancegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7446c-121">Type: [Microsoft.Isam.Esent.Interop.CreateInstanceGrbit](./createinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7446c-122">Opciones de creación.</span><span class="sxs-lookup"><span data-stu-id="7446c-122">Creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="7446c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7446c-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7446c-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="7446c-124">Reference</span></span>

[<span data-ttu-id="7446c-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="7446c-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7446c-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="7446c-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7446c-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7446c-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
