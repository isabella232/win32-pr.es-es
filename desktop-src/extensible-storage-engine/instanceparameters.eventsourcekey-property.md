---
description: 'Más información sobre: InstanceParameters. EventSourceKey (propiedad)'
title: Propiedad InstanceParameters. EventSourceKey
TOCTitle: 'EventSourceKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.eventsourcekey(v=EXCHG.10)
ms:contentKeyID: 55107449
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EventSourceKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d1dc80943095611737d0c9704bcc0e82ffee506f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001457"
---
# <a name="instanceparameterseventsourcekey-property"></a><span data-ttu-id="dbec9-103">Propiedad InstanceParameters. EventSourceKey</span><span class="sxs-lookup"><span data-stu-id="dbec9-103">InstanceParameters.EventSourceKey property</span></span>

<span data-ttu-id="dbec9-104">Obtiene o establece el nombre del registro de eventos que usa el motor de base de datos para sus mensajes de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="dbec9-104">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="dbec9-105">De forma predeterminada, todos los mensajes del registro de eventos Irán al registro de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dbec9-105">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="dbec9-106">Si se configura el nombre de la clave del registro para otro registro de eventos, los mensajes del registro de eventos Irán en su lugar.</span><span class="sxs-lookup"><span data-stu-id="dbec9-106">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<span data-ttu-id="dbec9-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dbec9-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dbec9-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dbec9-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dbec9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbec9-109">Syntax</span></span>

``` vb
'Declaration
Public Property EventSourceKey As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.EventSourceKey

instance.EventSourceKey = value
```

``` csharp
public string EventSourceKey { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="dbec9-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dbec9-110">Property value</span></span>

<span data-ttu-id="dbec9-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="dbec9-111">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="dbec9-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbec9-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dbec9-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="dbec9-113">Reference</span></span>

[<span data-ttu-id="dbec9-114">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="dbec9-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="dbec9-115">Miembros de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="dbec9-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="dbec9-116">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="dbec9-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
