---
description: Recupera la ruta de acceso al paquete de controladores de impresora especificado en un servidor de impresión.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: Función GetPrinterDriverPackagePath (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ea355782df6cce7910f92a46af3cde320536106e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707229"
---
# <a name="getprinterdriverpackagepath-function"></a><span data-ttu-id="588db-103">GetPrinterDriverPackagePath función)</span><span class="sxs-lookup"><span data-stu-id="588db-103">GetPrinterDriverPackagePath function</span></span>

<span data-ttu-id="588db-104">Recupera la ruta de acceso al paquete de controladores de impresora especificado en un servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="588db-104">Retrieves the path to the specified printer driver package on a print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="588db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="588db-105">Syntax</span></span>


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a><span data-ttu-id="588db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="588db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="588db-107">*pszServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="588db-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="588db-108">Puntero a una cadena constante terminada en null que especifica el nombre del servidor de impresión.</span><span class="sxs-lookup"><span data-stu-id="588db-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="588db-109">Use **null** para el equipo local.</span><span class="sxs-lookup"><span data-stu-id="588db-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="588db-110">*pszEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="588db-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="588db-111">Puntero a una cadena constante terminada en null que especifica la arquitectura del procesador (por ejemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="588db-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="588db-112">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="588db-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="588db-113">*pszLanguage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="588db-113">*pszLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="588db-114">Puntero a una cadena constante terminada en null que especifica el idioma de la [interfaz de usuario multilingüe](/windows/desktop/Intl/mui-resource-management) para el controlador que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="588db-114">A pointer to a constant, null-terminated string that specifies the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) language for the driver being installed.</span></span> <span data-ttu-id="588db-115">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="588db-115">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="588db-116">*pszPackageID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="588db-116">*pszPackageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="588db-117">Puntero a una cadena constante terminada en null que especifica el identificador del paquete de controladores.</span><span class="sxs-lookup"><span data-stu-id="588db-117">A pointer to a constant, null-terminated string that specifies the ID of the driver package.</span></span>

</dd> <dt>

<span data-ttu-id="588db-118">*pszDriverPackageCab* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="588db-118">*pszDriverPackageCab* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="588db-119">Un puntero a una cadena terminada en null que especifica la ruta de acceso al archivo. cab para el paquete de controladores.</span><span class="sxs-lookup"><span data-stu-id="588db-119">A pointer to a null-terminated string that specifies the path to the cabinet file for the driver package.</span></span> <span data-ttu-id="588db-120">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="588db-120">This can be **NULL**.</span></span> <span data-ttu-id="588db-121">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="588db-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="588db-122">*cchDriverPackageCab* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="588db-122">*cchDriverPackageCab* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="588db-123">Tamaño, en caracteres, del búfer *pszDriverPackageCab* .</span><span class="sxs-lookup"><span data-stu-id="588db-123">The size, in characters, of the *pszDriverPackageCab* buffer.</span></span> <span data-ttu-id="588db-124">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="588db-124">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="588db-125">*pcchRequiredSize* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="588db-125">*pcchRequiredSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="588db-126">Puntero al tamaño requerido del búfer de *pszDriverPackageCab* .</span><span class="sxs-lookup"><span data-stu-id="588db-126">A pointer to the required size of the *pszDriverPackageCab* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="588db-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="588db-127">Return value</span></span>

<span data-ttu-id="588db-128">Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.</span><span class="sxs-lookup"><span data-stu-id="588db-128">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="588db-129">Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="588db-129">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="588db-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="588db-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="588db-131">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="588db-131">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="588db-132">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="588db-132">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="588db-133">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="588db-133">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="588db-134">Para obtener un valor para *cchDriverPackageCab*, llame a la función con **null** como el valor de *pszDriverPackageCab*.</span><span class="sxs-lookup"><span data-stu-id="588db-134">To obtain a value for *cchDriverPackageCab*, call the function with **NULL** as the value of *pszDriverPackageCab*.</span></span> <span data-ttu-id="588db-135">Use el valor devuelto en *pcchRequiredSize* como el valor de *cchDriverPackageCab* y vuelva a llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="588db-135">Use the value returned in *pcchRequiredSize* as the value of *cchDriverPackageCab* and call the function again.</span></span>

<span data-ttu-id="588db-136">El *pszPackageID* se suele obtener de una llamada a [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).</span><span class="sxs-lookup"><span data-stu-id="588db-136">The *pszPackageID* is typically obtained from a call to [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="588db-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="588db-137">Requirements</span></span>



| <span data-ttu-id="588db-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="588db-138">Requirement</span></span> | <span data-ttu-id="588db-139">Value</span><span class="sxs-lookup"><span data-stu-id="588db-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="588db-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="588db-140">Minimum supported client</span></span><br/> | <span data-ttu-id="588db-141">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="588db-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="588db-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="588db-142">Minimum supported server</span></span><br/> | <span data-ttu-id="588db-143">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="588db-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="588db-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="588db-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="588db-145"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="588db-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="588db-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="588db-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="588db-147"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="588db-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="588db-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="588db-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="588db-149"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="588db-149"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="588db-150">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="588db-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="588db-151">**GetPrinterDriverPackagePathW** (Unicode) y **GetPrinterDriverPackagePathA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="588db-151">**GetPrinterDriverPackagePathW** (Unicode) and **GetPrinterDriverPackagePathA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="588db-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="588db-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="588db-153">Impresión</span><span class="sxs-lookup"><span data-stu-id="588db-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="588db-154">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="588db-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

