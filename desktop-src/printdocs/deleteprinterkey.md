---
description: La función DeletePrinterKey elimina una clave especificada y todas sus subclaves para una impresora especificada.
ms.assetid: 0bd81b43-5c1e-4989-8350-2ec0dc215f28
title: Función DeletePrinterKey (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterKey
- DeletePrinterKeyA
- DeletePrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4be073f7832f647e156dbd3b5e12d23ffe6acc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815355"
---
# <a name="deleteprinterkey-function"></a><span data-ttu-id="ad06d-103">DeletePrinterKey función)</span><span class="sxs-lookup"><span data-stu-id="ad06d-103">DeletePrinterKey function</span></span>

<span data-ttu-id="ad06d-104">La función **DeletePrinterKey** elimina una clave especificada y todas sus subclaves para una impresora especificada.</span><span class="sxs-lookup"><span data-stu-id="ad06d-104">The **DeletePrinterKey** function deletes a specified key and all its subkeys for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad06d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad06d-105">Syntax</span></span>


```C++
DWORD DeletePrinterKey(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName
);
```



## <a name="parameters"></a><span data-ttu-id="ad06d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad06d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad06d-107">*hPrinter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ad06d-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad06d-108">Identificador de la impresora para la que la función elimina una clave.</span><span class="sxs-lookup"><span data-stu-id="ad06d-108">A handle to the printer for which the function deletes a key.</span></span> <span data-ttu-id="ad06d-109">Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.</span><span class="sxs-lookup"><span data-stu-id="ad06d-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="ad06d-110">*pKeyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ad06d-110">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad06d-111">Puntero a una cadena terminada en null que especifica la clave que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="ad06d-111">A pointer to a null-terminated string that specifies the key to delete.</span></span> <span data-ttu-id="ad06d-112">Use el carácter de barra diagonal inversa ( \\ ) como delimitador para especificar una ruta de acceso con una o más subclaves.</span><span class="sxs-lookup"><span data-stu-id="ad06d-112">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span>

<span data-ttu-id="ad06d-113">Si *pKeyName* es una cadena vacía (""), **DeletePrinterKey** elimina todas las claves por debajo de la clave de nivel superior de la impresora.</span><span class="sxs-lookup"><span data-stu-id="ad06d-113">If *pKeyName* is an empty string (""), **DeletePrinterKey** deletes all keys below the top-level key for the printer.</span></span> <span data-ttu-id="ad06d-114">Si *pKeyName* es **null**, **DELETEPRINTERKEY** devuelve un \_ parámetro de error no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="ad06d-114">If *pKeyName* is **NULL**, **DeletePrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad06d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad06d-115">Return value</span></span>

<span data-ttu-id="ad06d-116">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ad06d-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="ad06d-117">Si se produce un error en la función, el valor devuelto es un código de error del sistema.</span><span class="sxs-lookup"><span data-stu-id="ad06d-117">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad06d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad06d-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ad06d-119">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="ad06d-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ad06d-120">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ad06d-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ad06d-121">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="ad06d-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad06d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad06d-122">Requirements</span></span>



| <span data-ttu-id="ad06d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad06d-123">Requirement</span></span> | <span data-ttu-id="ad06d-124">Value</span><span class="sxs-lookup"><span data-stu-id="ad06d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad06d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad06d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ad06d-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ad06d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ad06d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad06d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ad06d-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ad06d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ad06d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad06d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad06d-130"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad06d-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ad06d-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad06d-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="ad06d-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad06d-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ad06d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ad06d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad06d-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ad06d-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ad06d-135">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ad06d-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ad06d-136">**DeletePrinterKeyW** (Unicode) y **DeletePrinterKeyA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ad06d-136">**DeletePrinterKeyW** (Unicode) and **DeletePrinterKeyA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="ad06d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad06d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad06d-138">Impresión</span><span class="sxs-lookup"><span data-stu-id="ad06d-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ad06d-139">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="ad06d-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ad06d-140">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="ad06d-140">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="ad06d-141">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="ad06d-141">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="ad06d-142">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="ad06d-142">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="ad06d-143">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="ad06d-143">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="ad06d-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="ad06d-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="ad06d-145">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="ad06d-145">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




