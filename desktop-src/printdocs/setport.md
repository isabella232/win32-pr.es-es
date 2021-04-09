---
description: La función SetPort establece el estado asociado a un puerto de impresora.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: Función SetPort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082602"
---
# <a name="setport-function"></a><span data-ttu-id="654be-103">SetPort función)</span><span class="sxs-lookup"><span data-stu-id="654be-103">SetPort function</span></span>

<span data-ttu-id="654be-104">La función **SetPort** establece el estado asociado a un puerto de impresora.</span><span class="sxs-lookup"><span data-stu-id="654be-104">The **SetPort** function sets the status associated with a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="654be-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="654be-105">Syntax</span></span>


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a><span data-ttu-id="654be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="654be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="654be-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="654be-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="654be-108">Puntero a una cadena terminada en cero que especifica el nombre del servidor de impresión al que está conectado el puerto.</span><span class="sxs-lookup"><span data-stu-id="654be-108">Pointer to a zero-terminated string that specifies the name of the printer server to which the port is connected.</span></span> <span data-ttu-id="654be-109">Establezca este parámetro en **null** si el puerto está en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="654be-109">Set this parameter to **NULL** if the port is on the local machine.</span></span>

</dd> <dt>

<span data-ttu-id="654be-110">*pPortName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="654be-110">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="654be-111">Puntero a una cadena terminada en cero que especifica el nombre del puerto de impresora.</span><span class="sxs-lookup"><span data-stu-id="654be-111">Pointer to a zero-terminated string that specifies the name of the printer port.</span></span>

</dd> <dt>

<span data-ttu-id="654be-112">*dwLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="654be-112">*dwLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="654be-113">Especifica el tipo de estructura al que apunta el parámetro *pPortInfo* .</span><span class="sxs-lookup"><span data-stu-id="654be-113">Specifies the type of structure pointed to by the *pPortInfo* parameter.</span></span>

<span data-ttu-id="654be-114">Este valor debe ser 3, que corresponde a una estructura de datos de [**Port \_ info \_ 3**](port-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="654be-114">This value must be 3, which corresponds to a [**PORT\_INFO\_3**](port-info-3.md) data structure.</span></span>

</dd> <dt>

<span data-ttu-id="654be-115">*pPortInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="654be-115">*pPortInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="654be-116">Puntero a una estructura de la [**información de puerto \_ \_ 3**](port-info-3.md) que contiene la información de estado de puerto que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="654be-116">Pointer to a [**PORT\_INFO\_3**](port-info-3.md) structure that contains the port status information to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="654be-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="654be-117">Return value</span></span>

<span data-ttu-id="654be-118">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="654be-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="654be-119">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="654be-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="654be-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="654be-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="654be-121">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="654be-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="654be-122">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="654be-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="654be-123">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="654be-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="654be-124">El autor de la llamada de la función **SetPort** debe ejecutarse como administrador.</span><span class="sxs-lookup"><span data-stu-id="654be-124">The caller of the **SetPort** function must be executing as an Administrator.</span></span> <span data-ttu-id="654be-125">Además, si el autor de la llamada es un monitor de puerto o un monitor de idioma, debe llamar a [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) para cesar la suplantación antes de llamar a **SetPort**.</span><span class="sxs-lookup"><span data-stu-id="654be-125">Additionally, if the caller is a Port Monitor or Language Monitor, it must call [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) to cease impersonation before it calls **SetPort**.</span></span>

<span data-ttu-id="654be-126">Todos los programas que llaman a **SetPort** deben tener acceso de servidor para \_ \_ administrar el acceso al servidor al que está conectado el puerto.</span><span class="sxs-lookup"><span data-stu-id="654be-126">All programs that call **SetPort** must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="654be-127">Cuando se establece un valor de estado de puerto de impresora con el valor de gravedad puerto de \_ \_ tipo \_ error, el administrador de trabajos de impresión deja de enviar trabajos al puerto.</span><span class="sxs-lookup"><span data-stu-id="654be-127">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="654be-128">El administrador de trabajos de impresión reanuda el envío de trabajos al puerto cuando el estado del puerto está desactivado por otra llamada a **SetPort**.</span><span class="sxs-lookup"><span data-stu-id="654be-128">The print spooler resumes sending jobs to the port when the port status is cleared by another call to **SetPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="654be-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="654be-129">Requirements</span></span>



| <span data-ttu-id="654be-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="654be-130">Requirement</span></span> | <span data-ttu-id="654be-131">Value</span><span class="sxs-lookup"><span data-stu-id="654be-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="654be-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="654be-132">Minimum supported client</span></span><br/> | <span data-ttu-id="654be-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="654be-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="654be-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="654be-134">Minimum supported server</span></span><br/> | <span data-ttu-id="654be-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="654be-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="654be-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="654be-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="654be-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="654be-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="654be-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="654be-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="654be-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="654be-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="654be-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="654be-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="654be-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="654be-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="654be-142">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="654be-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="654be-143">**SetPortW** (Unicode) y **SetPortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="654be-143">**SetPortW** (Unicode) and **SetPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="654be-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="654be-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="654be-145">Impresión</span><span class="sxs-lookup"><span data-stu-id="654be-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="654be-146">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="654be-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="654be-147">**INFO. de puerto \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="654be-147">**PORT\_INFO\_3**</span></span>](port-info-3.md)
</dt> </dl>

 

