---
description: 'Más información sobre: API. JetRegisterCallback (método)'
title: Método API. JetRegisterCallback
TOCTitle: 'JetRegisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.IntPtr,Microsoft.Isam.Esent.Interop.JET_HANDLE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100784
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97ba91d776575285d71e0ad4ec8d94eeb10a743a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707251"
---
# <a name="apijetregistercallback-method"></a><span data-ttu-id="bcabf-103">Método API. JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="bcabf-103">Api.JetRegisterCallback method</span></span>

<span data-ttu-id="bcabf-104">Permite a la aplicación configurar el motor de base de datos para emitir notificaciones a la aplicación para eventos concretos.</span><span class="sxs-lookup"><span data-stu-id="bcabf-104">Allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="bcabf-105">Estas notificaciones están asociadas a una tabla específica y permanecen en vigor solo hasta que se cierra la instancia que contiene la tabla mediante [JetTerm (JET_INSTANCE)](./api.jetterm-method.md).</span><span class="sxs-lookup"><span data-stu-id="bcabf-105">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm(JET_INSTANCE)](./api.jetterm-method.md).</span></span>

<span data-ttu-id="bcabf-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bcabf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bcabf-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bcabf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bcabf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcabf-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRegisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callback As JET_CALLBACK, _
    context As IntPtr, _
    <OutAttribute> ByRef callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callback As JET_CALLBACK
Dim context As IntPtr
Dim callbackId As JET_HANDLEApi.JetRegisterCallback(sesid, _
    tableid, cbtyp, callback, context, _
    callbackId)
```

``` csharp
public static void JetRegisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_CALLBACK callback,
    IntPtr context,
    out JET_HANDLE callbackId
)
```

#### <a name="parameters"></a><span data-ttu-id="bcabf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcabf-109">Parameters</span></span>

  - <span data-ttu-id="bcabf-110">sesid</span><span class="sxs-lookup"><span data-stu-id="bcabf-110">sesid</span></span>  
    <span data-ttu-id="bcabf-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bcabf-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bcabf-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="bcabf-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="bcabf-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="bcabf-113">tableid</span></span>  
    <span data-ttu-id="bcabf-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bcabf-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bcabf-115">Cursor abierto en la tabla en la que se debe registrar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="bcabf-115">A cursor opened on the table that the callback should be registered on.</span></span>

<!-- end list -->

  - <span data-ttu-id="bcabf-116">cbtyp</span><span class="sxs-lookup"><span data-stu-id="bcabf-116">cbtyp</span></span>  
    <span data-ttu-id="bcabf-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bcabf-117">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="bcabf-118">Los motivos de devolución de llamada para los que la aplicación desea recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="bcabf-118">The callback reasons for which the application wishes to receive notifications.</span></span>

<!-- end list -->

  - <span data-ttu-id="bcabf-119">devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="bcabf-119">callback</span></span>  
    <span data-ttu-id="bcabf-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="bcabf-120">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="bcabf-121">La función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="bcabf-121">The callback function.</span></span>

<!-- end list -->

  - <span data-ttu-id="bcabf-122">context</span><span class="sxs-lookup"><span data-stu-id="bcabf-122">context</span></span>  
    <span data-ttu-id="bcabf-123">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="bcabf-123">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="bcabf-124">Contexto que se proporcionará a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="bcabf-124">A context that will be given to the callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="bcabf-125">callbackId</span><span class="sxs-lookup"><span data-stu-id="bcabf-125">callbackId</span></span>  
    <span data-ttu-id="bcabf-126">Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bcabf-126">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="bcabf-127">Identificador que se puede usar más adelante para cancelar el registro de la función de devolución de llamada determinada mediante [JetUnregisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md).</span><span class="sxs-lookup"><span data-stu-id="bcabf-127">A handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="bcabf-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcabf-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bcabf-129">Referencia</span><span class="sxs-lookup"><span data-stu-id="bcabf-129">Reference</span></span>

[<span data-ttu-id="bcabf-130">Clase de API</span><span class="sxs-lookup"><span data-stu-id="bcabf-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bcabf-131">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="bcabf-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bcabf-132">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="bcabf-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
