---
description: El método SWbemRefresher. Add agrega un nuevo objeto SWbemRefreshableItem a la colección en el objeto SWbemRefresher. Objeto SWbemRefreshableItem a la colección del objeto SWbemRefresher.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Método SWbemRefresher. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707537"
---
# <a name="swbemrefresheradd-method"></a><span data-ttu-id="2bd29-103">SWbemRefresher. Add (método)</span><span class="sxs-lookup"><span data-stu-id="2bd29-103">SWbemRefresher.Add method</span></span>

<span data-ttu-id="2bd29-104">El método **SWbemRefresher. Add** agrega un nuevo objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) a la colección en el objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd29-104">The **SWbemRefresher.Add** method adds a new [**SWbemRefreshableItem**](swbemrefreshableitem.md) object to the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="2bd29-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2bd29-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2bd29-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bd29-106">Syntax</span></span>


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2bd29-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bd29-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bd29-108">*objWbemService*</span><span class="sxs-lookup"><span data-stu-id="2bd29-108">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd29-109">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bd29-109">Required.</span></span> <span data-ttu-id="2bd29-110">Un objeto [**SWbemServices**](swbemservices.md) que representa una conexión con el espacio de nombres en el que reside el objeto que se va a agregar al actualizador.</span><span class="sxs-lookup"><span data-stu-id="2bd29-110">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="2bd29-111">*strInstancePath*</span><span class="sxs-lookup"><span data-stu-id="2bd29-111">*strInstancePath*</span></span> 
</dt> <dd>

<span data-ttu-id="2bd29-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bd29-112">Required.</span></span> <span data-ttu-id="2bd29-113">Cadena que contiene la ruta de acceso relativa del objeto en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="2bd29-113">String that contains the relative path of the object in the namespace.</span></span> <span data-ttu-id="2bd29-114">La ruta de acceso debe contener una instancia de.</span><span class="sxs-lookup"><span data-stu-id="2bd29-114">The path must contain an instance.</span></span> <span data-ttu-id="2bd29-115">La propiedad [**index**](swbemrefreshableitem-index.md) de la [**SWbemRefreshableItem**](swbemrefreshableitem.md) devuelta representa el índice del objeto en la colección del actualizador.</span><span class="sxs-lookup"><span data-stu-id="2bd29-115">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="2bd29-116">*iFlags* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="2bd29-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd29-117">Cadena que contiene la ruta de acceso del objeto para el que se ejecuta el método.</span><span class="sxs-lookup"><span data-stu-id="2bd29-117">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="2bd29-118">*objWbemNamedvalueSet* \[ opta\]</span><span class="sxs-lookup"><span data-stu-id="2bd29-118">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2bd29-119">Normalmente, esto no está definido.</span><span class="sxs-lookup"><span data-stu-id="2bd29-119">Typically, this is undefined.</span></span> <span data-ttu-id="2bd29-120">De lo contrario, se trata de un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cuyos elementos representan la información de contexto que puede usar el proveedor que presta servicio a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2bd29-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="2bd29-121">Un proveedor que admite o requiere tal información debe documentar los nombres de valor reconocidos, el tipo de datos del valor, los valores permitidos y la semántica.</span><span class="sxs-lookup"><span data-stu-id="2bd29-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bd29-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bd29-122">Return value</span></span>

<span data-ttu-id="2bd29-123">Si la llamada se realiza correctamente, se devuelve un objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) que contiene un solo objeto actualizable.</span><span class="sxs-lookup"><span data-stu-id="2bd29-123">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains a single refreshable object is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd29-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bd29-124">Requirements</span></span>



| <span data-ttu-id="2bd29-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd29-125">Requirement</span></span> | <span data-ttu-id="2bd29-126">Value</span><span class="sxs-lookup"><span data-stu-id="2bd29-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd29-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bd29-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd29-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2bd29-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2bd29-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bd29-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd29-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2bd29-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2bd29-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bd29-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd29-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bd29-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2bd29-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2bd29-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="2bd29-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2bd29-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2bd29-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2bd29-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bd29-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bd29-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2bd29-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="2bd29-137">CLSID</span></span><br/>                    | <span data-ttu-id="2bd29-138">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="2bd29-138">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="2bd29-139">IID</span><span class="sxs-lookup"><span data-stu-id="2bd29-139">IID</span></span><br/>                      | <span data-ttu-id="2bd29-140">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="2bd29-140">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="2bd29-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bd29-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd29-142">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="2bd29-142">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




