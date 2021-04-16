---
description: Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: IWiaUIExtension::D método eviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 7d42d0c7f8cca510a9c8f78de7bf589f8e1d2d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541955"
---
# <a name="iwiauiextensiondevicedialog-method"></a><span data-ttu-id="d9e66-103">IWiaUIExtension::D método eviceDialog</span><span class="sxs-lookup"><span data-stu-id="d9e66-103">IWiaUIExtension::DeviceDialog method</span></span>

<span data-ttu-id="d9e66-104">Proporciona una interfaz de usuario personalizada que reemplaza la interfaz de usuario predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="d9e66-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e66-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9e66-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="d9e66-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9e66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9e66-107">*pDeviceDialogData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d9e66-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e66-108">Tipo: \**PDEVICEDIALOGDATA \** _</span><span class="sxs-lookup"><span data-stu-id="d9e66-108">Type: \**PDEVICEDIALOGDATA\** _</span></span>

<span data-ttu-id="d9e66-109">Apunta a una estructura [_ *DEVICEDIALOGDATA* \*](-wia-devicedialogdata.md) que contiene todos los datos necesarios para implementar el cuadro de diálogo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9e66-109">Points to a [_ *DEVICEDIALOGDATA*\*](-wia-devicedialogdata.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9e66-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9e66-110">Return value</span></span>

<span data-ttu-id="d9e66-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d9e66-111">Type: **HRESULT**</span></span>

<span data-ttu-id="d9e66-112">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="d9e66-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="d9e66-113">Si el usuario cancela el cuadro de diálogo, el método devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="d9e66-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="d9e66-114">Si no se implementa el método, devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="d9e66-114">If the method is not implemented, it returns E\_NOTIMPL.</span></span> <span data-ttu-id="d9e66-115">Si se produce un error en el método, devuelve un código de error COM estándar.</span><span class="sxs-lookup"><span data-stu-id="d9e66-115">If the method fails, it returns a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9e66-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9e66-116">Remarks</span></span>

<span data-ttu-id="d9e66-117">Si implementa la interfaz [**IWiaUIExtension**](-wia-iwiauiextension.md) y no desea reemplazar la interfaz de usuario del sistema, este método debe seguir implementado, pero no debe hacer nada más que devolver E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="d9e66-117">If you implement the [**IWiaUIExtension**](-wia-iwiauiextension.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9e66-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9e66-118">Requirements</span></span>



| <span data-ttu-id="d9e66-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9e66-119">Requirement</span></span> | <span data-ttu-id="d9e66-120">Value</span><span class="sxs-lookup"><span data-stu-id="d9e66-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d9e66-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9e66-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9e66-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d9e66-122">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d9e66-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9e66-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9e66-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9e66-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d9e66-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9e66-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9e66-126"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9e66-126"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




