---
title: Error. Item (método)
description: El método Item recupera un objeto ErrorItem de la cola de errores.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, clase error
- Clase de error Windows Media Player, Item (método)
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698606"
---
# <a name="erroritem-method"></a><span data-ttu-id="58f5a-106">Error. Item (método)</span><span class="sxs-lookup"><span data-stu-id="58f5a-106">Error.item method</span></span>

<span data-ttu-id="58f5a-107">El método **Item** recupera un objeto **ErrorItem** de la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="58f5a-107">The **item** method retrieves an **ErrorItem** object from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f5a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58f5a-108">Syntax</span></span>


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="58f5a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58f5a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58f5a-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="58f5a-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58f5a-111">**Número** (**largo**) que contiene el índice del objeto **ErrorItem** que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="58f5a-111">**Number** (**long**) containing the index of the **ErrorItem** object to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58f5a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58f5a-112">Return value</span></span>

<span data-ttu-id="58f5a-113">Este método devuelve un objeto **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="58f5a-113">This method returns an **ErrorItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="58f5a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58f5a-114">Remarks</span></span>

<span data-ttu-id="58f5a-115">Windows Media Player puede generar una serie de errores en respuesta a una condición de error.</span><span class="sxs-lookup"><span data-stu-id="58f5a-115">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="58f5a-116">Este método permite la recuperación de un error específico en la cola mediante el uso de un número de índice.</span><span class="sxs-lookup"><span data-stu-id="58f5a-116">This method allows the retrieval of a specific error in the queue by using an index number.</span></span> <span data-ttu-id="58f5a-117">Los números de índice de la cola de errores comienzan por cero.</span><span class="sxs-lookup"><span data-stu-id="58f5a-117">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="58f5a-118">Debe establecer la *configuración*. **enableErrorDialogs** en false si elige mostrar mensajes de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="58f5a-118">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="58f5a-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="58f5a-119">Examples</span></span>

<span data-ttu-id="58f5a-120">En el siguiente ejemplo de JScript se utiliza el *error*. objeto de **elemento** en un controlador de eventos para avisar al usuario del error más reciente.</span><span class="sxs-lookup"><span data-stu-id="58f5a-120">The following JScript example uses the *Error*.**item** object in an event handler to alert the user to the most recent error.</span></span> <span data-ttu-id="58f5a-121">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="58f5a-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

</SCRIPT> 

```



## <a name="requirements"></a><span data-ttu-id="58f5a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58f5a-122">Requirements</span></span>



| <span data-ttu-id="58f5a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="58f5a-123">Requirement</span></span> | <span data-ttu-id="58f5a-124">Value</span><span class="sxs-lookup"><span data-stu-id="58f5a-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58f5a-125">Versión</span><span class="sxs-lookup"><span data-stu-id="58f5a-125">Version</span></span><br/> | <span data-ttu-id="58f5a-126">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="58f5a-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="58f5a-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58f5a-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="58f5a-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58f5a-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58f5a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="58f5a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f5a-130">**Objeto de error**</span><span class="sxs-lookup"><span data-stu-id="58f5a-130">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="58f5a-131">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="58f5a-131">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





