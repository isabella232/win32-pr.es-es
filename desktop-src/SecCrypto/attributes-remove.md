---
description: Quita un objeto de atributo indizado de la colección.
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Attributes. Remove (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5981176afb332254d98171d40027e43383cb557
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671238"
---
# <a name="attributesremove-method"></a><span data-ttu-id="17895-103">Attributes. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="17895-103">Attributes.Remove method</span></span>

<span data-ttu-id="17895-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="17895-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="17895-105">En su lugar, use la [**clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="17895-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="17895-106">El método **Remove** quita un objeto de [**atributo**](attribute.md) indizado de la colección.</span><span class="sxs-lookup"><span data-stu-id="17895-106">The **Remove** method removes an indexed [**Attribute**](attribute.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="17895-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17895-107">Syntax</span></span>


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="17895-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17895-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17895-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="17895-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17895-110">Índice del objeto de [**atributo**](attribute.md) que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="17895-110">Index of the [**Attribute**](attribute.md) object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17895-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17895-111">Return value</span></span>

<span data-ttu-id="17895-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="17895-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17895-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17895-113">Remarks</span></span>

<span data-ttu-id="17895-114">Las aplicaciones que utilizan este método deben contener código para controlar una excepción generada por este método.</span><span class="sxs-lookup"><span data-stu-id="17895-114">Applications that use this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="17895-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17895-115">Requirements</span></span>



| <span data-ttu-id="17895-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="17895-116">Requirement</span></span> | <span data-ttu-id="17895-117">Value</span><span class="sxs-lookup"><span data-stu-id="17895-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17895-118">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="17895-118">End of client support</span></span><br/> | <span data-ttu-id="17895-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17895-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="17895-120">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="17895-120">End of server support</span></span><br/> | <span data-ttu-id="17895-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17895-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="17895-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="17895-122">Redistributable</span></span><br/>       | <span data-ttu-id="17895-123">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="17895-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="17895-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17895-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="17895-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17895-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17895-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="17895-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17895-127">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="17895-127">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="17895-128">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="17895-128">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
