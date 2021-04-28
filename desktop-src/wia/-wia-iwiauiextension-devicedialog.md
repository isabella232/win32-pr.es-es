---
description: 'Método IWiaUIExtension::D eviceDialog: proporciona una interfaz de usuario personalizada que reemplaza a la interfaz de usuario predeterminada del sistema.'
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: IWiaUIExtension::D eviceDialog (Wiadevd.h)
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
ms.openlocfilehash: d467769308707032b8e92b4ac7877488991356dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116713"
---
# <a name="iwiauiextensiondevicedialog-method"></a><span data-ttu-id="48341-103">IWiaUIExtension::D eviceDialog (método)</span><span class="sxs-lookup"><span data-stu-id="48341-103">IWiaUIExtension::DeviceDialog method</span></span>

<span data-ttu-id="48341-104">Proporciona una interfaz de usuario personalizada que reemplaza a la interfaz de usuario predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="48341-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="48341-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48341-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="48341-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48341-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48341-107">*pDeviceDialogData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="48341-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48341-108">Tipo: **PDEVICEDIALOGDATA \***</span><span class="sxs-lookup"><span data-stu-id="48341-108">Type: **PDEVICEDIALOGDATA\***</span></span>

<span data-ttu-id="48341-109">Apunta a una [**estructura DEVICEDIALOGDATA**](-wia-devicedialogdata.md) que contiene todos los datos necesarios para implementar el cuadro de diálogo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="48341-109">Points to a [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48341-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48341-110">Return value</span></span>

<span data-ttu-id="48341-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="48341-111">Type: **HRESULT**</span></span>

<span data-ttu-id="48341-112">Si el método se realiza correctamente, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="48341-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="48341-113">Si el usuario cancela el cuadro de diálogo, el método devuelve S \_ FALSE.</span><span class="sxs-lookup"><span data-stu-id="48341-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="48341-114">Si el método no se implementa, devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="48341-114">If the method is not implemented, it returns E\_NOTIMPL.</span></span> <span data-ttu-id="48341-115">Si se produce un error en el método, devuelve un código de error COM estándar.</span><span class="sxs-lookup"><span data-stu-id="48341-115">If the method fails, it returns a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="48341-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48341-116">Remarks</span></span>

<span data-ttu-id="48341-117">Si implementa la interfaz [**IWiaUIExtension**](-wia-iwiauiextension.md) y no desea reemplazar la interfaz de usuario del sistema, este método todavía debe implementarse, pero no debe hacer nada más que devolver E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="48341-117">If you implement the [**IWiaUIExtension**](-wia-iwiauiextension.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="48341-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48341-118">Requirements</span></span>



| <span data-ttu-id="48341-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="48341-119">Requirement</span></span> | <span data-ttu-id="48341-120">Valor</span><span class="sxs-lookup"><span data-stu-id="48341-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="48341-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48341-121">Minimum supported client</span></span><br/> | <span data-ttu-id="48341-122">Solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="48341-122">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="48341-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48341-123">Minimum supported server</span></span><br/> | <span data-ttu-id="48341-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="48341-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="48341-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48341-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="48341-126"><dt>Wiadevd.h</dt></span><span class="sxs-lookup"><span data-stu-id="48341-126"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




