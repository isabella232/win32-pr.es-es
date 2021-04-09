---
description: Muestra un cuadro de diálogo al usuario para preparar la adquisición de imágenes.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: IWiaItem2::D método eviceDlg (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154402"
---
# <a name="iwiaitem2devicedlg-method"></a><span data-ttu-id="e24b4-103">IWiaItem2::D método eviceDlg</span><span class="sxs-lookup"><span data-stu-id="e24b4-103">IWiaItem2::DeviceDlg method</span></span>

<span data-ttu-id="e24b4-104">Muestra un cuadro de diálogo al usuario para preparar la adquisición de imágenes.</span><span class="sxs-lookup"><span data-stu-id="e24b4-104">Displays a dialog box to the user to prepare for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="e24b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e24b4-105">Syntax</span></span>


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="e24b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e24b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e24b4-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e24b4-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e24b4-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="e24b4-108">Type: **LONG**</span></span>

<span data-ttu-id="e24b4-109">Especifica un conjunto de marcas que controlan la operación del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e24b4-109">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="e24b4-110">El valor puede ser 0 para representar el comportamiento predeterminado o cualquiera de las marcas de \_ diálogo del dispositivo WIA \_ descritas en [**WiaFlag**](-wia-wiaflag.md).</span><span class="sxs-lookup"><span data-stu-id="e24b4-110">The value can be either 0 to represent the default behavior or any of the WIA\_DEVICE\_DIALOG flags described in [**WiaFlag**](-wia-wiaflag.md).</span></span>

</dd> <dt>

<span data-ttu-id="e24b4-111">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e24b4-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e24b4-112">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="e24b4-112">Type: **HWND**</span></span>

<span data-ttu-id="e24b4-113">Identificador de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="e24b4-113">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="e24b4-114">*bstrFolderName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e24b4-114">*bstrFolderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e24b4-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e24b4-115">Type: **BSTR**</span></span>

<span data-ttu-id="e24b4-116">Especifica el nombre de la carpeta donde se transferirán los archivos.</span><span class="sxs-lookup"><span data-stu-id="e24b4-116">Specifies the folder name where the files are to be transferred.</span></span>

</dd> <dt>

<span data-ttu-id="e24b4-117">*bstrFilename* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e24b4-117">*bstrFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e24b4-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e24b4-118">Type: **BSTR**</span></span>

<span data-ttu-id="e24b4-119">Especifica el nombre del archivo de plantilla.</span><span class="sxs-lookup"><span data-stu-id="e24b4-119">Specifies the template file name.</span></span>

</dd> <dt>

<span data-ttu-id="e24b4-120">*plNumFiles* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e24b4-120">*plNumFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e24b4-121">Tipo: \**Long \** _</span><span class="sxs-lookup"><span data-stu-id="e24b4-121">Type: \**LONG\** _</span></span>

<span data-ttu-id="e24b4-122">Puntero al número de elementos de la matriz _ppbstrFilePaths \*.</span><span class="sxs-lookup"><span data-stu-id="e24b4-122">A pointer to the number of items in the _ppbstrFilePaths\* array.</span></span>

</dd> <dt>

<span data-ttu-id="e24b4-123">*ppbstrFilePaths* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e24b4-123">*ppbstrFilePaths* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e24b4-124">Tipo: **BSTR \* \***</span><span class="sxs-lookup"><span data-stu-id="e24b4-124">Type: **BSTR\*\***</span></span>

<span data-ttu-id="e24b4-125">Dirección de un puntero a una matriz de rutas de acceso de los archivos digitalizados.</span><span class="sxs-lookup"><span data-stu-id="e24b4-125">The address of a pointer to an array of paths for the scanned files.</span></span> <span data-ttu-id="e24b4-126">Inicialice el puntero para que apunte a una matriz de tamaño cero (0) antes de que se llame a **IWiaItem2::D evicedlg** .</span><span class="sxs-lookup"><span data-stu-id="e24b4-126">Initialize the pointer to point to an array of size zero (0) before **IWiaItem2::DeviceDlg** is called.</span></span>

</dd> <dt>

<span data-ttu-id="e24b4-127">*ppIWiaItem2* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e24b4-127">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e24b4-128">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e24b4-128">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="e24b4-129">La dirección de una matriz de punteros a las interfaces de [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="e24b4-129">The address of an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e24b4-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e24b4-130">Return value</span></span>

<span data-ttu-id="e24b4-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e24b4-131">Type: **HRESULT**</span></span>

<span data-ttu-id="e24b4-132">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e24b4-132">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e24b4-133">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e24b4-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e24b4-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e24b4-134">Remarks</span></span>

<span data-ttu-id="e24b4-135">Este método muestra un cuadro de diálogo al usuario que una aplicación usa para recopilar toda la información necesaria para la adquisición de la imagen.</span><span class="sxs-lookup"><span data-stu-id="e24b4-135">This method displays a dialog box to the user that an application uses to gather all the information required for image acquisition.</span></span> <span data-ttu-id="e24b4-136">También se usa para especificar propiedades de examen de imagen como el brillo y el contraste.</span><span class="sxs-lookup"><span data-stu-id="e24b4-136">It is also used to specify image scan properties such as brightness and contrast.</span></span>

<span data-ttu-id="e24b4-137">Cuando se devuelve este método, la aplicación puede usar la interfaz [**IWiaTransfer**](-wia-iwiatransfer.md) para adquirir la imagen.</span><span class="sxs-lookup"><span data-stu-id="e24b4-137">After this method returns, the application can use the [**IWiaTransfer**](-wia-iwiatransfer.md) interface to acquire the image.</span></span>

<span data-ttu-id="e24b4-138">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para cada elemento de la matriz de punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="e24b4-138">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method for each element in the array of interface pointers they receive through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="e24b4-139">Las aplicaciones también deben liberar la matriz mediante [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="e24b4-139">Applications must also free the array using [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="e24b4-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e24b4-140">Requirements</span></span>



| <span data-ttu-id="e24b4-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e24b4-141">Requirement</span></span> | <span data-ttu-id="e24b4-142">Value</span><span class="sxs-lookup"><span data-stu-id="e24b4-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e24b4-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e24b4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e24b4-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e24b4-144">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e24b4-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e24b4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e24b4-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e24b4-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e24b4-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e24b4-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="e24b4-148"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e24b4-148"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="e24b4-149">IDL</span><span class="sxs-lookup"><span data-stu-id="e24b4-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e24b4-150"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e24b4-150"><dt>Wia.idl</dt></span></span> </dl> |



 

 
