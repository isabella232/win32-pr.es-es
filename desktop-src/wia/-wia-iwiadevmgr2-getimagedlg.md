---
description: 'El método IWiaDevMgr2:: GetImageDlg muestra uno o varios cuadros de diálogo que permiten a un usuario adquirir una imagen de un dispositivo de adquisición de imágenes de Windows (WIA) 2,0 y escribir la imagen en un archivo especificado.'
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'IWiaDevMgr2:: GetImageDlg (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720537"
---
# <a name="iwiadevmgr2getimagedlg-method"></a><span data-ttu-id="b0545-103">IWiaDevMgr2:: GetImageDlg (método)</span><span class="sxs-lookup"><span data-stu-id="b0545-103">IWiaDevMgr2::GetImageDlg method</span></span>

<span data-ttu-id="b0545-104">El método **IWiaDevMgr2:: GetImageDlg** muestra uno o varios cuadros de diálogo que permiten a un usuario adquirir una imagen de un dispositivo de adquisición de imágenes de Windows (WIA) 2,0 y escribir la imagen en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b0545-104">The **IWiaDevMgr2::GetImageDlg** method displays one or more dialog boxes that enable a user to acquire an image from a Windows Image Acquisition (WIA) 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="b0545-105">Este método extiende la funcionalidad de [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) para encapsular la adquisición de imágenes en una única llamada API.</span><span class="sxs-lookup"><span data-stu-id="b0545-105">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0545-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0545-106">Syntax</span></span>


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a><span data-ttu-id="b0545-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0545-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0545-108">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0545-108">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0545-109">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="b0545-109">Type: **LONG**</span></span>

<span data-ttu-id="b0545-110">Especifica el comportamiento del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b0545-110">Specifies dialog box behavior.</span></span> <span data-ttu-id="b0545-111">Se puede establecer en los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="b0545-111">Can be set to the following values:</span></span>



| <span data-ttu-id="b0545-112">Marca</span><span class="sxs-lookup"><span data-stu-id="b0545-112">Flag</span></span>                                 | <span data-ttu-id="b0545-113">Significado</span><span class="sxs-lookup"><span data-stu-id="b0545-113">Meaning</span></span>                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0545-114">0</span><span class="sxs-lookup"><span data-stu-id="b0545-114">0</span></span>                                    | <span data-ttu-id="b0545-115">Comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b0545-115">Default behavior.</span></span>                                                                                                                                                           |
| <span data-ttu-id="b0545-116">cuadro de diálogo de dispositivo WIA uso de la \_ \_ interfaz de \_ \_ \_ usuario común</span><span class="sxs-lookup"><span data-stu-id="b0545-116">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="b0545-117">Use la interfaz de usuario del sistema en lugar de la interfaz de usuario proporcionada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="b0545-117">Use the system UI instead of the vendor-supplied UI.</span></span> <span data-ttu-id="b0545-118">Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b0545-118">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="b0545-119">Si no hay ninguna interfaz de usuario disponible, la función devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="b0545-119">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b0545-120">*bstrDeviceID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0545-120">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0545-121">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b0545-121">Type: **BSTR**</span></span>

<span data-ttu-id="b0545-122">Especifica el escáner que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b0545-122">Specifies the scanner to use.</span></span>

</dd> <dt>

<span data-ttu-id="b0545-123">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0545-123">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0545-124">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="b0545-124">Type: **HWND**</span></span>

<span data-ttu-id="b0545-125">Identificador de la ventana que posee el cuadro de diálogo **obtener imagen** .</span><span class="sxs-lookup"><span data-stu-id="b0545-125">A handle of the window that owns the **Get Image** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b0545-126">*bstrFolderName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0545-126">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0545-127">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b0545-127">Type: **BSTR**</span></span>

<span data-ttu-id="b0545-128">Especifica el nombre de la carpeta Ito almacena los archivos digitalizados en.</span><span class="sxs-lookup"><span data-stu-id="b0545-128">Specifies the name of the folder ito store the scanned files in.</span></span>

</dd> <dt>

<span data-ttu-id="b0545-129">*bstrFilename* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0545-129">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0545-130">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="b0545-130">Type: **BSTR**</span></span>

<span data-ttu-id="b0545-131">Especifica el nombre del archivo en el que se van a escribir los datos de la imagen.</span><span class="sxs-lookup"><span data-stu-id="b0545-131">Specifies the name of the file to write the image data to.</span></span>

</dd> <dt>

<span data-ttu-id="b0545-132">*plNumFiles* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0545-132">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0545-133">Tipo: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="b0545-133">Type: \**LONG\** _</span></span>

<span data-ttu-id="b0545-134">Puntero al número de archivos que se van a examinar.</span><span class="sxs-lookup"><span data-stu-id="b0545-134">A pointer to the number of files to scan.</span></span>

</dd> <dt>

<span data-ttu-id="b0545-135">_ppbstrFilePaths \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="b0545-135">_ppbstrFilePaths\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0545-136">Tipo: **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="b0545-136">Type: **BSTR\*\***</span></span>

<span data-ttu-id="b0545-137">Dirección de un puntero a una matriz de rutas de acceso de los archivos digitalizados.</span><span class="sxs-lookup"><span data-stu-id="b0545-137">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="b0545-138">Inicialice el puntero para que apunte a una matriz de tamaño cero (0) antes de que se llame a **IWiaDevMgr2:: GetImageDlg** .</span><span class="sxs-lookup"><span data-stu-id="b0545-138">Initialize the pointer to point to an array of size zero (0) before **IWiaDevMgr2::GetImageDlg** is called.</span></span> <span data-ttu-id="b0545-139">Vea **Comentarios**.</span><span class="sxs-lookup"><span data-stu-id="b0545-139">See **Remarks**.</span></span>

</dd> <dt>

<span data-ttu-id="b0545-140">*ppItem* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b0545-140">*ppItem* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0545-141">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b0545-141">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="b0545-142">Dirección de un puntero al [**IWiaItem2**](-wia-iwiaitem2.md) desde el que se analizaron las imágenes.</span><span class="sxs-lookup"><span data-stu-id="b0545-142">The address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) that the images were scanned from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0545-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0545-143">Return value</span></span>

<span data-ttu-id="b0545-144">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b0545-144">Type: **HRESULT**</span></span>

<span data-ttu-id="b0545-145">**IWiaDevMgr2:: GetImageDlg** devuelve s \_ OK si los datos se transfieren correctamente, devuelve s \_ false si el usuario cancela el cuadro de diálogo o devuelve un error com estándar.</span><span class="sxs-lookup"><span data-stu-id="b0545-145">**IWiaDevMgr2::GetImageDlg** returns S\_OK if the data is transferred successfully, returns S\_FALSE if the user cancels the dialog box, or returns a standard COM error.</span></span>

> [!Note]  
> <span data-ttu-id="b0545-146">El parámetro *ppbstrFilePaths* no está necesariamente vacío, si la función devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="b0545-146">The *ppbstrFilePaths* parameter is not necessarily empty, if the function returns S\_FALSE.</span></span> <span data-ttu-id="b0545-147">Si el usuario cancela, las páginas que han completado el examen se procesan y se devuelven en *ppbstrFilePaths*.</span><span class="sxs-lookup"><span data-stu-id="b0545-147">If the user cancels, the pages that have completed scanning are processed and returned in *ppbstrFilePaths*.</span></span> <span data-ttu-id="b0545-148">Incluso si no se usan, debe liberar la matriz.</span><span class="sxs-lookup"><span data-stu-id="b0545-148">Even if they are not used, you must free the array.</span></span> <span data-ttu-id="b0545-149">Vea **Comentarios**.</span><span class="sxs-lookup"><span data-stu-id="b0545-149">See **Remarks**.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="b0545-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0545-150">Remarks</span></span>

<span data-ttu-id="b0545-151">Si la aplicación pasa **null** para el valor del parámetro *bstrDeviceID* , **IWiaDevMgr2:: GetImageDlg** muestra el cuadro de diálogo **seleccionar dispositivo** para que el usuario pueda seleccionar el dispositivo de entrada WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="b0545-151">If the application passes **NULL** for the value of the *bstrDeviceID* parameter, **IWiaDevMgr2::GetImageDlg** displays the **Select Device** dialog box so that the user can select the WIA 2.0 input device.</span></span>

<span data-ttu-id="b0545-152">Use un elemento de menú denominado **desde el escáner** en el menú **archivo** para que las selecciones de dispositivo e imagen estén disponibles en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b0545-152">Use a menu item named **From scanner** on the **File** menu so that device and image selections are available in your application.</span></span>

<span data-ttu-id="b0545-153">Llame a [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) en cada BSTR de la matriz a la que apunta *ppbstrFilePaths* \[ \] , y llame a [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) en la matriz para liberar memoria asociada.</span><span class="sxs-lookup"><span data-stu-id="b0545-153">Call [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) on each BSTR in the array that *ppbstrFilePaths*\[i\] points to, and call [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) on the array itself to free associated memory.</span></span> <span data-ttu-id="b0545-154">Si \_ se devuelve S false, compruebe si el valor al que apunta *plNumFiles* no es cero.</span><span class="sxs-lookup"><span data-stu-id="b0545-154">If S\_FALSE is returned, check to see if the value that *plNumFiles* points to is not zero.</span></span> <span data-ttu-id="b0545-155">Si el valor no es cero, libere los  \[ \] recursos de ppbstrFilePaths i en la aplicación, ya que el usuario puede cancelar después de examinar una o más páginas.</span><span class="sxs-lookup"><span data-stu-id="b0545-155">If the value is not zero, free the *ppbstrFilePaths*\[i\] resources in the application, because the user might cancel after scanning one or more pages.</span></span> <span data-ttu-id="b0545-156">Inicialice *plNumFiles* en cero antes de llamar a **IWiaDevMgr2:: GetImageDlg**.</span><span class="sxs-lookup"><span data-stu-id="b0545-156">Initialize *plNumFiles* to zero before you call **IWiaDevMgr2::GetImageDlg**.</span></span> <span data-ttu-id="b0545-157">Si *plNumFiles* no se inicializa en cero y un error en la infraestructura com hace que la función devuelva S \_ false antes de que se llame a **IWiaDevMgr2:: GetImageDlg** , entonces *plNumFiles* tendrá un valor de elemento no utilizado erróneo.</span><span class="sxs-lookup"><span data-stu-id="b0545-157">If *plNumFiles* is not initialized to zero and a failure in the COM infrastructure causes the function to return S\_FALSE before **IWiaDevMgr2::GetImageDlg** is called, then *plNumFiles* will have a misleading garbage value.</span></span>

<span data-ttu-id="b0545-158">El cuadro de diálogo debe tener derechos suficientes en *bstrFolderName* para que pueda guardar los archivos con nombres de archivo únicos.</span><span class="sxs-lookup"><span data-stu-id="b0545-158">The dialog box must have sufficient rights to *bstrFolderName* so that it can save the files with unique file names.</span></span> <span data-ttu-id="b0545-159">Proteja la carpeta con una lista de control de acceso (ACL), ya que contiene datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="b0545-159">Protect the folder with an access control list (ACL) because it contains user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0545-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0545-160">Requirements</span></span>



| <span data-ttu-id="b0545-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0545-161">Requirement</span></span> | <span data-ttu-id="b0545-162">Value</span><span class="sxs-lookup"><span data-stu-id="b0545-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b0545-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0545-163">Minimum supported client</span></span><br/> | <span data-ttu-id="b0545-164">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b0545-164">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b0545-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0545-165">Minimum supported server</span></span><br/> | <span data-ttu-id="b0545-166">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0545-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b0545-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0545-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0545-168"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0545-168"><dt>Wia.h</dt></span></span> </dl> |



 

 
