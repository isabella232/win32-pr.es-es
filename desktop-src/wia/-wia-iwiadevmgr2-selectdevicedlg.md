---
description: 'Método IWiaDevMgr2::SelectDeviceDlg: muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.'
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: Método IWiaDevMgr2::SelectDeviceDlg (Wia.h)
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
ms.openlocfilehash: 60ec24f264b8fe0424f17fc32deaf803e55c3346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091263"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a><span data-ttu-id="f68e2-103">Método IWiaDevMgr2::SelectDeviceDlg</span><span class="sxs-lookup"><span data-stu-id="f68e2-103">IWiaDevMgr2::SelectDeviceDlg method</span></span>

<span data-ttu-id="f68e2-104">Muestra un cuadro de diálogo que permite al usuario seleccionar un dispositivo de hardware para la adquisición de imágenes.</span><span class="sxs-lookup"><span data-stu-id="f68e2-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f68e2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f68e2-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a><span data-ttu-id="f68e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f68e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f68e2-107">*hwndParent* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f68e2-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f68e2-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="f68e2-108">Type: **HWND**</span></span>

<span data-ttu-id="f68e2-109">Especifica la ventana primaria del cuadro **de diálogo Seleccionar** dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f68e2-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="f68e2-110">*lDeviceType* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f68e2-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f68e2-111">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="f68e2-111">Type: **LONG**</span></span>

<span data-ttu-id="f68e2-112">Especifica qué tipo de dispositivo WIA 2.0 se va a usar.</span><span class="sxs-lookup"><span data-stu-id="f68e2-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="f68e2-113">Consulte [Especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md) para obtener una lista de valores posibles.</span><span class="sxs-lookup"><span data-stu-id="f68e2-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="f68e2-114">*lFlags* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f68e2-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f68e2-115">Tipo: **LONG**</span><span class="sxs-lookup"><span data-stu-id="f68e2-115">Type: **LONG**</span></span>

<span data-ttu-id="f68e2-116">Especifica el comportamiento del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f68e2-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="f68e2-117">El valor puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="f68e2-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="f68e2-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="f68e2-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="f68e2-119">Usa el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f68e2-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="f68e2-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ DEVICE \_ NODEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f68e2-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="f68e2-121">Muestra el cuadro de diálogo aunque solo haya un dispositivo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f68e2-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f68e2-122">*pbstrDeviceID* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f68e2-122">*pbstrDeviceID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f68e2-123">Tipo: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="f68e2-123">Type: **BSTR\***</span></span>

<span data-ttu-id="f68e2-124">En la salida, recibe una cadena que contiene la cadena de identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f68e2-124">On output, receives a string which contains the device's identifier string.</span></span> <span data-ttu-id="f68e2-125">En la entrada, pase la dirección de un puntero si se necesita esta información o **NULL** si no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="f68e2-125">On input, pass the address of a pointer if this information is needed, or **NULL** if it is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="f68e2-126">*ppItemRoot* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f68e2-126">*ppItemRoot* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f68e2-127">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f68e2-127">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="f68e2-128">Recibe la dirección de un puntero a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento raíz del árbol jerárquico que representa el dispositivo WIA 2.0 seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f68e2-128">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item of the hierarchical tree that represents the selected WIA 2.0 device.</span></span> <span data-ttu-id="f68e2-129">Si no se encuentra ningún dispositivo, recibe **NULL.**</span><span class="sxs-lookup"><span data-stu-id="f68e2-129">If no device is found, it receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f68e2-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f68e2-130">Return value</span></span>

<span data-ttu-id="f68e2-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f68e2-131">Type: **HRESULT**</span></span>

<span data-ttu-id="f68e2-132">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f68e2-132">This method can return one of these values.</span></span>



| <span data-ttu-id="f68e2-133">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f68e2-133">Return code</span></span>                                                                                                  | <span data-ttu-id="f68e2-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="f68e2-134">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f68e2-135"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f68e2-135"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="f68e2-136">El dispositivo se seleccionó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f68e2-136">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="f68e2-137"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="f68e2-137"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="f68e2-138">El usuario canceló el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f68e2-138">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="f68e2-139"><dt>**WIA \_ S NO HAY DISPOSITIVO \_ \_ \_ DISPONIBLE**</dt></span><span class="sxs-lookup"><span data-stu-id="f68e2-139"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="f68e2-140">Ningún dispositivo de hardware WIA 2.0 coincide con las especificaciones indicadas en *el parámetro lDeviceType.*</span><span class="sxs-lookup"><span data-stu-id="f68e2-140">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f68e2-141">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f68e2-141">Remarks</span></span>

<span data-ttu-id="f68e2-142">Este método crea y muestra el cuadro **de** diálogo Seleccionar dispositivo para que el usuario pueda seleccionar un dispositivo WIA 2.0 para la adquisición de imágenes.</span><span class="sxs-lookup"><span data-stu-id="f68e2-142">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="f68e2-143">Si un dispositivo se selecciona correctamente, el método **IWiaDevMgr2::SelectDeviceDlg** crea un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f68e2-143">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlg** method creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for the device.</span></span> <span data-ttu-id="f68e2-144">Almacena un puntero a la **interfaz IWiaItem2** del elemento raíz en el parámetro *ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="f68e2-144">It stores a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span>

<span data-ttu-id="f68e2-145">La aplicación puede restringir los dispositivos que se muestran al usuario a tipos concretos especificando los tipos de dispositivo mediante el *parámetro lDeviceType.*</span><span class="sxs-lookup"><span data-stu-id="f68e2-145">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="f68e2-146">Si solo un dispositivo cumple la especificación, **IWiaDevMgr2::SelectDeviceDlg** no muestra el **cuadro de diálogo** Seleccionar dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f68e2-146">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlg** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="f68e2-147">En su lugar, crea el árbol [**IWiaItem2**](-wia-iwiaitem2.md) para el dispositivo y almacena un puntero a la interfaz **IWiaItem2** del elemento raíz en el *parámetro ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="f68e2-147">Instead it creates the [**IWiaItem2**](-wia-iwiaitem2.md) tree for the device and store a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span> <span data-ttu-id="f68e2-148">Puede invalidar este comportamiento y forzar a **IWiaDevMgr2::SelectDeviceDlg** a mostrar el cuadro de diálogo especificando WIA SELECT DEVICE NODEFAULT como valor para el parámetro \_ \_ \_ *lFlags.*</span><span class="sxs-lookup"><span data-stu-id="f68e2-148">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlg** to display the dialog box by specifying WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="f68e2-149">Si más de un dispositivo WIA 2.0 coincide con la  especificación, todos los dispositivos correspondientes se muestran en el cuadro de diálogo Seleccionar dispositivo para que el usuario pueda elegir uno.</span><span class="sxs-lookup"><span data-stu-id="f68e2-149">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the **Select Device** dialog box so the user may choose one.</span></span>

<span data-ttu-id="f68e2-150">Las aplicaciones deben llamar [al método IUnknown::Release en](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) los punteros de interfaz que reciben a través del parámetro *ppItemRoot.*</span><span class="sxs-lookup"><span data-stu-id="f68e2-150">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppItemRoot* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="f68e2-151">Se recomienda que las aplicaciones hagan que la selección de dispositivos e imágenes esté disponible a través de un elemento de menú denominado **Desde escáner** en el **menú** Archivo.</span><span class="sxs-lookup"><span data-stu-id="f68e2-151">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f68e2-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f68e2-152">Requirements</span></span>



| <span data-ttu-id="f68e2-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="f68e2-153">Requirement</span></span> | <span data-ttu-id="f68e2-154">Valor</span><span class="sxs-lookup"><span data-stu-id="f68e2-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f68e2-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f68e2-155">Minimum supported client</span></span><br/> | <span data-ttu-id="f68e2-156">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="f68e2-156">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f68e2-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f68e2-157">Minimum supported server</span></span><br/> | <span data-ttu-id="f68e2-158">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f68e2-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f68e2-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f68e2-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="f68e2-160"><dt>Wia.h</dt></span><span class="sxs-lookup"><span data-stu-id="f68e2-160"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="f68e2-161">Idl</span><span class="sxs-lookup"><span data-stu-id="f68e2-161">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f68e2-162"><dt>Wia.idl</dt></span><span class="sxs-lookup"><span data-stu-id="f68e2-162"><dt>Wia.idl</dt></span></span> </dl> |



 

 
