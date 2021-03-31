---
description: 'Más información sobre: método API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)'
title: Método API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.Int32@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100727
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 840c17ef1d74b57b4bee75b9efafe5a314f09a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907780"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-int32-string-int32"></a><span data-ttu-id="a24c0-103">Método API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</span><span class="sxs-lookup"><span data-stu-id="a24c0-103">Api.JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</span></span>

<span data-ttu-id="a24c0-104">Obtiene las opciones de configuración de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a24c0-104">Gets database configuration options.</span></span>

<span data-ttu-id="a24c0-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a24c0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a24c0-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a24c0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a24c0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a24c0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As Integer, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As Integer
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref int paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a><span data-ttu-id="a24c0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a24c0-108">Parameters</span></span>

  - <span data-ttu-id="a24c0-109">instance</span><span class="sxs-lookup"><span data-stu-id="a24c0-109">instance</span></span>  
    <span data-ttu-id="a24c0-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a24c0-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="a24c0-111">Instancia de de la que se van a recuperar las opciones.</span><span class="sxs-lookup"><span data-stu-id="a24c0-111">The instance to retrieve the options from.</span></span>

<!-- end list -->

  - <span data-ttu-id="a24c0-112">sesid</span><span class="sxs-lookup"><span data-stu-id="a24c0-112">sesid</span></span>  
    <span data-ttu-id="a24c0-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a24c0-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a24c0-114">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="a24c0-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a24c0-115">paramid</span><span class="sxs-lookup"><span data-stu-id="a24c0-115">paramid</span></span>  
    <span data-ttu-id="a24c0-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a24c0-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="a24c0-117">Parámetro que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="a24c0-117">The parameter to get.</span></span>

<!-- end list -->

  - <span data-ttu-id="a24c0-118">Parámetro ParamValue</span><span class="sxs-lookup"><span data-stu-id="a24c0-118">paramValue</span></span>  
    <span data-ttu-id="a24c0-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a24c0-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a24c0-120">Devuelve el valor del parámetro si el valor es un entero.</span><span class="sxs-lookup"><span data-stu-id="a24c0-120">Returns the value of the parameter, if the value is an integer.</span></span>

<!-- end list -->

  - <span data-ttu-id="a24c0-121">paramString</span><span class="sxs-lookup"><span data-stu-id="a24c0-121">paramString</span></span>  
    <span data-ttu-id="a24c0-122">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a24c0-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a24c0-123">Devuelve el valor del parámetro, si el valor es una cadena.</span><span class="sxs-lookup"><span data-stu-id="a24c0-123">Returns the value of the parameter, if the value is a string.</span></span>

<!-- end list -->

  - <span data-ttu-id="a24c0-124">maxParam</span><span class="sxs-lookup"><span data-stu-id="a24c0-124">maxParam</span></span>  
    <span data-ttu-id="a24c0-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a24c0-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a24c0-126">Tamaño máximo de la cadena de parámetro.</span><span class="sxs-lookup"><span data-stu-id="a24c0-126">The maximum size of the parameter string.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a24c0-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a24c0-127">Return value</span></span>

<span data-ttu-id="a24c0-128">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a24c0-128">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="a24c0-129">Código de advertencia de ESENT.</span><span class="sxs-lookup"><span data-stu-id="a24c0-129">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="a24c0-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a24c0-130">Remarks</span></span>

<span data-ttu-id="a24c0-131">[ErrorToString](./jet-param-enumeration.md) pasa el número de error en paramValue, que es el motivo por el que es un parámetro ref y no un parámetro out.</span><span class="sxs-lookup"><span data-stu-id="a24c0-131">[ErrorToString](./jet-param-enumeration.md) passes in the error number in the paramValue, which is why it is a ref parameter and not an out parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="a24c0-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a24c0-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a24c0-133">Referencia</span><span class="sxs-lookup"><span data-stu-id="a24c0-133">Reference</span></span>

[<span data-ttu-id="a24c0-134">Clase de API</span><span class="sxs-lookup"><span data-stu-id="a24c0-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a24c0-135">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="a24c0-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a24c0-136">Sobrecarga JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a24c0-136">JetGetSystemParameter overload</span></span>](./api.jetgetsystemparameter-method.md)

[<span data-ttu-id="a24c0-137">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a24c0-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
