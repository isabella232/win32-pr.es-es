---
description: Quita el objeto OID especificado de la colección.
ms.assetid: c5eb6831-b195-4dc1-a6bd-d4245f9b0213
title: OID. Remove (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 000310e0034d413dea16a45f79647c3e0f7cf52d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690063"
---
# <a name="oidsremove-method"></a><span data-ttu-id="0c3c2-103">OID. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="0c3c2-103">OIDs.Remove method</span></span>

<span data-ttu-id="0c3c2-104">\[El método **Remove** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="0c3c2-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0c3c2-105">En su lugar, use la [**clase OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="0c3c2-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="0c3c2-106">El método **Remove** quita el objeto [**OID**](oid.md) especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="0c3c2-106">The **Remove** method removes the specified [**OID**](oid.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c3c2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c3c2-107">Syntax</span></span>


```VB
OIDs.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="0c3c2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c3c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c3c2-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0c3c2-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c3c2-110">Índice del objeto [**OID**](oid.md) que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="0c3c2-110">Index of the [**OID**](oid.md) object to be removed.</span></span> <span data-ttu-id="0c3c2-111">Puede ser un índice de la colección o el valor con puntos del OID.</span><span class="sxs-lookup"><span data-stu-id="0c3c2-111">This can be either an index into the collection or the dotted value of the OID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c3c2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c3c2-112">Return value</span></span>

<span data-ttu-id="0c3c2-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0c3c2-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c3c2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c3c2-114">Requirements</span></span>



| <span data-ttu-id="0c3c2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c3c2-115">Requirement</span></span> | <span data-ttu-id="0c3c2-116">Value</span><span class="sxs-lookup"><span data-stu-id="0c3c2-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c3c2-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0c3c2-117">Redistributable</span></span><br/> | <span data-ttu-id="0c3c2-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c3c2-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0c3c2-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c3c2-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="0c3c2-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c3c2-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
