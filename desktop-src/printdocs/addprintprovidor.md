---
description: La función AddPrintProvidor instala un proveedor de impresión local y vincula los archivos de configuración, datos y proveedor.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Función AddPrintProvidor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: adf5f914046eb82e070e3e9915325989ff868d1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677729"
---
# <a name="addprintprovidor-function"></a><span data-ttu-id="9fa8f-103">AddPrintProvidor función)</span><span class="sxs-lookup"><span data-stu-id="9fa8f-103">AddPrintProvidor function</span></span>

<span data-ttu-id="9fa8f-104">La función **AddPrintProvidor** instala un proveedor de impresión local y vincula los archivos de configuración, datos y proveedor.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-104">The **AddPrintProvidor** function installs a local print provider and links the configuration, data, and provider files.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fa8f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fa8f-105">Syntax</span></span>


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="9fa8f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fa8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fa8f-107">*pName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9fa8f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa8f-108">Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se debe instalar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-108">A pointer to a null-terminated string that specifies the name of the server on which the provider should be installed.</span></span> <span data-ttu-id="9fa8f-109">En el caso de los sistemas que solo admiten la instalación local de proveedores, este parámetro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-109">For systems that only support local installation of providers, this parameter should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9fa8f-110">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9fa8f-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa8f-111">Nivel de la estructura a la que apunta *pProviderInfo* .</span><span class="sxs-lookup"><span data-stu-id="9fa8f-111">The level of the structure to which *pProviderInfo* points.</span></span> <span data-ttu-id="9fa8f-112">Puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-112">It can be one of the following.</span></span>



| <span data-ttu-id="9fa8f-113">Value</span><span class="sxs-lookup"><span data-stu-id="9fa8f-113">Value</span></span>                                                                                                | <span data-ttu-id="9fa8f-114">Significado</span><span class="sxs-lookup"><span data-stu-id="9fa8f-114">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="9fa8f-115"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="9fa8f-115"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="9fa8f-116">La función usa una estructura [**PROVIDOR \_ info \_ 1**](providor-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="9fa8f-116">Function uses a [**PROVIDOR\_INFO\_1**](providor-info-1.md) structure.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="9fa8f-117"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="9fa8f-117"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="9fa8f-118">La función usa una estructura de [**PROVIDOR \_ info \_ 2**](providor-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="9fa8f-118">Function uses a [**PROVIDOR\_INFO\_2**](providor-info-2.md) structure.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9fa8f-119">*pProviderInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9fa8f-119">*pProviderInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa8f-120">Puntero a una estructura de proveedor de impresión, tal y como se indica en el *nivel*.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-120">A pointer to a print provider structure, as indicated by *Level*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fa8f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fa8f-121">Return value</span></span>

<span data-ttu-id="9fa8f-122">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9fa8f-123">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-123">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fa8f-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fa8f-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9fa8f-125">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9fa8f-126">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9fa8f-127">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9fa8f-128">Antes de que una aplicación llame a la función **AddPrintProvidor** , todos los archivos requeridos por el proveedor deben copiarse en el directorio system32.</span><span class="sxs-lookup"><span data-stu-id="9fa8f-128">Before an application calls the **AddPrintProvidor** function, all files required by the provider must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="9fa8f-129">Un proveedor agregado por **AddPrintProvidor** se puede quitar llamando a [**DeletePrintProvidor**](deleteprintprovidor.md).</span><span class="sxs-lookup"><span data-stu-id="9fa8f-129">A provider added by **AddPrintProvidor** may be removed by calling [**DeletePrintProvidor**](deleteprintprovidor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa8f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fa8f-130">Requirements</span></span>



| <span data-ttu-id="9fa8f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fa8f-131">Requirement</span></span> | <span data-ttu-id="9fa8f-132">Value</span><span class="sxs-lookup"><span data-stu-id="9fa8f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa8f-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fa8f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9fa8f-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9fa8f-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9fa8f-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fa8f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9fa8f-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9fa8f-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9fa8f-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fa8f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fa8f-138"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9fa8f-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9fa8f-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9fa8f-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="9fa8f-140"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fa8f-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9fa8f-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9fa8f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fa8f-142"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="9fa8f-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="9fa8f-143">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="9fa8f-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9fa8f-144">**AddPrintProvidorW** (Unicode) y **AddPrintProvidorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9fa8f-144">**AddPrintProvidorW** (Unicode) and **AddPrintProvidorA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="9fa8f-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fa8f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa8f-146">Impresión</span><span class="sxs-lookup"><span data-stu-id="9fa8f-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9fa8f-147">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="9fa8f-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9fa8f-148">**DeletePrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-148">**DeletePrintProvidor**</span></span>](deleteprintprovidor.md)
</dt> <dt>

[<span data-ttu-id="9fa8f-149">**PROVIDOR \_ info \_ 1**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-149">**PROVIDOR\_INFO\_1**</span></span>](providor-info-1.md)
</dt> <dt>

[<span data-ttu-id="9fa8f-150">**PROVIDOR \_ info \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9fa8f-150">**PROVIDOR\_INFO\_2**</span></span>](providor-info-2.md)
</dt> </dl>

 

 




