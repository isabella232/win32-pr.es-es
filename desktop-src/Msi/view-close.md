---
description: El método Close del objeto View finaliza la ejecución de la consulta y libera los recursos de la base de datos.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: View. Close (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680329"
---
# <a name="viewclose-method"></a><span data-ttu-id="0a5ce-103">View. Close (método)</span><span class="sxs-lookup"><span data-stu-id="0a5ce-103">View.Close method</span></span>

<span data-ttu-id="0a5ce-104">El método **Close** del objeto [**View**](view-object.md) finaliza la ejecución de la consulta y libera los recursos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-104">The **Close** method of the [**View**](view-object.md) object terminates query execution and releases database resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a5ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a5ce-105">Syntax</span></span>


```JScript
View.Close()
```



## <a name="parameters"></a><span data-ttu-id="0a5ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a5ce-106">Parameters</span></span>

<span data-ttu-id="0a5ce-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a5ce-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a5ce-108">Return value</span></span>

<span data-ttu-id="0a5ce-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a5ce-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a5ce-110">Remarks</span></span>

<span data-ttu-id="0a5ce-111">Se debe llamar a este método antes de volver a llamar al método [**Execute**](view-execute.md) en el objeto de [**vista**](view-object.md) , a menos que se hayan obtenido todas las filas del conjunto de resultados con el método [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="0a5ce-111">This method must be called before the [**Execute**](view-execute.md) method is called again on the [**View**](view-object.md) object unless all rows of the result set have been obtained with the [**Fetch**](view-fetch.md) method.</span></span> <span data-ttu-id="0a5ce-112">Se llama internamente cuando se destruye la vista.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-112">It is called internally when the view is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a5ce-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a5ce-113">Requirements</span></span>



| <span data-ttu-id="0a5ce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a5ce-114">Requirement</span></span> | <span data-ttu-id="0a5ce-115">Value</span><span class="sxs-lookup"><span data-stu-id="0a5ce-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a5ce-116">Versión</span><span class="sxs-lookup"><span data-stu-id="0a5ce-116">Version</span></span><br/> | <span data-ttu-id="0a5ce-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0a5ce-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0a5ce-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0a5ce-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0a5ce-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a5ce-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="0a5ce-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a5ce-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0a5ce-122">IID</span><span class="sxs-lookup"><span data-stu-id="0a5ce-122">IID</span></span><br/>     | <span data-ttu-id="0a5ce-123">IID \_ iView se define como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0a5ce-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




