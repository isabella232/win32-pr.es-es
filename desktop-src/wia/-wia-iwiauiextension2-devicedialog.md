---
description: 'Método IWiaUIExtension2::D eviceDialog: proporciona una interfaz de usuario personalizada que reemplaza a la interfaz de usuario predeterminada del sistema.'
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: Método IWiaUIExtension2::D eviceDialog (Wiadevd.h)
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
ms.openlocfilehash: 94e717184c936ae85ba1cf345a13b44f9bbdce4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116653"
---
# <a name="iwiauiextension2devicedialog-method"></a><span data-ttu-id="43e08-103">IWiaUIExtension2::D eviceDialog (método)</span><span class="sxs-lookup"><span data-stu-id="43e08-103">IWiaUIExtension2::DeviceDialog method</span></span>

<span data-ttu-id="43e08-104">Proporciona una interfaz de usuario personalizada que reemplaza a la interfaz de usuario predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="43e08-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e08-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43e08-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="43e08-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43e08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43e08-107">*pDeviceDialogData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="43e08-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e08-108">Tipo: **PDEVICEDIALOGDATA2 \***</span><span class="sxs-lookup"><span data-stu-id="43e08-108">Type: **PDEVICEDIALOGDATA2\***</span></span>

<span data-ttu-id="43e08-109">Apunta a una [**estructura DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) que contiene todos los datos necesarios para implementar el cuadro de diálogo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43e08-109">Points to a [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43e08-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43e08-110">Return value</span></span>

<span data-ttu-id="43e08-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="43e08-111">Type: **HRESULT**</span></span>

<span data-ttu-id="43e08-112">Si el método se realiza correctamente, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43e08-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="43e08-113">Si el usuario cancela el cuadro de diálogo, el método devuelve S \_ FALSE.</span><span class="sxs-lookup"><span data-stu-id="43e08-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="43e08-114">Si se produce un error en el método, devuelve un código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="43e08-114">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="43e08-115">En la tabla siguiente se muestran algunos de los posibles códigos de estado de devolución.</span><span class="sxs-lookup"><span data-stu-id="43e08-115">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="43e08-116">Código de error</span><span class="sxs-lookup"><span data-stu-id="43e08-116">Error code</span></span>    | <span data-ttu-id="43e08-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="43e08-117">Description</span></span>                              |
|---------------|------------------------------------------|
| <span data-ttu-id="43e08-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="43e08-118">E\_INVALIDARG</span></span> | <span data-ttu-id="43e08-119">El parámetro pDeviceDialogData es **NULL.**</span><span class="sxs-lookup"><span data-stu-id="43e08-119">Parameter pDeviceDialogData is **NULL**.</span></span> |
| <span data-ttu-id="43e08-120">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="43e08-120">E\_NOTIMPL</span></span>    | <span data-ttu-id="43e08-121">El método no está implementado.</span><span class="sxs-lookup"><span data-stu-id="43e08-121">The method is not implemented.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="43e08-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43e08-122">Remarks</span></span>

<span data-ttu-id="43e08-123">Si implementa la interfaz [**IWiaUIExtension2**](-wia-iwiauiextension2.md) y no desea reemplazar la interfaz de usuario del sistema, este método todavía debe implementarse, pero no debe hacer nada más que devolver E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="43e08-123">If you implement the [**IWiaUIExtension2**](-wia-iwiauiextension2.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e08-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43e08-124">Requirements</span></span>



| <span data-ttu-id="43e08-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e08-125">Requirement</span></span> | <span data-ttu-id="43e08-126">Valor</span><span class="sxs-lookup"><span data-stu-id="43e08-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="43e08-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43e08-127">Minimum supported client</span></span><br/> | <span data-ttu-id="43e08-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="43e08-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="43e08-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43e08-129">Minimum supported server</span></span><br/> | <span data-ttu-id="43e08-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="43e08-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="43e08-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43e08-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="43e08-132"><dt>Wiadevd.h</dt></span><span class="sxs-lookup"><span data-stu-id="43e08-132"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




