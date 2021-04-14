---
description: El método Sequence del objeto Session abre una consulta en la tabla especificada, ordenando las acciones por los números de la columna Sequence.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Session. Sequence (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653974"
---
# <a name="sessionsequence-method"></a><span data-ttu-id="8926a-103">Session. Sequence (método)</span><span class="sxs-lookup"><span data-stu-id="8926a-103">Session.Sequence method</span></span>

<span data-ttu-id="8926a-104">El método **Sequence** del objeto [**Session**](session-object.md) abre una consulta en la tabla especificada, ordenando las acciones por los números de la columna Sequence.</span><span class="sxs-lookup"><span data-stu-id="8926a-104">The **Sequence** method of the [**Session**](session-object.md) object opens a query on the specified table, ordering the actions by the numbers in the Sequence column.</span></span> <span data-ttu-id="8926a-105">Para cada fila capturada, se llama al método [**OnAction**](session-doaction.md) , siempre que cualquier expresión de condición proporcionada no se evalúe como false.</span><span class="sxs-lookup"><span data-stu-id="8926a-105">For each row fetched, the [**DoAction**](session-doaction.md) method is called, provided that any supplied condition expression does not evaluate to False.</span></span> <span data-ttu-id="8926a-106">Devuelve una enumeración msiDoActionStatusEnum, tal y como se describe en el método [**OnAction**](session-doaction.md) .</span><span class="sxs-lookup"><span data-stu-id="8926a-106">Returns an enumeration msiDoActionStatusEnum, as described in the [**DoAction**](session-doaction.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8926a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8926a-107">Syntax</span></span>


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a><span data-ttu-id="8926a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8926a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8926a-109">*table*</span><span class="sxs-lookup"><span data-stu-id="8926a-109">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="8926a-110">Nombre de cadena requerido de la tabla que se va a utilizar para la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="8926a-110">Required string name of the table to use for sequencing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8926a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8926a-111">Return value</span></span>

<span data-ttu-id="8926a-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8926a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8926a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8926a-113">Remarks</span></span>

<span data-ttu-id="8926a-114">Normalmente, se llama a este método internamente mediante acciones de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="8926a-114">This method is normally called internally by top-level actions.</span></span>

<span data-ttu-id="8926a-115">Una secuencia de acciones que contiene acciones que actualizan el sistema, como las acciones [InstallFiles](installfiles-action.md) y [WriteRegistryValues](writeregistryvalues-action.md) , no se puede ejecutar llamando al método **Sequence** .</span><span class="sxs-lookup"><span data-stu-id="8926a-115">An action sequence containing actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **Sequence** method.</span></span> <span data-ttu-id="8926a-116">La excepción a esta regla es si se llama al método de **secuencia** desde una acción personalizada programada en la [tabla InstallExecuteSequence](installexecutesequence-table.md) entre las acciones [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="8926a-116">The exception to this rule is if the **Sequence** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="8926a-117">Se puede llamar a las acciones que no actualizan el sistema, como [AppSearch](appsearch-action.md) o [CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="8926a-117">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="8926a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8926a-118">Requirements</span></span>



| <span data-ttu-id="8926a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8926a-119">Requirement</span></span> | <span data-ttu-id="8926a-120">Value</span><span class="sxs-lookup"><span data-stu-id="8926a-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8926a-121">Versión</span><span class="sxs-lookup"><span data-stu-id="8926a-121">Version</span></span><br/> | <span data-ttu-id="8926a-122">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8926a-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8926a-123">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8926a-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8926a-124">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="8926a-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8926a-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8926a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="8926a-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8926a-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8926a-127">IID</span><span class="sxs-lookup"><span data-stu-id="8926a-127">IID</span></span><br/>     | <span data-ttu-id="8926a-128">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8926a-128">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




