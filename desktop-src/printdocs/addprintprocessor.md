---
description: La función AddPrintProcessor instala un procesador de impresión en el servidor especificado y agrega el nombre del procesador de impresión a la lista de procesadores de impresión admitidos.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: Función AddPrintProcessor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 871df9fee211ae13e1552978ce651840d7f542f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678323"
---
# <a name="addprintprocessor-function"></a><span data-ttu-id="74930-103">AddPrintProcessor función)</span><span class="sxs-lookup"><span data-stu-id="74930-103">AddPrintProcessor function</span></span>

<span data-ttu-id="74930-104">La función **AddPrintProcessor** instala un procesador de impresión en el servidor especificado y agrega el nombre del procesador de impresión a la lista de procesadores de impresión admitidos.</span><span class="sxs-lookup"><span data-stu-id="74930-104">The **AddPrintProcessor** function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span>

## <a name="syntax"></a><span data-ttu-id="74930-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74930-105">Syntax</span></span>


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="74930-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74930-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74930-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74930-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74930-108">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se debe instalar el procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="74930-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor should be installed.</span></span> <span data-ttu-id="74930-109">Si este parámetro es **null**, el procesador de impresión se instala localmente.</span><span class="sxs-lookup"><span data-stu-id="74930-109">If this parameter is **NULL**, the print processor is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="74930-110">*pEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74930-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74930-111">Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="74930-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="74930-112">Si este parámetro es **null**, se utiliza el entorno actual del llamador/cliente (no del destino/servidor).</span><span class="sxs-lookup"><span data-stu-id="74930-112">If this parameter is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="74930-113">*pPathName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74930-113">*pPathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74930-114">Puntero a una cadena terminada en null que especifica el nombre del archivo que contiene el procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="74930-114">A pointer to a null-terminated string that specifies the name of the file that contains the print processor.</span></span> <span data-ttu-id="74930-115">Este archivo debe estar en el directorio del procesador de impresión del sistema.</span><span class="sxs-lookup"><span data-stu-id="74930-115">This file must be in the system print-processor directory.</span></span>

</dd> <dt>

<span data-ttu-id="74930-116">*pPrintProcessorName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74930-116">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74930-117">Puntero a una cadena terminada en null que especifica el nombre del procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="74930-117">A pointer to a null-terminated string that specifies the name of the print processor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74930-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74930-118">Return value</span></span>

<span data-ttu-id="74930-119">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="74930-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="74930-120">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="74930-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="74930-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74930-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="74930-122">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="74930-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="74930-123">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="74930-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="74930-124">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="74930-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="74930-125">El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="74930-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="74930-126">Antes de llamar a la función **AddPrintProcessor** , una aplicación debe comprobar que el archivo que contiene el procesador de impresión se almacena en el directorio del procesador de impresión del sistema.</span><span class="sxs-lookup"><span data-stu-id="74930-126">Before calling the **AddPrintProcessor** function, an application should verify that the file containing the print processor is stored in the system print-processor directory.</span></span> <span data-ttu-id="74930-127">Una aplicación puede recuperar el nombre del directorio del procesador de impresión del sistema llamando a la función [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="74930-127">An application can retrieve the name of the system print-processor directory by calling the [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) function.</span></span>

<span data-ttu-id="74930-128">Una aplicación puede determinar el nombre de los procesadores de impresión existentes mediante una llamada a la función [**EnumPrintProcessors**](enumprintprocessors.md) .</span><span class="sxs-lookup"><span data-stu-id="74930-128">An application can determine the name of existing print processors by calling the [**EnumPrintProcessors**](enumprintprocessors.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="74930-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74930-129">Requirements</span></span>



| <span data-ttu-id="74930-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="74930-130">Requirement</span></span> | <span data-ttu-id="74930-131">Value</span><span class="sxs-lookup"><span data-stu-id="74930-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74930-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74930-132">Minimum supported client</span></span><br/> | <span data-ttu-id="74930-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="74930-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="74930-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74930-134">Minimum supported server</span></span><br/> | <span data-ttu-id="74930-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="74930-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="74930-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74930-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="74930-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74930-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="74930-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74930-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="74930-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74930-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="74930-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74930-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74930-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="74930-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="74930-142">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="74930-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="74930-143">**AddPrintProcessorW** (Unicode) y **AddPrintProcessorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="74930-143">**AddPrintProcessorW** (Unicode) and **AddPrintProcessorA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="74930-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="74930-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74930-145">Impresión</span><span class="sxs-lookup"><span data-stu-id="74930-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="74930-146">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="74930-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="74930-147">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="74930-147">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="74930-148">**GetPrintProcessorDirectory**</span><span class="sxs-lookup"><span data-stu-id="74930-148">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)
</dt> </dl>

 

