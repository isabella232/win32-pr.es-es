---
description: El método OnAction del objeto de sesión ejecuta la función de acción correspondiente al nombre proporcionado.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Método Session. OnAction (fotoadquisición. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3084cfd51e7efbcfbfbc3cbcf2c9be21d8373d21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680410"
---
# <a name="sessiondoaction-method"></a><span data-ttu-id="8aaf5-103">Session. OnAction (método)</span><span class="sxs-lookup"><span data-stu-id="8aaf5-103">Session.DoAction method</span></span>

<span data-ttu-id="8aaf5-104">El método **OnAction** del objeto de [**sesión**](session-object.md) ejecuta la función de acción correspondiente al nombre proporcionado.</span><span class="sxs-lookup"><span data-stu-id="8aaf5-104">The **DoAction** method of the [**Session**](session-object.md) object executes the action function corresponding to the name supplied.</span></span> <span data-ttu-id="8aaf5-105">Si se proporciona un nombre de acción nulo, el motor utiliza el valor en mayúsculas de la [propiedad Action](action.md) como la acción que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="8aaf5-105">If a Null action name is supplied, the engine uses the uppercase value of the [ACTION property](action.md) as the action to perform.</span></span> <span data-ttu-id="8aaf5-106">Si no se define ningún valor de propiedad, se realiza la acción predeterminada, que se define actualmente como INSTALL.</span><span class="sxs-lookup"><span data-stu-id="8aaf5-106">If no property value is defined, the default action is performed, currently defined as INSTALL.</span></span> <span data-ttu-id="8aaf5-107">Este método devuelve una enumeración de enteros.</span><span class="sxs-lookup"><span data-stu-id="8aaf5-107">This method returns an integer enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aaf5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8aaf5-108">Syntax</span></span>


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a><span data-ttu-id="8aaf5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8aaf5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aaf5-110">*action*</span><span class="sxs-lookup"><span data-stu-id="8aaf5-110">*action*</span></span> 
</dt> <dd>

<span data-ttu-id="8aaf5-111">Nombre de cadena requerido de la acción que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="8aaf5-111">Required string name of the action to execute.</span></span> <span data-ttu-id="8aaf5-112">Distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8aaf5-112">Case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8aaf5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8aaf5-113">Return value</span></span>

<span data-ttu-id="8aaf5-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8aaf5-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aaf5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8aaf5-115">Remarks</span></span>

<span data-ttu-id="8aaf5-116">Las acciones que actualizan el sistema, como las acciones [InstallFiles](installfiles-action.md) y [WriteRegistryValues](writeregistryvalues-action.md) , no se pueden ejecutar llamando al método **OnAction** .</span><span class="sxs-lookup"><span data-stu-id="8aaf5-116">Actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **DoAction** method.</span></span> <span data-ttu-id="8aaf5-117">La excepción a esta regla es si se llama al método **OnAction** desde una acción personalizada programada en la [tabla InstallExecuteSequence](installexecutesequence-table.md) entre las acciones [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="8aaf5-117">The exception to this rule is if the **DoAction** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="8aaf5-118">Se puede llamar a las acciones que no actualizan el sistema, como [AppSearch](appsearch-action.md) o [CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="8aaf5-118">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aaf5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aaf5-119">Requirements</span></span>



| <span data-ttu-id="8aaf5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aaf5-120">Requirement</span></span> | <span data-ttu-id="8aaf5-121">Value</span><span class="sxs-lookup"><span data-stu-id="8aaf5-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aaf5-122">Versión</span><span class="sxs-lookup"><span data-stu-id="8aaf5-122">Version</span></span><br/> | <span data-ttu-id="8aaf5-123">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8aaf5-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8aaf5-124">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8aaf5-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8aaf5-125">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="8aaf5-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8aaf5-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8aaf5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8aaf5-127"><dt>Fotoadquisición. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aaf5-127"><dt>Photoacquire.h</dt></span></span> </dl>                                                                                                                                                               |
| <span data-ttu-id="8aaf5-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8aaf5-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="8aaf5-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8aaf5-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8aaf5-130">IID</span><span class="sxs-lookup"><span data-stu-id="8aaf5-130">IID</span></span><br/>     | <span data-ttu-id="8aaf5-131">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8aaf5-131">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




