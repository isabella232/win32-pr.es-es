---
description: Agrega el objeto OID especificado a la colección.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: OID. Add (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690561"
---
# <a name="oidsadd-method"></a><span data-ttu-id="b7942-103">OID. Add (método)</span><span class="sxs-lookup"><span data-stu-id="b7942-103">OIDs.Add method</span></span>

<span data-ttu-id="b7942-104">\[El método **Add** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b7942-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b7942-105">En su lugar, use la [**clase OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="b7942-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b7942-106">El método **Add** agrega el objeto [**OID**](oid.md) especificado a la colección.</span><span class="sxs-lookup"><span data-stu-id="b7942-106">The **Add** method adds the specified [**OID**](oid.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7942-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7942-107">Syntax</span></span>


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a><span data-ttu-id="b7942-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7942-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7942-109">*OID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7942-109">*OID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7942-110">Objeto [**OID**](oid.md) que se va a agregar a la colección.</span><span class="sxs-lookup"><span data-stu-id="b7942-110">The [**OID**](oid.md) object to be added to the collection.</span></span> <span data-ttu-id="b7942-111">El objeto **OID** se agrega en el criterio de ordenación según su valor de puntos.</span><span class="sxs-lookup"><span data-stu-id="b7942-111">The **OID** object is added in sorted order based on its dotted value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7942-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7942-112">Return value</span></span>

<span data-ttu-id="b7942-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b7942-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7942-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7942-114">Requirements</span></span>



| <span data-ttu-id="b7942-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7942-115">Requirement</span></span> | <span data-ttu-id="b7942-116">Value</span><span class="sxs-lookup"><span data-stu-id="b7942-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7942-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b7942-117">Redistributable</span></span><br/> | <span data-ttu-id="b7942-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7942-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b7942-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7942-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="b7942-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7942-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
