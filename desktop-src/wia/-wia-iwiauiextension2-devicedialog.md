---
description: Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: IWiaUIExtension2::D método eviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 142ec77572708063e24b38d342fb49f69c7651c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275455"
---
# <a name="iwiauiextension2devicedialog-method"></a><span data-ttu-id="3bc71-103">IWiaUIExtension2::D método eviceDialog</span><span class="sxs-lookup"><span data-stu-id="3bc71-103">IWiaUIExtension2::DeviceDialog method</span></span>

<span data-ttu-id="3bc71-104">Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="3bc71-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bc71-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bc71-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="3bc71-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bc71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bc71-107">*pDeviceDialogData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3bc71-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bc71-108">Tipo: \**PDEVICEDIALOGDATA2 \** _</span><span class="sxs-lookup"><span data-stu-id="3bc71-108">Type: \**PDEVICEDIALOGDATA2\** _</span></span>

<span data-ttu-id="3bc71-109">Apunta a una estructura [_ *DEVICEDIALOGDATA2* \*](-wia-devicedialogdata2.md) que contiene todos los datos necesarios para implementar el cuadro de diálogo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3bc71-109">Points to a [_ *DEVICEDIALOGDATA2*\*](-wia-devicedialogdata2.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bc71-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bc71-110">Return value</span></span>

<span data-ttu-id="3bc71-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3bc71-111">Type: **HRESULT**</span></span>

<span data-ttu-id="3bc71-112">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="3bc71-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="3bc71-113">Si el usuario cancela el cuadro de diálogo, el método devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="3bc71-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="3bc71-114">Si se produce un error en el método, devuelve un código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="3bc71-114">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="3bc71-115">En la tabla siguiente se muestran algunos de los códigos de estado devueltos posibles.</span><span class="sxs-lookup"><span data-stu-id="3bc71-115">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="3bc71-116">Código de error</span><span class="sxs-lookup"><span data-stu-id="3bc71-116">Error code</span></span>    | <span data-ttu-id="3bc71-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bc71-117">Description</span></span>                              |
|---------------|------------------------------------------|
| <span data-ttu-id="3bc71-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3bc71-118">E\_INVALIDARG</span></span> | <span data-ttu-id="3bc71-119">El parámetro pDeviceDialogData es **null**.</span><span class="sxs-lookup"><span data-stu-id="3bc71-119">Parameter pDeviceDialogData is **NULL**.</span></span> |
| <span data-ttu-id="3bc71-120">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3bc71-120">E\_NOTIMPL</span></span>    | <span data-ttu-id="3bc71-121">El método no está implementado.</span><span class="sxs-lookup"><span data-stu-id="3bc71-121">The method is not implemented.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="3bc71-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3bc71-122">Remarks</span></span>

<span data-ttu-id="3bc71-123">Si implementa la interfaz [**IWiaUIExtension2**](-wia-iwiauiextension2.md) y no desea reemplazar la interfaz de usuario del sistema, este método debe seguir implementado, pero no debe hacer nada más que devolver E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="3bc71-123">If you implement the [**IWiaUIExtension2**](-wia-iwiauiextension2.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bc71-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bc71-124">Requirements</span></span>



| <span data-ttu-id="3bc71-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bc71-125">Requirement</span></span> | <span data-ttu-id="3bc71-126">Value</span><span class="sxs-lookup"><span data-stu-id="3bc71-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc71-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bc71-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3bc71-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3bc71-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3bc71-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bc71-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3bc71-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3bc71-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3bc71-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3bc71-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bc71-132"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bc71-132"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




