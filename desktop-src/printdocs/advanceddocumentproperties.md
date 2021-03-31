---
description: La función AdvancedDocumentProperties muestra un cuadro de diálogo de configuración de impresora para la impresora especificada, lo que permite al usuario configurar esa impresora.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: Función AdvancedDocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817771"
---
# <a name="advanceddocumentproperties-function"></a><span data-ttu-id="f3cf5-103">AdvancedDocumentProperties función)</span><span class="sxs-lookup"><span data-stu-id="f3cf5-103">AdvancedDocumentProperties function</span></span>

<span data-ttu-id="f3cf5-104">La función **AdvancedDocumentProperties** muestra un cuadro de diálogo de configuración de impresora para la impresora especificada, lo que permite al usuario configurar esa impresora.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-104">The **AdvancedDocumentProperties** function displays a printer-configuration dialog box for the specified printer, allowing the user to configure that printer.</span></span>

<span data-ttu-id="f3cf5-105">Esta función es un caso especial de la función [**DocumentProperties**](documentproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="f3cf5-105">This function is a special case of the [**DocumentProperties**](documentproperties.md) function.</span></span> <span data-ttu-id="f3cf5-106">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-106">For more details, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3cf5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3cf5-107">Syntax</span></span>


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a><span data-ttu-id="f3cf5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3cf5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3cf5-109">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3cf5-109">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3cf5-110">Identificador de la ventana primaria del cuadro de diálogo de configuración de la impresora.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-110">A handle to the parent window of the printer-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="f3cf5-111">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3cf5-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3cf5-112">Identificador de un objeto de impresora.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-112">A handle to a printer object.</span></span> <span data-ttu-id="f3cf5-113">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f3cf5-114">*pDeviceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3cf5-114">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3cf5-115">Un puntero a una cadena terminada en null que especifica el nombre del dispositivo para el que se debe mostrar un cuadro de diálogo de configuración de impresora.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-115">A pointer to a null-terminated string specifying the name of the device for which a printer-configuration dialog box should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="f3cf5-116">*pDevModeOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f3cf5-116">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3cf5-117">Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contendrá los datos de configuración especificados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that will contain the configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="f3cf5-118">*pDevModeInput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3cf5-118">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3cf5-119">Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contiene los datos de configuración que se utilizan para inicializar los controles del cuadro de diálogo de configuración de la impresora.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-119">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains the configuration data used to initialize the controls of the printer-configuration dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3cf5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3cf5-120">Return value</span></span>

<span data-ttu-id="f3cf5-121">Si la función [**DocumentProperties**](documentproperties.md) con estos parámetros es correcta, el valor devuelto de **AdvancedDocumentProperties** es 1.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-121">If the [**DocumentProperties**](documentproperties.md) function with these parameters is successful, the return value of **AdvancedDocumentProperties** is 1.</span></span> <span data-ttu-id="f3cf5-122">De lo contrario, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-122">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3cf5-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3cf5-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f3cf5-124">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f3cf5-125">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f3cf5-126">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f3cf5-127">Esta función solo puede mostrar el cuadro de diálogo Configuración de impresora para que un usuario pueda configurarlo.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-127">This function can only display the printer-configuration dialog box so a user can configure it.</span></span> <span data-ttu-id="f3cf5-128">Para obtener más control, utilice [**DocumentProperties**](documentproperties.md).</span><span class="sxs-lookup"><span data-stu-id="f3cf5-128">For more control, use [**DocumentProperties**](documentproperties.md).</span></span> <span data-ttu-id="f3cf5-129">Los parámetros de entrada de esta función se pasan directamente a **DocumentProperties** y el valor *fMode* se establece en DM \_ en \_ buffer \| DM en el \_ \_ \| búfer DM \_ out \_ .</span><span class="sxs-lookup"><span data-stu-id="f3cf5-129">The input parameters for this function are passed directly to **DocumentProperties** and the *fMode* value is set to DM\_IN\_BUFFER \| DM\_IN\_PROMPT \| DM\_OUT\_BUFFER.</span></span> <span data-ttu-id="f3cf5-130">A diferencia de **DocumentProperties**, esta función solo devuelve 1 o 0.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-130">Unlike **DocumentProperties**, this function only returns 1 or 0.</span></span> <span data-ttu-id="f3cf5-131">Por lo tanto, no se puede determinar el tamaño necesario de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) estableciendo *pDevMode* en cero.</span><span class="sxs-lookup"><span data-stu-id="f3cf5-131">Thus, you cannot determine the required size of [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) by setting *pDevMode* to zero.</span></span>

<span data-ttu-id="f3cf5-132">Una aplicación puede obtener el nombre al que apunta el parámetro *pDeviceName* llamando a la función [**GetPrinter**](getprinter.md) y, a continuación, examinando el miembro **pPrinterName** de la estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="f3cf5-132">An application can obtain the name pointed to by the *pDeviceName* parameter by calling the [**GetPrinter**](getprinter.md) function and then examining the **pPrinterName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3cf5-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3cf5-133">Requirements</span></span>



| <span data-ttu-id="f3cf5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3cf5-134">Requirement</span></span> | <span data-ttu-id="f3cf5-135">Value</span><span class="sxs-lookup"><span data-stu-id="f3cf5-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3cf5-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3cf5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f3cf5-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f3cf5-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f3cf5-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3cf5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f3cf5-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3cf5-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f3cf5-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3cf5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3cf5-141"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3cf5-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f3cf5-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3cf5-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="f3cf5-143"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3cf5-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f3cf5-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3cf5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3cf5-145"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f3cf5-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f3cf5-146">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f3cf5-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f3cf5-147">**AdvancedDocumentPropertiesW** (Unicode) y **AdvancedDocumentPropertiesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f3cf5-147">**AdvancedDocumentPropertiesW** (Unicode) and **AdvancedDocumentPropertiesA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f3cf5-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3cf5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3cf5-149">Impresión</span><span class="sxs-lookup"><span data-stu-id="f3cf5-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f3cf5-150">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="f3cf5-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f3cf5-151">**AddPrinter (**</span><span class="sxs-lookup"><span data-stu-id="f3cf5-151">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="f3cf5-152">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="f3cf5-152">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="f3cf5-153">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="f3cf5-153">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="f3cf5-154">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="f3cf5-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="f3cf5-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f3cf5-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f3cf5-156">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f3cf5-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




