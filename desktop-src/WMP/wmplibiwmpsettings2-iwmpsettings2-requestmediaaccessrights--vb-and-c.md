---
title: IWMPSettings2 requestMediaAccessRights, método
description: El método requestMediaAccessRights solicita un nivel de acceso especificado a la biblioteca. | IWMPSettings2 requestMediaAccessRights, método
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- método requestMediaAccessRights de Windows Media Player
- método requestMediaAccessRights Windows Media Player, interfaz IWMPSettings2
- Interfaz IWMPSettings2 Windows Media Player, método requestMediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690420"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a><span data-ttu-id="f2764-107">IWMPSettings2:: requestMediaAccessRights (método)</span><span class="sxs-lookup"><span data-stu-id="f2764-107">IWMPSettings2::requestMediaAccessRights method</span></span>

<span data-ttu-id="f2764-108">El método **requestMediaAccessRights** solicita un nivel de acceso especificado a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f2764-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2764-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2764-109">Syntax</span></span>


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a><span data-ttu-id="f2764-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2764-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2764-111">*bstrDesiredAccess* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2764-111">*bstrDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2764-112">**System. String** que es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f2764-112">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="f2764-113">Value</span><span class="sxs-lookup"><span data-stu-id="f2764-113">Value</span></span> | <span data-ttu-id="f2764-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2764-114">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="f2764-115">ninguno</span><span class="sxs-lookup"><span data-stu-id="f2764-115">none</span></span>  | <span data-ttu-id="f2764-116">Solo los derechos de acceso a elementos actuales.</span><span class="sxs-lookup"><span data-stu-id="f2764-116">Current item access rights only.</span></span> |
| <span data-ttu-id="f2764-117">leer</span><span class="sxs-lookup"><span data-stu-id="f2764-117">read</span></span>  | <span data-ttu-id="f2764-118">Solo derechos de acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="f2764-118">Read access rights only.</span></span>         |
| <span data-ttu-id="f2764-119">full</span><span class="sxs-lookup"><span data-stu-id="f2764-119">full</span></span>  | <span data-ttu-id="f2764-120">Derechos de acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f2764-120">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2764-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2764-121">Return value</span></span>

<span data-ttu-id="f2764-122">**System. Boolean** que indica si se han concedido los derechos de acceso solicitados.</span><span class="sxs-lookup"><span data-stu-id="f2764-122">A **System.Boolean** that indicates whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2764-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2764-123">Remarks</span></span>

<span data-ttu-id="f2764-124">Una página web debe solicitar primero el permiso del usuario para leer o escribir datos en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f2764-124">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="f2764-125">Al invocar este método, se solicita al usuario un cuadro de diálogo que solicita el nivel de permiso especificado.</span><span class="sxs-lookup"><span data-stu-id="f2764-125">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="f2764-126">Esto significa que ciertos métodos, propiedades y eventos serán inaccesibles desde el código si no se han concedido los derechos de acceso correspondientes.</span><span class="sxs-lookup"><span data-stu-id="f2764-126">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="f2764-127">El nivel de derechos de acceso actual se puede recuperar mediante **IWMPSettings2. mediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="f2764-127">The current access rights level can be retrieved by using **IWMPSettings2.mediaAccessRights**.</span></span>

<span data-ttu-id="f2764-128">No es necesario que las aplicaciones que se ejecutan en el equipo del usuario utilicen este método.</span><span class="sxs-lookup"><span data-stu-id="f2764-128">Applications running on the user's computer are not required to use this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2764-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2764-129">Requirements</span></span>



| <span data-ttu-id="f2764-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2764-130">Requirement</span></span> | <span data-ttu-id="f2764-131">Value</span><span class="sxs-lookup"><span data-stu-id="f2764-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2764-132">Versión</span><span class="sxs-lookup"><span data-stu-id="f2764-132">Version</span></span><br/>   | <span data-ttu-id="f2764-133">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="f2764-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f2764-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f2764-134">Namespace</span></span><br/> | <span data-ttu-id="f2764-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f2764-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f2764-136">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="f2764-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f2764-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f2764-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2764-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2764-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2764-139">**Interfaz IWMPSettings2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f2764-139">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f2764-140">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f2764-140">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





