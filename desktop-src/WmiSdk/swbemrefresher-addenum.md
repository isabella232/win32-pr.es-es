---
description: Agrega un nuevo enumerador al objeto SWbemRefresher. Este enumerador es para todas las instancias de la clase que se especifica en el parámetro strClass.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Método SWbemRefresher. AddEnum (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820223"
---
# <a name="swbemrefresheraddenum-method"></a><span data-ttu-id="ddc79-104">SWbemRefresher. AddEnum, método</span><span class="sxs-lookup"><span data-stu-id="ddc79-104">SWbemRefresher.AddEnum method</span></span>

<span data-ttu-id="ddc79-105">El método **SWbemRefresher. AddEnum** agrega un nuevo enumerador al objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="ddc79-105">The **SWbemRefresher.AddEnum** method adds a new enumerator to the [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="ddc79-106">Este enumerador es para todas las instancias de la clase que se especifica en el parámetro *strClass* .</span><span class="sxs-lookup"><span data-stu-id="ddc79-106">This enumerator is for all the instances of the class that is specified in the *strClass* parameter.</span></span>

<span data-ttu-id="ddc79-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ddc79-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc79-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddc79-108">Syntax</span></span>


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ddc79-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddc79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddc79-110">*objWbemService*</span><span class="sxs-lookup"><span data-stu-id="ddc79-110">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="ddc79-111">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ddc79-111">Required.</span></span> <span data-ttu-id="ddc79-112">Un objeto [**SWbemServices**](swbemservices.md) que representa una conexión con el espacio de nombres en el que reside el objeto que se va a agregar al actualizador.</span><span class="sxs-lookup"><span data-stu-id="ddc79-112">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="ddc79-113">*strClass*</span><span class="sxs-lookup"><span data-stu-id="ddc79-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="ddc79-114">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ddc79-114">Required.</span></span> <span data-ttu-id="ddc79-115">Cadena que contiene la clase que se va a agregar al actualizador.</span><span class="sxs-lookup"><span data-stu-id="ddc79-115">String that contains the class that is being added to the refresher.</span></span> <span data-ttu-id="ddc79-116">Esta clase se usa como un enumerador de las instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="ddc79-116">This class is used as an enumerator of the instances of the class.</span></span> <span data-ttu-id="ddc79-117">La propiedad [**index**](swbemrefreshableitem-index.md) del [**SWbemRefreshableItem**](swbemrefreshableitem.md) devuelto representa el índice del enumerador en la colección de actualizador.</span><span class="sxs-lookup"><span data-stu-id="ddc79-117">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the enumerator in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="ddc79-118">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="ddc79-118">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc79-119">Cadena que contiene la ruta de acceso del objeto para el que se ejecuta el método.</span><span class="sxs-lookup"><span data-stu-id="ddc79-119">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="ddc79-120">*objWbemNamedvalueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="ddc79-120">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ddc79-121">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="ddc79-121">Typically, this is undefined.</span></span> <span data-ttu-id="ddc79-122">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que presta servicio a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ddc79-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="ddc79-123">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="ddc79-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddc79-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddc79-124">Return value</span></span>

<span data-ttu-id="ddc79-125">Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) que contiene un enumerador para todas las instancias de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="ddc79-125">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains an enumerator for all the instances for the specified class is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc79-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddc79-126">Requirements</span></span>



| <span data-ttu-id="ddc79-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddc79-127">Requirement</span></span> | <span data-ttu-id="ddc79-128">Value</span><span class="sxs-lookup"><span data-stu-id="ddc79-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc79-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddc79-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ddc79-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddc79-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ddc79-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddc79-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ddc79-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddc79-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ddc79-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddc79-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddc79-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddc79-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ddc79-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ddc79-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="ddc79-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ddc79-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ddc79-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ddc79-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddc79-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddc79-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ddc79-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="ddc79-139">CLSID</span></span><br/>                    | <span data-ttu-id="ddc79-140">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="ddc79-140">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="ddc79-141">IID</span><span class="sxs-lookup"><span data-stu-id="ddc79-141">IID</span></span><br/>                      | <span data-ttu-id="ddc79-142">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="ddc79-142">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="ddc79-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddc79-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc79-144">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="ddc79-144">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




