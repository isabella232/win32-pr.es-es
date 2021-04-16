---
description: Agrega un objeto de atributo a la colección.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Attributes. Add (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 824bff2fcca190e25f9b9c63ba0964674aff9fb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671620"
---
# <a name="attributesadd-method"></a><span data-ttu-id="4a914-103">Attributes. Add (método)</span><span class="sxs-lookup"><span data-stu-id="4a914-103">Attributes.Add method</span></span>

<span data-ttu-id="4a914-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a914-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="4a914-105">En su lugar, use la [**clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="4a914-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="4a914-106">El método **Add** agrega un objeto de [**atributo**](attribute.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="4a914-106">The **Add** method adds an [**Attribute**](attribute.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a914-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a914-107">Syntax</span></span>


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a><span data-ttu-id="4a914-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a914-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a914-109">*Atributo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4a914-109">*Attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a914-110">Objeto de [**atributo**](attribute.md) que se va a agregar al final de la colección.</span><span class="sxs-lookup"><span data-stu-id="4a914-110">The [**Attribute**](attribute.md) object to be added at the end of the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a914-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a914-111">Return value</span></span>

<span data-ttu-id="4a914-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4a914-112">This method does not return a value.</span></span> <span data-ttu-id="4a914-113">Una aplicación que utiliza este método debe contener código para controlar una excepción generada por este método.</span><span class="sxs-lookup"><span data-stu-id="4a914-113">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a914-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a914-114">Requirements</span></span>



| <span data-ttu-id="4a914-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a914-115">Requirement</span></span> | <span data-ttu-id="4a914-116">Value</span><span class="sxs-lookup"><span data-stu-id="4a914-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a914-117">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4a914-117">End of client support</span></span><br/> | <span data-ttu-id="4a914-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a914-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4a914-119">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4a914-119">End of server support</span></span><br/> | <span data-ttu-id="4a914-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a914-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4a914-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4a914-121">Redistributable</span></span><br/>       | <span data-ttu-id="4a914-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a914-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4a914-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a914-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4a914-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a914-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a914-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a914-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a914-126">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="4a914-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="4a914-127">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="4a914-127">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
