---
description: 'Más información sobre: método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, cadena)'
title: Método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, cadena)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100819
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d8d9d65af803a011c0a6a79fdaec2fb0a44755b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279616"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-jet_callback-string"></a><span data-ttu-id="9f19e-103">Método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, cadena)</span><span class="sxs-lookup"><span data-stu-id="9f19e-103">Api.JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)</span></span>

<span data-ttu-id="9f19e-104">Establece las opciones de configuración de base de datos.</span><span class="sxs-lookup"><span data-stu-id="9f19e-104">Sets database configuration options.</span></span>

<span data-ttu-id="9f19e-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f19e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9f19e-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9f19e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9f19e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f19e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As JET_CALLBACK, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As JET_CALLBACK
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    JET_CALLBACK paramValue,
    string paramString
)
```

#### <a name="parameters"></a><span data-ttu-id="9f19e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f19e-108">Parameters</span></span>

  - <span data-ttu-id="9f19e-109">instance</span><span class="sxs-lookup"><span data-stu-id="9f19e-109">instance</span></span>  
    <span data-ttu-id="9f19e-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9f19e-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="9f19e-111">Instancia en la que se va a establecer la opción o [Nil](./jet-instance.nil-property.md) para establecer la opción en todas las instancias.</span><span class="sxs-lookup"><span data-stu-id="9f19e-111">The instance to set the option on or [Nil](./jet-instance.nil-property.md) to set the option on all instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="9f19e-112">sesid</span><span class="sxs-lookup"><span data-stu-id="9f19e-112">sesid</span></span>  
    <span data-ttu-id="9f19e-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9f19e-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9f19e-114">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="9f19e-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9f19e-115">paramid</span><span class="sxs-lookup"><span data-stu-id="9f19e-115">paramid</span></span>  
    <span data-ttu-id="9f19e-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9f19e-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="9f19e-117">Parámetro que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="9f19e-117">The parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="9f19e-118">Parámetro ParamValue</span><span class="sxs-lookup"><span data-stu-id="9f19e-118">paramValue</span></span>  
    <span data-ttu-id="9f19e-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="9f19e-119">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="9f19e-120">Valor del parámetro que se va a establecer si el parámetro es un JET_CALLBACK.</span><span class="sxs-lookup"><span data-stu-id="9f19e-120">The value of the parameter to set, if the parameter is a JET_CALLBACK.</span></span>

<!-- end list -->

  - <span data-ttu-id="9f19e-121">paramString</span><span class="sxs-lookup"><span data-stu-id="9f19e-121">paramString</span></span>  
    <span data-ttu-id="9f19e-122">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9f19e-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9f19e-123">Valor del parámetro que se va a establecer, si el parámetro es un tipo de cadena.</span><span class="sxs-lookup"><span data-stu-id="9f19e-123">The value of the parameter to set, if the parameter is a string type.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9f19e-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f19e-124">Return value</span></span>

<span data-ttu-id="9f19e-125">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9f19e-125">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="9f19e-126">Código de advertencia de ESENT.</span><span class="sxs-lookup"><span data-stu-id="9f19e-126">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9f19e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f19e-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f19e-128">Referencia</span><span class="sxs-lookup"><span data-stu-id="9f19e-128">Reference</span></span>

[<span data-ttu-id="9f19e-129">Clase de API</span><span class="sxs-lookup"><span data-stu-id="9f19e-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9f19e-130">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="9f19e-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9f19e-131">Sobrecarga JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9f19e-131">JetSetSystemParameter overload</span></span>](./api.jetsetsystemparameter-method.md)

[<span data-ttu-id="9f19e-132">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9f19e-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
