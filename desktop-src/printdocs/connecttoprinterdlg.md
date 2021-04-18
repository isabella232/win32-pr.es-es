---
description: La función ConnectToPrinterDlg muestra un cuadro de diálogo que permite a los usuarios examinar y conectarse a las impresoras de una red.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: Función ConnectToPrinterDlg (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678375"
---
# <a name="connecttoprinterdlg-function"></a><span data-ttu-id="b7f4a-103">ConnectToPrinterDlg función)</span><span class="sxs-lookup"><span data-stu-id="b7f4a-103">ConnectToPrinterDlg function</span></span>

<span data-ttu-id="b7f4a-104">La función **ConnectToPrinterDlg** muestra un cuadro de diálogo que permite a los usuarios examinar y conectarse a las impresoras de una red.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-104">The **ConnectToPrinterDlg** function displays a dialog box that lets users browse and connect to printers on a network.</span></span> <span data-ttu-id="b7f4a-105">Si el usuario selecciona una impresora, la función intenta crear una conexión con ella. Si no hay un controlador adecuado instalado en el servidor, el usuario tiene la opción de crear una impresora localmente.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-105">If the user selects a printer, the function attempts to create a connection to it; if a suitable driver is not installed on the server, the user is given the option of creating a printer locally.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f4a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7f4a-106">Syntax</span></span>


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="b7f4a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7f4a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7f4a-108">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b7f4a-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7f4a-109">Especifica la ventana primaria del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-109">Specifies the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b7f4a-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b7f4a-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7f4a-111">Este parámetro está reservado y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-111">This parameter is reserved and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7f4a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7f4a-112">Return value</span></span>

<span data-ttu-id="b7f4a-113">Si la función se ejecuta correctamente y el usuario selecciona una impresora, el valor devuelto es un identificador de la impresora seleccionada.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-113">If the function succeeds and the user selects a printer, the return value is a handle to the selected printer.</span></span>

<span data-ttu-id="b7f4a-114">Si se produce un error en la función o el usuario cancela el cuadro de diálogo sin seleccionar una impresora, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-114">If the function fails, or the user cancels the dialog box without selecting a printer, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7f4a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7f4a-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b7f4a-116">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b7f4a-117">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b7f4a-118">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b7f4a-119">La función **ConnectToPrinterDlg** intenta crear una conexión a la impresora seleccionada.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-119">The **ConnectToPrinterDlg** function attempts to create a connection to the selected printer.</span></span> <span data-ttu-id="b7f4a-120">Sin embargo, si el servidor en el que reside la impresora no tiene instalado un controlador adecuado, la función ofrece al usuario la opción de crear una impresora localmente.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-120">However, if the server on which the printer resides does not have a suitable driver installed, the function offers the user the option of creating a printer locally.</span></span> <span data-ttu-id="b7f4a-121">Una aplicación que realiza la llamada puede determinar si la función ha creado una impresora localmente llamando a [**GetPrinter**](getprinter.md) con una estructura de [**\_ información \_ 2**](printer-info-2.md) de la impresora y, a continuación, examinando el miembro de **atributos** de la estructura.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-121">A calling application can determine whether the function has created a printer locally by calling [**GetPrinter**](getprinter.md) with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, then examining that structure's **Attributes** member.</span></span>

<span data-ttu-id="b7f4a-122">Una aplicación debe llamar a [**DeletePrinter**](deleteprinter.md) para eliminar una impresora local.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-122">An application should call [**DeletePrinter**](deleteprinter.md) to delete a local printer.</span></span> <span data-ttu-id="b7f4a-123">Una aplicación debe llamar a [**DeletePrinterConnection**](deleteprinterconnection.md) para eliminar una conexión a una impresora.</span><span class="sxs-lookup"><span data-stu-id="b7f4a-123">An application should call [**DeletePrinterConnection**](deleteprinterconnection.md) to delete a connection to a printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7f4a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7f4a-124">Requirements</span></span>



| <span data-ttu-id="b7f4a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f4a-125">Requirement</span></span> | <span data-ttu-id="b7f4a-126">Value</span><span class="sxs-lookup"><span data-stu-id="b7f4a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f4a-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7f4a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f4a-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b7f4a-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b7f4a-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7f4a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f4a-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b7f4a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b7f4a-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7f4a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7f4a-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7f4a-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b7f4a-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b7f4a-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7f4a-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7f4a-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b7f4a-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7f4a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7f4a-136"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b7f4a-136"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="b7f4a-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7f4a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f4a-138">Impresión</span><span class="sxs-lookup"><span data-stu-id="b7f4a-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b7f4a-139">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="b7f4a-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b7f4a-140">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="b7f4a-140">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="b7f4a-141">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="b7f4a-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="b7f4a-142">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="b7f4a-142">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="b7f4a-143">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="b7f4a-143">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="b7f4a-144">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="b7f4a-144">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="b7f4a-145">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b7f4a-145">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




