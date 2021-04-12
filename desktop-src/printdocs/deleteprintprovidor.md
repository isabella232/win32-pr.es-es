---
description: La función DeletePrintProvidor quita un proveedor de impresión agregado por la función AddPrintProvidor.
ms.assetid: b7104f9a-111c-4904-a355-063bb4cc81f1
title: Función DeletePrintProvidor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProvidor
- DeletePrintProvidorA
- DeletePrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e68e56f115bac8abb1d0999990f57067f791d76d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277678"
---
# <a name="deleteprintprovidor-function"></a><span data-ttu-id="96282-103">DeletePrintProvidor función)</span><span class="sxs-lookup"><span data-stu-id="96282-103">DeletePrintProvidor function</span></span>

<span data-ttu-id="96282-104">La función **DeletePrintProvidor** quita un proveedor de impresión agregado por la función [**AddPrintProvidor**](addprintprovidor.md) .</span><span class="sxs-lookup"><span data-stu-id="96282-104">The **DeletePrintProvidor** function removes a print provider added by the [**AddPrintProvidor**](addprintprovidor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="96282-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96282-105">Syntax</span></span>


```C++
BOOL DeletePrintProvidor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProviderName
);
```



## <a name="parameters"></a><span data-ttu-id="96282-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96282-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96282-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96282-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96282-108">Sector debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="96282-108">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="96282-109">*pEnvironment* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96282-109">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96282-110">Puntero a una cadena terminada en null que especifica el entorno desde el que se va a quitar el proveedor (por ejemplo, Windows NT x86, Windows IA64 o Windows x64).</span><span class="sxs-lookup"><span data-stu-id="96282-110">A pointer to a null-terminated string that specifies the environment from which the provider is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="96282-111">Si este parámetro es **null**, el proveedor se quita del entorno actual de la aplicación que realiza la llamada y del equipo cliente (no de la aplicación de destino y del servidor de impresión).</span><span class="sxs-lookup"><span data-stu-id="96282-111">If this parameter is **NULL**, the provider is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="96282-112">**Null** es el valor recomendado porque proporciona la máxima portabilidad.</span><span class="sxs-lookup"><span data-stu-id="96282-112">**NULL** is the recommended value because it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="96282-113">*pPrintProviderName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96282-113">*pPrintProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96282-114">Puntero a una cadena terminada en null que especifica el nombre del proveedor que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="96282-114">A pointer to a null-terminated string that specifies the name of the provider to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96282-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96282-115">Return value</span></span>

<span data-ttu-id="96282-116">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="96282-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="96282-117">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="96282-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="96282-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96282-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="96282-119">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="96282-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="96282-120">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="96282-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="96282-121">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="96282-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96282-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96282-122">Requirements</span></span>



| <span data-ttu-id="96282-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="96282-123">Requirement</span></span> | <span data-ttu-id="96282-124">Value</span><span class="sxs-lookup"><span data-stu-id="96282-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96282-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96282-125">Minimum supported client</span></span><br/> | <span data-ttu-id="96282-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="96282-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="96282-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96282-127">Minimum supported server</span></span><br/> | <span data-ttu-id="96282-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="96282-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="96282-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96282-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="96282-130"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96282-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="96282-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96282-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="96282-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96282-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="96282-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96282-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96282-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="96282-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="96282-135">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="96282-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="96282-136">**DeletePrintProvidorW** (Unicode) y **DeletePrintProvidorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="96282-136">**DeletePrintProvidorW** (Unicode) and **DeletePrintProvidorA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="96282-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="96282-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96282-138">Impresión</span><span class="sxs-lookup"><span data-stu-id="96282-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="96282-139">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="96282-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="96282-140">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="96282-140">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




