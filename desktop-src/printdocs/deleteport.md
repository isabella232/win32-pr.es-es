---
description: La función DeletePort muestra un cuadro de diálogo que permite al usuario eliminar un nombre de puerto.
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: Función DeletePort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fa0e3d4b0b5fd43d946d0b6a96b96d0494997a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277679"
---
# <a name="deleteport-function"></a><span data-ttu-id="060a4-103">DeletePort función)</span><span class="sxs-lookup"><span data-stu-id="060a4-103">DeletePort function</span></span>

<span data-ttu-id="060a4-104">La función **DeletePort** muestra un cuadro de diálogo que permite al usuario eliminar un nombre de puerto.</span><span class="sxs-lookup"><span data-stu-id="060a4-104">The **DeletePort** function displays a dialog box that allows the user to delete a port name.</span></span>

## <a name="syntax"></a><span data-ttu-id="060a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="060a4-105">Syntax</span></span>


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="060a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="060a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="060a4-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="060a4-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="060a4-108">Puntero a una cadena terminada en cero que especifica el nombre del servidor para el que se debe eliminar el puerto.</span><span class="sxs-lookup"><span data-stu-id="060a4-108">A pointer to a zero-terminated string that specifies the name of the server for which the port should be deleted.</span></span> <span data-ttu-id="060a4-109">Si este parámetro es **null**, se elimina un puerto local.</span><span class="sxs-lookup"><span data-stu-id="060a4-109">If this parameter is **NULL**, a local port is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="060a4-110">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="060a4-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="060a4-111">Identificador de la ventana primaria del cuadro de diálogo de eliminación de puertos.</span><span class="sxs-lookup"><span data-stu-id="060a4-111">A handle to the parent window of the port-deletion dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="060a4-112">*pPortName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="060a4-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="060a4-113">Puntero a una cadena terminada en cero que especifica el nombre del puerto que se debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="060a4-113">A pointer to a zero-terminated string that specifies the name of the port that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="060a4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="060a4-114">Return value</span></span>

<span data-ttu-id="060a4-115">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="060a4-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="060a4-116">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="060a4-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="060a4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="060a4-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="060a4-118">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="060a4-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="060a4-119">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="060a4-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="060a4-120">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="060a4-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="060a4-121">Una aplicación puede recuperar los nombres de puertos válidos mediante una llamada a la función [**EnumPorts**](enumports.md) .</span><span class="sxs-lookup"><span data-stu-id="060a4-121">An application can retrieve the names of valid ports by calling the [**EnumPorts**](enumports.md) function.</span></span>

<span data-ttu-id="060a4-122">La función **DeletePort** devuelve un error si una impresora está conectada actualmente al puerto especificado.</span><span class="sxs-lookup"><span data-stu-id="060a4-122">The **DeletePort** function returns an error if a printer is currently connected to the specified port.</span></span>

<span data-ttu-id="060a4-123">El autor de la llamada de la función **DeletePort** debe tener acceso al servidor \_ \_ para administrar el acceso al servidor al que está conectado el puerto.</span><span class="sxs-lookup"><span data-stu-id="060a4-123">The caller of the **DeletePort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="060a4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="060a4-124">Requirements</span></span>



| <span data-ttu-id="060a4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="060a4-125">Requirement</span></span> | <span data-ttu-id="060a4-126">Value</span><span class="sxs-lookup"><span data-stu-id="060a4-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="060a4-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="060a4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="060a4-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="060a4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="060a4-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="060a4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="060a4-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="060a4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="060a4-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="060a4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="060a4-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="060a4-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="060a4-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="060a4-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="060a4-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="060a4-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="060a4-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="060a4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="060a4-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="060a4-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="060a4-137">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="060a4-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="060a4-138">**DeletePortW** (Unicode) y **DeletePortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="060a4-138">**DeletePortW** (Unicode) and **DeletePortA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="060a4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="060a4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="060a4-140">Impresión</span><span class="sxs-lookup"><span data-stu-id="060a4-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="060a4-141">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="060a4-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="060a4-142">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="060a4-142">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="060a4-143">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="060a4-143">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




