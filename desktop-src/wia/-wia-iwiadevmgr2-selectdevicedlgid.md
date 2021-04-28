---
description: 'Método IWiaDevMgr2::SelectDeviceDlgID: muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.'
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: Método IWiaDevMgr2::SelectDeviceDlgID (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a4279bef86d761ed0eb7d90ad3b8dee46e0f17f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106823"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a><span data-ttu-id="2a758-103">Método IWiaDevMgr2::SelectDeviceDlgID</span><span class="sxs-lookup"><span data-stu-id="2a758-103">IWiaDevMgr2::SelectDeviceDlgID method</span></span>

<span data-ttu-id="2a758-104">Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.</span><span class="sxs-lookup"><span data-stu-id="2a758-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a758-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a758-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="2a758-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a758-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a758-107">*hwndParent* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2a758-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a758-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="2a758-108">Type: **HWND**</span></span>

<span data-ttu-id="2a758-109">Especifica la ventana primaria del cuadro **de diálogo Seleccionar** dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a758-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="2a758-110">*lDeviceType* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2a758-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a758-111">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="2a758-111">Type: **LONG**</span></span>

<span data-ttu-id="2a758-112">Especifica qué tipo de dispositivo WIA 2.0 se va a usar.</span><span class="sxs-lookup"><span data-stu-id="2a758-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="2a758-113">Consulte [Especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md) para obtener una lista de valores posibles.</span><span class="sxs-lookup"><span data-stu-id="2a758-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="2a758-114">*lFlags* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2a758-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a758-115">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="2a758-115">Type: **LONG**</span></span>

<span data-ttu-id="2a758-116">Especifica el comportamiento del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2a758-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="2a758-117">El valor puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="2a758-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="2a758-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="2a758-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="2a758-119">Usa el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2a758-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="2a758-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ DEVICE \_ NODEFAULT**</span><span class="sxs-lookup"><span data-stu-id="2a758-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="2a758-121">Muestra el cuadro de diálogo aunque solo haya un dispositivo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2a758-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2a758-122">*pbstrDeviceID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2a758-122">*pbstrDeviceID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2a758-123">Tipo: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="2a758-123">Type: **BSTR\***</span></span>

<span data-ttu-id="2a758-124">Puntero a una cadena que recibe la cadena de identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a758-124">Pointer to a string that receives the identifier string of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a758-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a758-125">Return value</span></span>

<span data-ttu-id="2a758-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2a758-126">Type: **HRESULT**</span></span>

<span data-ttu-id="2a758-127">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2a758-127">This method can return one of these values.</span></span>



| <span data-ttu-id="2a758-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2a758-128">Return code</span></span>                                                                                                  | <span data-ttu-id="2a758-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a758-129">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a758-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2a758-130"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="2a758-131">El dispositivo se seleccionó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2a758-131">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="2a758-132"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="2a758-132"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="2a758-133">El usuario canceló el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2a758-133">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="2a758-134"><dt>**WIA \_ S NO HAY DISPOSITIVO \_ \_ \_ DISPONIBLE**</dt></span><span class="sxs-lookup"><span data-stu-id="2a758-134"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="2a758-135">Ningún dispositivo de hardware WIA 2.0 coincide con las especificaciones indicadas en *el parámetro lDeviceType.*</span><span class="sxs-lookup"><span data-stu-id="2a758-135">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="2a758-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a758-136">Remarks</span></span>

<span data-ttu-id="2a758-137">Este método crea y muestra el cuadro **de** diálogo Seleccionar dispositivo para que el usuario pueda seleccionar un dispositivo WIA 2.0 para la adquisición de imágenes.</span><span class="sxs-lookup"><span data-stu-id="2a758-137">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="2a758-138">Si un dispositivo se selecciona correctamente, el método **IWiaDevMgr2::SelectDeviceDlgID** pasa su cadena de identificador a la aplicación a través de su *parámetro pbstrDeviceID.*</span><span class="sxs-lookup"><span data-stu-id="2a758-138">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlgID** method passes its identifier string to the application through its *pbstrDeviceID* parameter.</span></span>

<span data-ttu-id="2a758-139">La aplicación puede restringir los dispositivos que se muestran al usuario a tipos concretos especificando los tipos de dispositivo mediante el *parámetro lDeviceType.*</span><span class="sxs-lookup"><span data-stu-id="2a758-139">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="2a758-140">Si solo un dispositivo cumple la especificación, **IWiaDevMgr2::SelectDeviceDlgID** no muestra el **cuadro de diálogo** Seleccionar dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a758-140">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlgID** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="2a758-141">En su lugar, pasa la cadena de identificador del dispositivo a la aplicación sin mostrar el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2a758-141">Instead it passes the device's identifier string to the application without displaying the dialog box.</span></span> <span data-ttu-id="2a758-142">Puede invalidar este comportamiento y forzar que **IWiaDevMgr2::SelectDeviceDlgID** muestre el cuadro de diálogo pasando WIA SELECT DEVICE NODEFAULT como valor para el parámetro \_ \_ \_ *lFlags.*</span><span class="sxs-lookup"><span data-stu-id="2a758-142">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlgID** to display the dialog box by passing WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="2a758-143">Si más de un dispositivo WIA 2.0 coincide con la especificación, todos los dispositivos correspondientes se muestran en el cuadro de diálogo Seleccionardispositivo para que el usuario pueda elegir uno.</span><span class="sxs-lookup"><span data-stu-id="2a758-143">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the SelectDevice dialog box so the user may choose one.</span></span>

> [!Note]  
> <span data-ttu-id="2a758-144">Se recomienda que las aplicaciones hagan que la selección de dispositivos e imágenes esté disponible a través de un elemento de menú denominado **Desde escáner** en **el menú** Archivo.</span><span class="sxs-lookup"><span data-stu-id="2a758-144">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2a758-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a758-145">Requirements</span></span>



| <span data-ttu-id="2a758-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a758-146">Requirement</span></span> | <span data-ttu-id="2a758-147">Valor</span><span class="sxs-lookup"><span data-stu-id="2a758-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a758-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a758-148">Minimum supported client</span></span><br/> | <span data-ttu-id="2a758-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2a758-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2a758-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a758-150">Minimum supported server</span></span><br/> | <span data-ttu-id="2a758-151">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a758-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2a758-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a758-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a758-153"><dt>Wia.h</dt></span><span class="sxs-lookup"><span data-stu-id="2a758-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a758-154">Idl</span><span class="sxs-lookup"><span data-stu-id="2a758-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a758-155"><dt>Wia.idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a758-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 




