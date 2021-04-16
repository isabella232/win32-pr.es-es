---
title: Propiedad mediaAccessRights de IWMPSettings2
description: La propiedad mediaAccessRights obtiene un valor que indica los permisos concedidos actualmente para el acceso a la biblioteca.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- propiedades de mediaAccessRights Media Player de Windows
- propiedad mediaAccessRights de Windows Media Player, interfaz IWMPSettings2
- Interfaz IWMPSettings2 Windows Media Player, propiedad mediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689940"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a><span data-ttu-id="65940-106">IWMPSettings2:: mediaAccessRights (propiedad)</span><span class="sxs-lookup"><span data-stu-id="65940-106">IWMPSettings2::mediaAccessRights property</span></span>

<span data-ttu-id="65940-107">La propiedad **mediaAccessRights** obtiene un valor que indica los permisos concedidos actualmente para el acceso a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="65940-107">The **mediaAccessRights** property gets a value indicating the permissions currently granted for library access.</span></span>

<span data-ttu-id="65940-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="65940-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="65940-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65940-109">Syntax</span></span>


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a><span data-ttu-id="65940-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="65940-110">Property value</span></span>

<span data-ttu-id="65940-111">**System. String** que es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="65940-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="65940-112">Value</span><span class="sxs-lookup"><span data-stu-id="65940-112">Value</span></span> | <span data-ttu-id="65940-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="65940-113">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="65940-114">ninguno</span><span class="sxs-lookup"><span data-stu-id="65940-114">none</span></span>  | <span data-ttu-id="65940-115">Solo los derechos de acceso a elementos actuales.</span><span class="sxs-lookup"><span data-stu-id="65940-115">Current item access rights only.</span></span> |
| <span data-ttu-id="65940-116">leer</span><span class="sxs-lookup"><span data-stu-id="65940-116">read</span></span>  | <span data-ttu-id="65940-117">Solo derechos de acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="65940-117">Read access rights only.</span></span>         |
| <span data-ttu-id="65940-118">full</span><span class="sxs-lookup"><span data-stu-id="65940-118">full</span></span>  | <span data-ttu-id="65940-119">Derechos de acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="65940-119">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="65940-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65940-120">Remarks</span></span>

<span data-ttu-id="65940-121">Una página web debe solicitar primero el permiso del usuario para leer o escribir datos en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="65940-121">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="65940-122">Esto significa que ciertos métodos, propiedades y eventos serán inaccesibles desde el código si no se han concedido los derechos de acceso correspondientes.</span><span class="sxs-lookup"><span data-stu-id="65940-122">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="65940-123">Para obtener derechos de acceso, la aplicación llama a **IWMPSettings2. Get \_ requestMediaAccessRights**, pasando un parámetro que especifica el nivel de derechos de acceso deseado.</span><span class="sxs-lookup"><span data-stu-id="65940-123">To obtain access rights, the application calls **IWMPSettings2.get\_requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="65940-124">Las aplicaciones que se ejecutan en el equipo del usuario siempre tienen derechos de acceso completo.</span><span class="sxs-lookup"><span data-stu-id="65940-124">Applications running on the user's computer always have full access rights.</span></span>

## <a name="requirements"></a><span data-ttu-id="65940-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65940-125">Requirements</span></span>



| <span data-ttu-id="65940-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="65940-126">Requirement</span></span> | <span data-ttu-id="65940-127">Value</span><span class="sxs-lookup"><span data-stu-id="65940-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65940-128">Versión</span><span class="sxs-lookup"><span data-stu-id="65940-128">Version</span></span><br/>   | <span data-ttu-id="65940-129">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="65940-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="65940-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="65940-130">Namespace</span></span><br/> | <span data-ttu-id="65940-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="65940-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="65940-132">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="65940-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="65940-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="65940-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65940-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="65940-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65940-135">**Interfaz IWMPSettings2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="65940-135">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="65940-136">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="65940-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





