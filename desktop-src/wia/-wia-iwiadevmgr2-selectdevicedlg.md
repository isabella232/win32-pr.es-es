---
description: Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'IWiaDevMgr2:: SelectDeviceDlg (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: cb41ec8e94782ee4d7408c53e2d4e098d986fe83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720536"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a><span data-ttu-id="90fb9-103">IWiaDevMgr2:: SelectDeviceDlg (método)</span><span class="sxs-lookup"><span data-stu-id="90fb9-103">IWiaDevMgr2::SelectDeviceDlg method</span></span>

<span data-ttu-id="90fb9-104">Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.</span><span class="sxs-lookup"><span data-stu-id="90fb9-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="90fb9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90fb9-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a><span data-ttu-id="90fb9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90fb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90fb9-107">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90fb9-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90fb9-108">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="90fb9-108">Type: **HWND**</span></span>

<span data-ttu-id="90fb9-109">Especifica la ventana primaria del cuadro de diálogo **seleccionar dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="90fb9-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="90fb9-110">*lDeviceType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90fb9-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90fb9-111">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="90fb9-111">Type: **LONG**</span></span>

<span data-ttu-id="90fb9-112">Especifica el tipo de dispositivo WIA 2,0 que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="90fb9-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="90fb9-113">Vea [especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md) para obtener una lista de valores posibles.</span><span class="sxs-lookup"><span data-stu-id="90fb9-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="90fb9-114">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90fb9-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90fb9-115">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="90fb9-115">Type: **LONG**</span></span>

<span data-ttu-id="90fb9-116">Especifica el comportamiento del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="90fb9-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="90fb9-117">El valor puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="90fb9-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="90fb9-118"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="90fb9-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="90fb9-119">Usa el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="90fb9-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="90fb9-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ seleccionar \_ dispositivo \_ predeterminado**</span><span class="sxs-lookup"><span data-stu-id="90fb9-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="90fb9-121">Mostrar el cuadro de diálogo aunque solo haya un dispositivo coincidente.</span><span class="sxs-lookup"><span data-stu-id="90fb9-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="90fb9-122">*pbstrDeviceID* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="90fb9-122">*pbstrDeviceID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="90fb9-123">Tipo: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="90fb9-123">Type: \**BSTR\** _</span></span>

<span data-ttu-id="90fb9-124">En la salida, recibe una cadena que contiene la cadena de identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90fb9-124">On output, receives a string which contains the device's identifier string.</span></span> <span data-ttu-id="90fb9-125">En la entrada, pase la dirección de un puntero si esta información es necesaria o _ *null*\* si no es necesario.</span><span class="sxs-lookup"><span data-stu-id="90fb9-125">On input, pass the address of a pointer if this information is needed, or _ *NULL*\* if it is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="90fb9-126">*ppItemRoot* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="90fb9-126">*ppItemRoot* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="90fb9-127">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="90fb9-127">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="90fb9-128">Recibe la dirección de un puntero a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento raíz del árbol jerárquico que representa el dispositivo WIA 2,0 seleccionado.</span><span class="sxs-lookup"><span data-stu-id="90fb9-128">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item of the hierarchical tree that represents the selected WIA 2.0 device.</span></span> <span data-ttu-id="90fb9-129">Si no se encuentra ningún dispositivo, recibe un **valor null**.</span><span class="sxs-lookup"><span data-stu-id="90fb9-129">If no device is found, it receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90fb9-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90fb9-130">Return value</span></span>

<span data-ttu-id="90fb9-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="90fb9-131">Type: **HRESULT**</span></span>

<span data-ttu-id="90fb9-132">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="90fb9-132">This method can return one of these values.</span></span>



| <span data-ttu-id="90fb9-133">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="90fb9-133">Return code</span></span>                                                                                                  | <span data-ttu-id="90fb9-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="90fb9-134">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90fb9-135"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="90fb9-135"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="90fb9-136">El dispositivo se seleccionó correctamente.</span><span class="sxs-lookup"><span data-stu-id="90fb9-136">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="90fb9-137"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="90fb9-137"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="90fb9-138">El usuario canceló el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="90fb9-138">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="90fb9-139"><dt>**WIA \_ S \_ no hay ningún \_ dispositivo \_ disponible**</dt></span><span class="sxs-lookup"><span data-stu-id="90fb9-139"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="90fb9-140">Ningún dispositivo de hardware WIA 2,0 coincide con las especificaciones proporcionadas en el parámetro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="90fb9-140">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="90fb9-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90fb9-141">Remarks</span></span>

<span data-ttu-id="90fb9-142">Este método crea y muestra el cuadro de diálogo **seleccionar dispositivo** para que el usuario pueda seleccionar un dispositivo WIA 2,0 para la adquisición de imágenes.</span><span class="sxs-lookup"><span data-stu-id="90fb9-142">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="90fb9-143">Si un dispositivo se selecciona correctamente, el método **IWiaDevMgr2:: SelectDeviceDlg** crea un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90fb9-143">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlg** method creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for the device.</span></span> <span data-ttu-id="90fb9-144">Almacena un puntero a la interfaz **IWiaItem2** del elemento raíz en el parámetro *ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="90fb9-144">It stores a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span>

<span data-ttu-id="90fb9-145">La aplicación puede restringir los dispositivos que se muestran al usuario a determinados tipos especificando los tipos de dispositivo mediante el parámetro *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="90fb9-145">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="90fb9-146">Si solo un dispositivo cumple la especificación, **IWiaDevMgr2:: SelectDeviceDlg** no muestra el cuadro de diálogo **seleccionar dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="90fb9-146">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlg** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="90fb9-147">En su lugar, crea el árbol [**IWiaItem2**](-wia-iwiaitem2.md) para el dispositivo y almacena un puntero a la interfaz **IWiaItem2** del elemento raíz en el parámetro *ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="90fb9-147">Instead it creates the [**IWiaItem2**](-wia-iwiaitem2.md) tree for the device and store a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span> <span data-ttu-id="90fb9-148">Puede invalidar este comportamiento y forzar **IWiaDevMgr2:: SelectDeviceDlg** para mostrar el cuadro de diálogo especificando \_ WIA \_ seleccionar \_ dispositivo nodefault como valor del parámetro *lFlags* .</span><span class="sxs-lookup"><span data-stu-id="90fb9-148">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlg** to display the dialog box by specifying WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="90fb9-149">Si más de un dispositivo WIA 2,0 coincide con la especificación, todos los dispositivos coincidentes se muestran en el cuadro de diálogo **seleccionar dispositivo** para que el usuario pueda elegir uno.</span><span class="sxs-lookup"><span data-stu-id="90fb9-149">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the **Select Device** dialog box so the user may choose one.</span></span>

<span data-ttu-id="90fb9-150">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppItemRoot* .</span><span class="sxs-lookup"><span data-stu-id="90fb9-150">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppItemRoot* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="90fb9-151">Se recomienda que las aplicaciones hagan que la selección de dispositivos y imágenes esté disponible a través de un elemento de menú denominado **desde el escáner** en el menú **archivo** .</span><span class="sxs-lookup"><span data-stu-id="90fb9-151">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="90fb9-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90fb9-152">Requirements</span></span>



| <span data-ttu-id="90fb9-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="90fb9-153">Requirement</span></span> | <span data-ttu-id="90fb9-154">Value</span><span class="sxs-lookup"><span data-stu-id="90fb9-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90fb9-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90fb9-155">Minimum supported client</span></span><br/> | <span data-ttu-id="90fb9-156">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="90fb9-156">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="90fb9-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90fb9-157">Minimum supported server</span></span><br/> | <span data-ttu-id="90fb9-158">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="90fb9-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="90fb9-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90fb9-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="90fb9-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="90fb9-160"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="90fb9-161">IDL</span><span class="sxs-lookup"><span data-stu-id="90fb9-161">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90fb9-162"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90fb9-162"><dt>Wia.idl</dt></span></span> </dl> |



 

 
