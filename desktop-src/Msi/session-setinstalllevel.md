---
description: El método SetInstallLevel del objeto de sesión establece el nivel de instalación de la instalación actual en un valor especificado y vuelve a calcular los Estados Select e installed para todas las características de la tabla de características.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Método Session. SetInstallLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653972"
---
# <a name="sessionsetinstalllevel-method"></a><span data-ttu-id="32899-103">Método Session. SetInstallLevel</span><span class="sxs-lookup"><span data-stu-id="32899-103">Session.SetInstallLevel method</span></span>

<span data-ttu-id="32899-104">El método **SetInstallLevel** del objeto de [**sesión**](session-object.md) establece el nivel de instalación de la instalación actual en un valor especificado y vuelve a calcular los Estados Select e installed para todas las características de la tabla de características.</span><span class="sxs-lookup"><span data-stu-id="32899-104">The **SetInstallLevel** method of the [**Session**](session-object.md) object sets the install level for the current installation to a specified value and recalculates the Select and Installed states for all features in the Feature table.</span></span> <span data-ttu-id="32899-105">También establece el estado de la acción de cada componente en la [tabla de componentes](component-table.md) basándose en el nuevo nivel.</span><span class="sxs-lookup"><span data-stu-id="32899-105">It also sets the Action state of each component in the [Component table](component-table.md) based on the new level.</span></span>

## <a name="syntax"></a><span data-ttu-id="32899-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32899-106">Syntax</span></span>


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a><span data-ttu-id="32899-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32899-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32899-108">*installLevel*</span><span class="sxs-lookup"><span data-stu-id="32899-108">*installLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="32899-109">Requerido nuevo nivel de instalación solicitado.</span><span class="sxs-lookup"><span data-stu-id="32899-109">Required requested new install level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32899-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32899-110">Return value</span></span>

<span data-ttu-id="32899-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="32899-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32899-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32899-112">Remarks</span></span>

<span data-ttu-id="32899-113">La [acción CostInitialize](costinitialize-action.md) debe ejecutarse antes de llamar a **SetInstallLevel**.</span><span class="sxs-lookup"><span data-stu-id="32899-113">The [CostInitialize action](costinitialize-action.md) must be executed prior to calling **SetInstallLevel**.</span></span>

<span data-ttu-id="32899-114">Si se pasa 0 para el parámetro *installLevel* , no se cambia el nivel de instalación actual, pero todas las características se siguen actualizando según el nivel de instalación actual.</span><span class="sxs-lookup"><span data-stu-id="32899-114">If 0 is passed for the *installLevel* parameter, the current install level is not changed, but all features are still updated based on the current install level.</span></span> <span data-ttu-id="32899-115">Por ejemplo, el módulo controlador podría usar esta funcionalidad para restablecer todas las selecciones a sus Estados predeterminados iniciales en cualquier momento del proceso de selección de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="32899-115">For example, this functionality could be used by the Handler module to reset all selections back to their initial default states at any point in the UI selection process.</span></span>

<span data-ttu-id="32899-116">Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="32899-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="32899-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32899-117">Requirements</span></span>



| <span data-ttu-id="32899-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="32899-118">Requirement</span></span> | <span data-ttu-id="32899-119">Value</span><span class="sxs-lookup"><span data-stu-id="32899-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32899-120">Versión</span><span class="sxs-lookup"><span data-stu-id="32899-120">Version</span></span><br/> | <span data-ttu-id="32899-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="32899-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="32899-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32899-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="32899-123">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="32899-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="32899-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32899-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="32899-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32899-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="32899-126">IID</span><span class="sxs-lookup"><span data-stu-id="32899-126">IID</span></span><br/>     | <span data-ttu-id="32899-127">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="32899-127">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




