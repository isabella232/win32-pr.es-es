---
title: THEME. showErrorDialog
description: El método showErrorDialog muestra el cuadro de diálogo de error estándar.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- Media Player de Windows de THEME. showErrorDialog
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690450"
---
# <a name="themeshowerrordialog"></a><span data-ttu-id="fada3-104">THEME. showErrorDialog</span><span class="sxs-lookup"><span data-stu-id="fada3-104">THEME.showErrorDialog</span></span>

<span data-ttu-id="fada3-105">El método **showErrorDialog** muestra el cuadro de diálogo de error estándar.</span><span class="sxs-lookup"><span data-stu-id="fada3-105">The **showErrorDialog** method displays the standard error dialog box.</span></span>

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a><span data-ttu-id="fada3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fada3-106">Parameters</span></span>

<span data-ttu-id="fada3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fada3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fada3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fada3-108">Return Value</span></span>

<span data-ttu-id="fada3-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fada3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fada3-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fada3-110">Remarks</span></span>

<span data-ttu-id="fada3-111">Si **Settings. enableErrorDialogs** es false, este método se puede usar para mostrar el cuadro de diálogo de error mediante programación.</span><span class="sxs-lookup"><span data-stu-id="fada3-111">If **Settings.enableErrorDialogs** is false, this method can be used to programmatically display the error dialog.</span></span> <span data-ttu-id="fada3-112">Si no hay ningún error en la cola de errores, no se muestra el cuadro de diálogo de error.</span><span class="sxs-lookup"><span data-stu-id="fada3-112">If there are no errors in the error queue, the error dialog box is not shown.</span></span>

<span data-ttu-id="fada3-113">En Windows Media Player serie 9 o posterior, se debe llamar a este método desde el controlador de eventos de error.</span><span class="sxs-lookup"><span data-stu-id="fada3-113">For Windows Media Player 9 Series or later, this method must be called from the error event handler.</span></span> <span data-ttu-id="fada3-114">Windows Media Player serie 9 o posterior borra la cola de errores de las máscaras una vez que se ha desencadenado el evento de error.</span><span class="sxs-lookup"><span data-stu-id="fada3-114">Windows Media Player 9 Series or later clears the error queue for skins after the error event has been fired.</span></span>

## <a name="requirements"></a><span data-ttu-id="fada3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fada3-115">Requirements</span></span>



| <span data-ttu-id="fada3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fada3-116">Requirement</span></span> | <span data-ttu-id="fada3-117">Value</span><span class="sxs-lookup"><span data-stu-id="fada3-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fada3-118">Versión</span><span class="sxs-lookup"><span data-stu-id="fada3-118">Version</span></span><br/> | <span data-ttu-id="fada3-119">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="fada3-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fada3-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="fada3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fada3-121">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="fada3-121">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="fada3-122">**Settings. enableErrorDialogs**</span><span class="sxs-lookup"><span data-stu-id="fada3-122">**Settings.enableErrorDialogs**</span></span>](settings-enableerrordialogs.md)
</dt> </dl>

 

 





