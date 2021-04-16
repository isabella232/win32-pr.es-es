---
description: El método fetch del objeto View recupera la siguiente fila de datos de columna si hay más filas disponibles en el conjunto de resultados; en caso contrario, es NULL. Llame al método Execute antes del método Fetch.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: View. fetch (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678981"
---
# <a name="viewfetch-method"></a><span data-ttu-id="bab27-104">View. fetch (método)</span><span class="sxs-lookup"><span data-stu-id="bab27-104">View.Fetch method</span></span>

<span data-ttu-id="bab27-105">El método **Fetch** del objeto [**View**](view-object.md) recupera la siguiente fila de datos de columna si hay más filas disponibles en el conjunto de resultados; en caso contrario, es NULL.</span><span class="sxs-lookup"><span data-stu-id="bab27-105">The **Fetch** method of the [**View**](view-object.md) object retrieves the next row of column data if more rows are available in the result set, otherwise it is Null.</span></span> <span data-ttu-id="bab27-106">Llame al método [**Execute**](view-execute.md) antes del método **Fetch** .</span><span class="sxs-lookup"><span data-stu-id="bab27-106">Call the [**Execute**](view-execute.md) method before the **Fetch** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab27-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bab27-107">Syntax</span></span>


```JScript
View.Fetch()
```



## <a name="parameters"></a><span data-ttu-id="bab27-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bab27-108">Parameters</span></span>

<span data-ttu-id="bab27-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bab27-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bab27-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bab27-110">Return value</span></span>

<span data-ttu-id="bab27-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bab27-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab27-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bab27-112">Remarks</span></span>

<span data-ttu-id="bab27-113">Se debe usar el mismo objeto de [**registro**](record-object.md) para recuperar los datos de varias filas, o bien se debe liberar el objeto saliendo del ámbito.</span><span class="sxs-lookup"><span data-stu-id="bab27-113">The same [**Record**](record-object.md) object should be used to retrieve the data in multiple rows, or else the object should be released by going out of scope.</span></span> <span data-ttu-id="bab27-114">El registro se puede probar para el final del conjunto de resultados mediante la sintaxis "If FetchRecord is Nothing".</span><span class="sxs-lookup"><span data-stu-id="bab27-114">The record can be tested for the end of the result set using the syntax "If FetchRecord Is Nothing".</span></span>

## <a name="requirements"></a><span data-ttu-id="bab27-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bab27-115">Requirements</span></span>



| <span data-ttu-id="bab27-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bab27-116">Requirement</span></span> | <span data-ttu-id="bab27-117">Value</span><span class="sxs-lookup"><span data-stu-id="bab27-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bab27-118">Versión</span><span class="sxs-lookup"><span data-stu-id="bab27-118">Version</span></span><br/> | <span data-ttu-id="bab27-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bab27-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bab27-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bab27-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bab27-121">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="bab27-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bab27-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bab27-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="bab27-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bab27-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bab27-124">IID</span><span class="sxs-lookup"><span data-stu-id="bab27-124">IID</span></span><br/>     | <span data-ttu-id="bab27-125">IID \_ iView se define como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bab27-125">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




