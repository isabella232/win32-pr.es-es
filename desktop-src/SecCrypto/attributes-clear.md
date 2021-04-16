---
description: Borra todos los objetos de atributo de la colección.
ms.assetid: 98b022f8-15aa-44b4-aaff-de09081d80b6
title: Attributes. Clear (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eec570200234f455467c30a3eb12429226400c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671263"
---
# <a name="attributesclear-method"></a><span data-ttu-id="9a7e3-103">Attributes. Clear (método)</span><span class="sxs-lookup"><span data-stu-id="9a7e3-103">Attributes.Clear method</span></span>

<span data-ttu-id="9a7e3-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9a7e3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="9a7e3-105">En su lugar, use la [**clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="9a7e3-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="9a7e3-106">El método **Clear** borra todos los objetos de [**atributo**](attribute.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="9a7e3-106">The **Clear** method clears all [**Attribute**](attribute.md) objects from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7e3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a7e3-107">Syntax</span></span>


```VB
Attributes.Clear()
```



## <a name="parameters"></a><span data-ttu-id="9a7e3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a7e3-108">Parameters</span></span>

<span data-ttu-id="9a7e3-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9a7e3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a7e3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a7e3-110">Return value</span></span>

<span data-ttu-id="9a7e3-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9a7e3-111">This method does not return a value.</span></span> <span data-ttu-id="9a7e3-112">Una aplicación que utiliza este método debe contener código para controlar una excepción generada por este método.</span><span class="sxs-lookup"><span data-stu-id="9a7e3-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7e3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a7e3-113">Requirements</span></span>



| <span data-ttu-id="9a7e3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a7e3-114">Requirement</span></span> | <span data-ttu-id="9a7e3-115">Value</span><span class="sxs-lookup"><span data-stu-id="9a7e3-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7e3-116">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9a7e3-116">End of client support</span></span><br/> | <span data-ttu-id="9a7e3-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a7e3-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9a7e3-118">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="9a7e3-118">End of server support</span></span><br/> | <span data-ttu-id="9a7e3-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a7e3-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9a7e3-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="9a7e3-120">Redistributable</span></span><br/>       | <span data-ttu-id="9a7e3-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a7e3-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9a7e3-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a7e3-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9a7e3-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a7e3-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a7e3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a7e3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7e3-125">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="9a7e3-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="9a7e3-126">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="9a7e3-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
