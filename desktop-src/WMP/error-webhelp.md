---
title: Error. WebHelp (método)
description: El método WebHelp inicia la página de ayuda Web de Windows Media Player para mostrar información adicional sobre el primer error en la cola de errores (índice cero). | Error. WebHelp (método)
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- método WebHelp Windows Media Player
- método WebHelp Windows Media Player, clase error
- Clase de error Windows Media Player, método WebHelp
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700108"
---
# <a name="errorwebhelp-method"></a><span data-ttu-id="983c9-107">Error. WebHelp (método)</span><span class="sxs-lookup"><span data-stu-id="983c9-107">Error.webHelp method</span></span>

<span data-ttu-id="983c9-108">El método **WebHelp** inicia la página de ayuda Web de Windows Media Player para mostrar información adicional sobre el primer error en la cola de errores (índice cero).</span><span class="sxs-lookup"><span data-stu-id="983c9-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="983c9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="983c9-109">Syntax</span></span>


```JScript
Error.webHelp()
```



## <a name="parameters"></a><span data-ttu-id="983c9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="983c9-110">Parameters</span></span>

<span data-ttu-id="983c9-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="983c9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="983c9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="983c9-112">Return value</span></span>

<span data-ttu-id="983c9-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="983c9-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="983c9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="983c9-114">Remarks</span></span>

<span data-ttu-id="983c9-115">Las páginas de ayuda web siempre contienen la información más reciente y más detallada sobre los errores de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="983c9-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="983c9-116">Este método transfiere automáticamente la otra información que necesita la ayuda Web, como la versión del sistema operativo que se está usando.</span><span class="sxs-lookup"><span data-stu-id="983c9-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="983c9-117">Para tener acceso directamente a las páginas de ayuda Web, use el código de error y los vínculos del centro de soporte técnico siguientes.</span><span class="sxs-lookup"><span data-stu-id="983c9-117">To access the Web Help pages directly, use the following error code and support center links.</span></span>

-   [<span data-ttu-id="983c9-118">Información del código de error de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="983c9-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="983c9-119">Centro de soluciones de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="983c9-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

<span data-ttu-id="983c9-120">**Windows Media Player 10 Mobile:** Este método siempre se realiza correctamente, pero no realiza la operación deseada.</span><span class="sxs-lookup"><span data-stu-id="983c9-120">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="examples"></a><span data-ttu-id="983c9-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="983c9-121">Examples</span></span>

<span data-ttu-id="983c9-122">En el ejemplo siguiente se crea un elemento de botón HTML que inicia la página de ayuda Web de Microsoft Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="983c9-122">The following example creates an HTML BUTTON element that launches the Microsoft Windows Media Player Web Help page.</span></span> <span data-ttu-id="983c9-123">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="983c9-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a><span data-ttu-id="983c9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="983c9-124">Requirements</span></span>



| <span data-ttu-id="983c9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="983c9-125">Requirement</span></span> | <span data-ttu-id="983c9-126">Value</span><span class="sxs-lookup"><span data-stu-id="983c9-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="983c9-127">Versión</span><span class="sxs-lookup"><span data-stu-id="983c9-127">Version</span></span><br/> | <span data-ttu-id="983c9-128">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="983c9-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="983c9-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="983c9-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="983c9-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="983c9-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="983c9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="983c9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983c9-132">**Objeto de error**</span><span class="sxs-lookup"><span data-stu-id="983c9-132">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





