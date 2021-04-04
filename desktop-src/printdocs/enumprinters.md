---
description: La función EnumPrinters enumera las impresoras, los servidores de impresión, los dominios o los proveedores de impresión disponibles.
ms.assetid: 0d0cc726-c515-4146-9273-cdf1db3c76b7
title: Función EnumPrinters (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinters
- EnumPrintersA
- EnumPrintersW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6d82e8e6ff4f56a3c67fa29c48e982ebe0fd4599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909589"
---
# <a name="enumprinters-function"></a><span data-ttu-id="6c08b-103">EnumPrinters función)</span><span class="sxs-lookup"><span data-stu-id="6c08b-103">EnumPrinters function</span></span>

<span data-ttu-id="6c08b-104">La función **EnumPrinters** enumera las impresoras, los servidores de impresión, los dominios o los proveedores de impresión disponibles.</span><span class="sxs-lookup"><span data-stu-id="6c08b-104">The **EnumPrinters** function enumerates available printers, print servers, domains, or print providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c08b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c08b-105">Syntax</span></span>


```C++
BOOL EnumPrinters(
  _In_  DWORD   Flags,
  _In_  LPTSTR  Name,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinterEnum,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="6c08b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c08b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c08b-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="6c08b-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c08b-108">Los tipos de objetos de impresión que la función debe enumerar.</span><span class="sxs-lookup"><span data-stu-id="6c08b-108">The types of print objects that the function should enumerate.</span></span> <span data-ttu-id="6c08b-109">Este valor puede ser uno o varios de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="6c08b-109">This value can be one or more of the following values.</span></span>



| <span data-ttu-id="6c08b-110">Value</span><span class="sxs-lookup"><span data-stu-id="6c08b-110">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="6c08b-111">Significado</span><span class="sxs-lookup"><span data-stu-id="6c08b-111">Meaning</span></span>                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRINTER_ENUM_LOCAL"></span><span id="printer_enum_local"></span><dl> <span data-ttu-id="6c08b-112"><dt>**\_enumeración \_ local de impresora**</dt></span><span class="sxs-lookup"><span data-stu-id="6c08b-112"><dt>**PRINTER\_ENUM\_LOCAL**</dt></span></span> </dl>                       | <span data-ttu-id="6c08b-113">Si \_ \_ no se pasa también la marca Printer enum Name, la función omite el parámetro *Name* y enumera las impresoras instaladas localmente.</span><span class="sxs-lookup"><span data-stu-id="6c08b-113">If the PRINTER\_ENUM\_NAME flag is not also passed, the function ignores the *Name* parameter, and enumerates the locally installed printers.</span></span> <span data-ttu-id="6c08b-114">Si \_ también se pasa el nombre de la enumeración de impresora \_ , la función enumera las impresoras locales en el *nombre*.</span><span class="sxs-lookup"><span data-stu-id="6c08b-114">If PRINTER\_ENUM\_NAME is also passed, the function enumerates the local printers on *Name*.</span></span> <br/> |
| <span id="PRINTER_ENUM_NAME"></span><span id="printer_enum_name"></span><dl> <span data-ttu-id="6c08b-115"><dt>**nombre de la \_ enumeración de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c08b-115"><dt>**PRINTER\_ENUM\_NAME**</dt></span></span> </dl>                          | <span data-ttu-id="6c08b-116">La función enumera la impresora identificada por el *nombre*.</span><span class="sxs-lookup"><span data-stu-id="6c08b-116">The function enumerates the printer identified by *Name*.</span></span> <span data-ttu-id="6c08b-117">Puede ser un servidor, un dominio o un proveedor de impresión.</span><span class="sxs-lookup"><span data-stu-id="6c08b-117">This can be a server, a domain, or a print provider.</span></span> <span data-ttu-id="6c08b-118">Si *Name* es **null**, la función enumera los proveedores de impresión disponibles.</span><span class="sxs-lookup"><span data-stu-id="6c08b-118">If *Name* is **NULL**, the function enumerates available print providers.</span></span><br/>                                                    |
| <span id="PRINTER_ENUM_SHARED"></span><span id="printer_enum_shared"></span><dl> <span data-ttu-id="6c08b-119"><dt>**\_enumeración de impresora \_ compartida**</dt></span><span class="sxs-lookup"><span data-stu-id="6c08b-119"><dt>**PRINTER\_ENUM\_SHARED**</dt></span></span> </dl>                    | <span data-ttu-id="6c08b-120">La función enumera las impresoras que tienen el atributo Shared.</span><span class="sxs-lookup"><span data-stu-id="6c08b-120">The function enumerates printers that have the shared attribute.</span></span> <span data-ttu-id="6c08b-121">No se puede usar en aislamiento; Use una operación o para combinar con otro \_ tipo de enumeración de impresora.</span><span class="sxs-lookup"><span data-stu-id="6c08b-121">Cannot be used in isolation; use an OR operation to combine with another PRINTER\_ENUM type.</span></span><br/>                                                                               |
| <span id="PRINTER_ENUM_CONNECTIONS"></span><span id="printer_enum_connections"></span><dl> <span data-ttu-id="6c08b-122"><dt>**\_conexiones de enumeración de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c08b-122"><dt>**PRINTER\_ENUM\_CONNECTIONS**</dt></span></span> </dl>     | <span data-ttu-id="6c08b-123">La función enumera la lista de impresoras en las que el usuario ha realizado conexiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="6c08b-123">The function enumerates the list of printers to which the user has made previous connections.</span></span><br/>                                                                                                                                               |
| <span id="PRINTER_ENUM_NETWORK"></span><span id="printer_enum_network"></span><dl> <span data-ttu-id="6c08b-124"><dt>**\_red enum de impresora \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c08b-124"><dt>**PRINTER\_ENUM\_NETWORK**</dt></span></span> </dl>                 | <span data-ttu-id="6c08b-125">La función enumera las impresoras de red en el dominio del equipo.</span><span class="sxs-lookup"><span data-stu-id="6c08b-125">The function enumerates network printers in the computer's domain.</span></span> <span data-ttu-id="6c08b-126">Este valor solo es válido si el *nivel* es 1.</span><span class="sxs-lookup"><span data-stu-id="6c08b-126">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                                                |
| <span id="PRINTER_ENUM_REMOTE"></span><span id="printer_enum_remote"></span><dl> <span data-ttu-id="6c08b-127"><dt>**\_enumeración de impresora \_ remota**</dt></span><span class="sxs-lookup"><span data-stu-id="6c08b-127"><dt>**PRINTER\_ENUM\_REMOTE**</dt></span></span> </dl>                    | <span data-ttu-id="6c08b-128">La función enumera las impresoras de red y los servidores de impresión en el dominio del equipo.</span><span class="sxs-lookup"><span data-stu-id="6c08b-128">The function enumerates network printers and print servers in the computer's domain.</span></span> <span data-ttu-id="6c08b-129">Este valor solo es válido si el *nivel* es 1.</span><span class="sxs-lookup"><span data-stu-id="6c08b-129">This value is valid only if *Level* is 1.</span></span><br/>                                                                                                              |
| <span id="PRINTER_ENUM_CATEGORY_3D"></span><span id="printer_enum_category_3d"></span><dl> <span data-ttu-id="6c08b-130"><dt>**\_Categoría de enumeración de impresora \_ \_ 3D**</dt></span><span class="sxs-lookup"><span data-stu-id="6c08b-130"><dt>**PRINTER\_ENUM\_CATEGORY\_3D**</dt></span></span> </dl>    | <span data-ttu-id="6c08b-131">La función solo enumera las impresoras 3D.</span><span class="sxs-lookup"><span data-stu-id="6c08b-131">The function enumerates only 3D printers.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PRINTER_ENUM_CATEGORY_ALL"></span><span id="printer_enum_category_all"></span><dl> <span data-ttu-id="6c08b-132"><dt>**Categoría de enum de impresora \_ \_ \_ All**</dt></span><span class="sxs-lookup"><span data-stu-id="6c08b-132"><dt>**PRINTER\_ENUM\_CATEGORY\_ALL**</dt></span></span> </dl> | <span data-ttu-id="6c08b-133">La función enumera todos los dispositivos de impresión, incluidas las impresoras 3D.</span><span class="sxs-lookup"><span data-stu-id="6c08b-133">The function enumerates all print devices, including 3D printers.</span></span><br/>                                                                                                                                                                           |



 

<span data-ttu-id="6c08b-134">Si el *nivel* es 4, solo puede usar las constantes de enumeración Printer \_ \_ Connection y Printer \_ enum \_ local.</span><span class="sxs-lookup"><span data-stu-id="6c08b-134">If *Level* is 4, you can only use the PRINTER\_ENUM\_CONNECTIONS and PRINTER\_ENUM\_LOCAL constants.</span></span>

> [!Note]  
> <span data-ttu-id="6c08b-135">los dispositivos de impresión 3D no se enumeran de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6c08b-135">3D print devices are not enumerated by default.</span></span> <span data-ttu-id="6c08b-136">Debe incluir la **categoría de \_ enum \_ Printer \_ 3D** y **Printer \_ enum \_ local** para enumerar solo las impresoras 3D.</span><span class="sxs-lookup"><span data-stu-id="6c08b-136">You must include both **PRINTER\_ENUM\_CATEGORY\_3D** and **PRINTER\_ENUM\_LOCAL** to enumerate only 3D printers.</span></span> <span data-ttu-id="6c08b-137">Para incluir impresoras 3D, junto con todas las demás impresoras locales, use **Printer \_ enum \_ Category \_ All** y **Printer \_ enum \_ local**.</span><span class="sxs-lookup"><span data-stu-id="6c08b-137">To include 3D printers, along with all other local printers, use **PRINTER\_ENUM\_CATEGORY\_ALL** and **PRINTER\_ENUM\_LOCAL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="6c08b-138">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6c08b-138">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c08b-139">Si el *nivel* es 1, las *marcas* contienen \_ el nombre de la enumeración de la impresora \_ y *el nombre* no es **null**, el *nombre* es un puntero a una cadena terminada en null que especifica el nombre del objeto que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="6c08b-139">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is non-**NULL**, then *Name* is a pointer to a null-terminated string that specifies the name of the object to enumerate.</span></span> <span data-ttu-id="6c08b-140">Esta cadena puede ser el nombre de un servidor, un dominio o un proveedor de impresión.</span><span class="sxs-lookup"><span data-stu-id="6c08b-140">This string can be the name of a server, a domain, or a print provider.</span></span>

<span data-ttu-id="6c08b-141">Si el *nivel* es 1, las *marcas* contienen el nombre de la enumeración de la impresora \_ y el \_ *nombre* es **null**, la función enumera los proveedores de impresión disponibles.</span><span class="sxs-lookup"><span data-stu-id="6c08b-141">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_NAME, and *Name* is **NULL**, then the function enumerates the available print providers.</span></span>

<span data-ttu-id="6c08b-142">Si *LEVEL* es 1, *Flags* contiene Printer \_ enum \_ Remote y *Name* es **null**, la función enumera las impresoras del dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="6c08b-142">If *Level* is 1, *Flags* contains PRINTER\_ENUM\_REMOTE, and *Name* is **NULL**, then the function enumerates the printers in the user's domain.</span></span>

<span data-ttu-id="6c08b-143">Si *LEVEL* es 2 o 5,*Name* es un puntero a una cadena terminada en null que especifica el nombre de un servidor cuyas impresoras se van a enumerar.</span><span class="sxs-lookup"><span data-stu-id="6c08b-143">If *Level* is 2 or 5,*Name* is a pointer to a null-terminated string that specifies the name of a server whose printers are to be enumerated.</span></span> <span data-ttu-id="6c08b-144">Si esta cadena es **null**, la función enumera las impresoras instaladas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="6c08b-144">If this string is **NULL**, then the function enumerates the printers installed on the local computer.</span></span>

<span data-ttu-id="6c08b-145">Si el *nivel* es 4, *el nombre* debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="6c08b-145">If *Level* is 4, *Name* should be **NULL**.</span></span> <span data-ttu-id="6c08b-146">La función siempre realiza consultas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="6c08b-146">The function always queries on the local computer.</span></span>

<span data-ttu-id="6c08b-147">Cuando *el* valor de Name es **null**, al establecer *Flags* en Printer \_ enum \_ local \| Printer \_ enum \_ Connections se enumeran las impresoras instaladas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="6c08b-147">When *Name* is **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_CONNECTIONS enumerates printers that are installed on the local machine.</span></span> <span data-ttu-id="6c08b-148">Estas impresoras incluyen las que están conectadas físicamente al equipo local, así como a las impresoras remotas en las que tiene una conexión de red.</span><span class="sxs-lookup"><span data-stu-id="6c08b-148">These printers include those that are physically attached to the local machine as well as remote printers to which it has a network connection.</span></span>

<span data-ttu-id="6c08b-149">Cuando *Name* no es **null**, al establecer *Flags* en Printer \_ enum \_ local \| Printer \_ \_ Name enum se enumeran las impresoras locales instaladas en el *nombre* del servidor.</span><span class="sxs-lookup"><span data-stu-id="6c08b-149">When *Name* is not **NULL**, setting *Flags* to PRINTER\_ENUM\_LOCAL \| PRINTER\_ENUM\_NAME enumerates the local printers that are installed on the server *Name*.</span></span>

</dd> <dt>

<span data-ttu-id="6c08b-150">*Nivel* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6c08b-150">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c08b-151">Tipo de estructuras de datos a las que apunta *pPrinterEnum*.</span><span class="sxs-lookup"><span data-stu-id="6c08b-151">The type of data structures pointed to by *pPrinterEnum*.</span></span> <span data-ttu-id="6c08b-152">Los valores válidos son 1, 2, 4 y 5, que corresponden a las estructuras de datos de la información de la [**impresora \_ \_ 1**](printer-info-1.md), la información de la [**impresora \_ \_ 2**](printer-info-2.md) , la información de la [**impresora \_ \_ 4**](printer-info-4.md)y la información de la [**impresora \_ \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="6c08b-152">Valid values are 1, 2, 4, and 5, which correspond to the [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), and [**PRINTER\_INFO\_5**](printer-info-5.md) data structures.</span></span>

<span data-ttu-id="6c08b-153">Este valor puede ser 1, 2, 4 o 5.</span><span class="sxs-lookup"><span data-stu-id="6c08b-153">This value can be 1, 2, 4, or 5.</span></span>

</dd> <dt>

<span data-ttu-id="6c08b-154">*pPrinterEnum* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c08b-154">*pPrinterEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c08b-155">Un puntero a un búfer que recibe una matriz de las estructuras de la información de la [**impresora \_ \_ 1**](printer-info-1.md), la información de la impresora [**\_ \_ 2**](printer-info-2.md), la información de la [**impresora \_ \_ 4**](printer-info-4.md)o la información de la [**impresora \_ \_ 5**](printer-info-5.md) .</span><span class="sxs-lookup"><span data-stu-id="6c08b-155">A pointer to a buffer that receives an array of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md), [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span> <span data-ttu-id="6c08b-156">Cada estructura contiene datos que describen un objeto de impresión disponible.</span><span class="sxs-lookup"><span data-stu-id="6c08b-156">Each structure contains data that describes an available print object.</span></span>

<span data-ttu-id="6c08b-157">Si el *nivel* es 1, la matriz contiene estructuras de [**información de impresora \_ \_ 1**](printer-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="6c08b-157">If *Level* is 1, the array contains [**PRINTER\_INFO\_1**](printer-info-1.md) structures.</span></span> <span data-ttu-id="6c08b-158">Si el *nivel* es 2, la matriz contiene estructuras de [**\_ información \_ 2**](printer-info-2.md) de la impresora.</span><span class="sxs-lookup"><span data-stu-id="6c08b-158">If *Level* is 2, the array contains [**PRINTER\_INFO\_2**](printer-info-2.md) structures.</span></span> <span data-ttu-id="6c08b-159">Si el *nivel* es 4, la matriz contiene estructuras de la información de la [**impresora \_ \_ 4**](printer-info-4.md) .</span><span class="sxs-lookup"><span data-stu-id="6c08b-159">If *Level* is 4, the array contains [**PRINTER\_INFO\_4**](printer-info-4.md) structures.</span></span> <span data-ttu-id="6c08b-160">Si el *nivel* es 5, la matriz contiene estructuras de [**\_ información \_ 5**](printer-info-5.md) de la impresora.</span><span class="sxs-lookup"><span data-stu-id="6c08b-160">If *Level* is 5, the array contains [**PRINTER\_INFO\_5**](printer-info-5.md) structures.</span></span>

<span data-ttu-id="6c08b-161">El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras de datos y las cadenas u otros datos a los que apuntan los miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="6c08b-161">The buffer must be large enough to receive the array of data structures and any strings or other data to which the structure members point.</span></span> <span data-ttu-id="6c08b-162">Si el búfer es demasiado pequeño, el parámetro *pcbNeeded* devuelve el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="6c08b-162">If the buffer is too small, the *pcbNeeded* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="6c08b-163">*cbBuf* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6c08b-163">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c08b-164">Tamaño, en bytes, del búfer al que apunta *pPrinterEnum*.</span><span class="sxs-lookup"><span data-stu-id="6c08b-164">The size, in bytes, of the buffer pointed to by *pPrinterEnum*.</span></span>

</dd> <dt>

<span data-ttu-id="6c08b-165">*pcbNeeded* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c08b-165">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c08b-166">Un puntero a un valor que recibe el número de bytes copiados si la función se ejecuta correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="6c08b-166">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="6c08b-167">*pcReturned* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c08b-167">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c08b-168">Un puntero a un valor que recibe el número de estructuras de la información de la [**impresora \_ \_ 1**](printer-info-1.md), la información de la [**impresora \_ \_ 2**](printer-info-2.md) , la información de la [**impresora \_ \_ 4**](printer-info-4.md)o las estructuras de la información de la impresora [**\_ \_ 5**](printer-info-5.md) que devuelve la función en la matriz a la que señala *pPrinterEnum* .</span><span class="sxs-lookup"><span data-stu-id="6c08b-168">A pointer to a value that receives the number of [**PRINTER\_INFO\_1**](printer-info-1.md), [**PRINTER\_INFO\_2**](printer-info-2.md) , [**PRINTER\_INFO\_4**](printer-info-4.md), or [**PRINTER\_INFO\_5**](printer-info-5.md) structures that the function returns in the array to which *pPrinterEnum* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c08b-169">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c08b-169">Return value</span></span>

<span data-ttu-id="6c08b-170">Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6c08b-170">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6c08b-171">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="6c08b-171">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c08b-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c08b-172">Remarks</span></span>

<span data-ttu-id="6c08b-173">No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="6c08b-173">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="6c08b-174">Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6c08b-174">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6c08b-175">La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación.</span><span class="sxs-lookup"><span data-stu-id="6c08b-175">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6c08b-176">Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.</span><span class="sxs-lookup"><span data-stu-id="6c08b-176">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6c08b-177">Si **EnumPrinters** devuelve una estructura de [**información de impresora \_ \_ 1**](printer-info-1.md) en la que \_ se especifica el contenedor de enumeración de impresora \_ , esto indica que hay una jerarquía de objetos de impresora.</span><span class="sxs-lookup"><span data-stu-id="6c08b-177">If **EnumPrinters** returns a [**PRINTER\_INFO\_1**](printer-info-1.md) structure in which PRINTER\_ENUM\_CONTAINER is specified, this indicates that there is a hierarchy of printer objects.</span></span> <span data-ttu-id="6c08b-178">Una aplicación puede enumerar la jerarquía llamando a **EnumPrinters** de nuevo, estableciendo el *nombre* en el valor del miembro **pName** de la estructura de **\_ información \_** de la impresora.</span><span class="sxs-lookup"><span data-stu-id="6c08b-178">An application can enumerate the hierarchy by calling **EnumPrinters** again, setting *Name* to the value of the **PRINTER\_INFO\_1** structure's **pName** member.</span></span>

<span data-ttu-id="6c08b-179">La función **EnumPrinters** no recupera información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6c08b-179">The **EnumPrinters** function does not retrieve security information.</span></span> <span data-ttu-id="6c08b-180">Si se devuelven las estructuras de la información de la [**impresora \_ \_ 2**](printer-info-2.md) en la matriz a la que señala *pPrinterEnum*, sus miembros *pSecurityDescriptor* se establecerán en **null**.</span><span class="sxs-lookup"><span data-stu-id="6c08b-180">If [**PRINTER\_INFO\_2**](printer-info-2.md) structures are returned in the array pointed to by *pPrinterEnum*, their *pSecurityDescriptor* members will be set to **NULL**.</span></span>

<span data-ttu-id="6c08b-181">Para obtener información acerca de la impresora predeterminada, llame a [**GetDefaultPrinter**](getdefaultprinter.md).</span><span class="sxs-lookup"><span data-stu-id="6c08b-181">To get information about the default printer, call [**GetDefaultPrinter**](getdefaultprinter.md).</span></span>

<span data-ttu-id="6c08b-182">La estructura de la información de la [**impresora \_ \_ 4**](printer-info-4.md) proporciona una manera fácil y sumamente rápida de recuperar los nombres de las impresoras instaladas en un equipo local, así como las conexiones remotas que ha establecido un usuario.</span><span class="sxs-lookup"><span data-stu-id="6c08b-182">The [**PRINTER\_INFO\_4**](printer-info-4.md) structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="6c08b-183">Cuando se llama a **EnumPrinters** con una estructura de datos de la información de la **impresora \_ \_ 4** , esa función consulta el registro para obtener la información especificada y, a continuación, vuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="6c08b-183">When **EnumPrinters** is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="6c08b-184">Esto difiere del comportamiento de **EnumPrinters** cuando se llama con otros niveles de **información de impresora \_ \_ \* *_ estructuras de datos. En concreto, cuando*** se llama a _ EnumPrinters con una estructura de datos de nivel 2 (información de la [**impresora \_ \_ 2**](printer-info-2.md)), realiza una llamada [**OpenPrinter**](openprinter.md) en cada conexión remota.</span><span class="sxs-lookup"><span data-stu-id="6c08b-184">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_\**_ data structures. In particular, when _\* EnumPrinters*\* is called with a level 2 ([**PRINTER\_INFO\_2**](printer-info-2.md)) data structure, it performs an [**OpenPrinter**](openprinter.md) call on each remote connection.</span></span> <span data-ttu-id="6c08b-185">Si una conexión remota está inactiva o el servidor remoto ya no existe o la impresora remota ya no existe, la función debe esperar a que se agote el tiempo de espera de RPC y, por tanto, se produzca un error en la llamada **OpenPrinter** .</span><span class="sxs-lookup"><span data-stu-id="6c08b-185">If a remote connection is down, or the remote server no longer exists, or the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="6c08b-186">Esto puede tardar unos minutos.</span><span class="sxs-lookup"><span data-stu-id="6c08b-186">This can take a while.</span></span> <span data-ttu-id="6c08b-187">Pasar una estructura de la información de la **impresora \_ \_ 4** permite que una aplicación recupere un mínimo de la información necesaria; si se desea obtener información más detallada, se puede realizar una llamada posterior al nivel 2 de **EnumPrinters** .</span><span class="sxs-lookup"><span data-stu-id="6c08b-187">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinters** level 2 call can be made.</span></span>

<span data-ttu-id="6c08b-188">**Windows Vista:** Los datos de la impresora devueltos por **EnumPrinters** se recuperan de una caché local cuando el valor del *nivel* es 4.</span><span class="sxs-lookup"><span data-stu-id="6c08b-188">**Windows Vista:** The printer data returned by **EnumPrinters** is retrieved from a local cache when the value of *Level* is 4.</span></span>

<span data-ttu-id="6c08b-189">En la tabla siguiente se muestra la salida de **EnumPrinters** para varios valores de *marcas* cuando el parámetro *LEVEL* está establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="6c08b-189">The following table shows the **EnumPrinters** output for various *Flags* values when the *Level* parameter is set to 1.</span></span>

<span data-ttu-id="6c08b-190">En la columna parámetro de *nombre* de la tabla, debe sustituir un nombre apropiado para el proveedor de impresión, el dominio y la máquina.</span><span class="sxs-lookup"><span data-stu-id="6c08b-190">In the *Name* parameter column of the table, you should substitute an appropriate name for Print Provider, Domain, and Machine.</span></span> <span data-ttu-id="6c08b-191">Por ejemplo, para "proveedor de impresión", puede usar el nombre del proveedor de impresión de red o el nombre del proveedor de impresión local.</span><span class="sxs-lookup"><span data-stu-id="6c08b-191">For example, for "Print Provider," you could use the name of the network print provider or the name of the local print provider.</span></span> <span data-ttu-id="6c08b-192">Para recuperar los nombres de proveedor de impresión, llame a **EnumPrinters** con *el nombre* establecido en **null**.</span><span class="sxs-lookup"><span data-stu-id="6c08b-192">To retrieve print provider names, call **EnumPrinters** with *Name* set to **NULL**.</span></span>



| <span data-ttu-id="6c08b-193">*Flags* , parámetro</span><span class="sxs-lookup"><span data-stu-id="6c08b-193">*Flags* parameter</span></span>                                  | <span data-ttu-id="6c08b-194">Parámetro *Name*</span><span class="sxs-lookup"><span data-stu-id="6c08b-194">*Name* parameter</span></span>                            | <span data-ttu-id="6c08b-195">Resultado</span><span class="sxs-lookup"><span data-stu-id="6c08b-195">Result</span></span>                                                                                            |
|----------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c08b-196">\_Enumeración \_ de impresora local (y no \_ nombre de enumeración de impresora \_ )</span><span class="sxs-lookup"><span data-stu-id="6c08b-196">PRINTER\_ENUM\_LOCAL (and not PRINTER\_ENUM\_NAME)</span></span> | <span data-ttu-id="6c08b-197">Se omite el parámetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="6c08b-197">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="6c08b-198">Todas las impresoras locales.</span><span class="sxs-lookup"><span data-stu-id="6c08b-198">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="6c08b-199">nombre de la \_ enumeración de impresora \_</span><span class="sxs-lookup"><span data-stu-id="6c08b-199">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="6c08b-200">"Proveedor de impresión"</span><span class="sxs-lookup"><span data-stu-id="6c08b-200">"Print Provider"</span></span><br/>                 | <span data-ttu-id="6c08b-201">Todos los nombres de dominio</span><span class="sxs-lookup"><span data-stu-id="6c08b-201">All domain names</span></span><br/>                                                                       |
| <span data-ttu-id="6c08b-202">nombre de la \_ enumeración de impresora \_</span><span class="sxs-lookup"><span data-stu-id="6c08b-202">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="6c08b-203">"Proveedor de impresión! Dominio</span><span class="sxs-lookup"><span data-stu-id="6c08b-203">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="6c08b-204">Todas las impresoras y servidores de impresión en el dominio del equipo</span><span class="sxs-lookup"><span data-stu-id="6c08b-204">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="6c08b-205">nombre de la \_ enumeración de impresora \_</span><span class="sxs-lookup"><span data-stu-id="6c08b-205">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="6c08b-206">"Print Provider!! \\ \\ Sistema</span><span class="sxs-lookup"><span data-stu-id="6c08b-206">"Print Provider!!\\\\Machine"</span></span><br/>    | <span data-ttu-id="6c08b-207">Todas las impresoras compartidas en el \\ \\ equipo</span><span class="sxs-lookup"><span data-stu-id="6c08b-207">All printers shared at \\\\Machine</span></span><br/>                                                     |
| <span data-ttu-id="6c08b-208">nombre de la \_ enumeración de impresora \_</span><span class="sxs-lookup"><span data-stu-id="6c08b-208">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="6c08b-209">Una cadena vacía, ""</span><span class="sxs-lookup"><span data-stu-id="6c08b-209">An empty string, ""</span></span><br/>              | <span data-ttu-id="6c08b-210">Todas las impresoras locales.</span><span class="sxs-lookup"><span data-stu-id="6c08b-210">All local printers.</span></span><br/>                                                                    |
| <span data-ttu-id="6c08b-211">nombre de la \_ enumeración de impresora \_</span><span class="sxs-lookup"><span data-stu-id="6c08b-211">PRINTER\_ENUM\_NAME</span></span>                                | <span data-ttu-id="6c08b-212">**NULL**</span><span class="sxs-lookup"><span data-stu-id="6c08b-212">**NULL**</span></span><br/>                         | <span data-ttu-id="6c08b-213">Todos los proveedores de impresión en el dominio del equipo</span><span class="sxs-lookup"><span data-stu-id="6c08b-213">All print providers in the computer's domain</span></span><br/>                                           |
| <span data-ttu-id="6c08b-214">\_conexiones de enumeración de impresora \_</span><span class="sxs-lookup"><span data-stu-id="6c08b-214">PRINTER\_ENUM\_CONNECTIONS</span></span>                         | <span data-ttu-id="6c08b-215">Se omite el parámetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="6c08b-215">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="6c08b-216">Todas las impresoras remotas conectadas</span><span class="sxs-lookup"><span data-stu-id="6c08b-216">All connected remote printers</span></span><br/>                                                          |
| <span data-ttu-id="6c08b-217">\_red enum de impresora \_</span><span class="sxs-lookup"><span data-stu-id="6c08b-217">PRINTER\_ENUM\_NETWORK</span></span>                             | <span data-ttu-id="6c08b-218">Se omite el parámetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="6c08b-218">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="6c08b-219">Todas las impresoras del dominio del equipo</span><span class="sxs-lookup"><span data-stu-id="6c08b-219">All printers in the computer's domain</span></span><br/>                                                  |
| <span data-ttu-id="6c08b-220">\_enumeración de impresora \_ remota</span><span class="sxs-lookup"><span data-stu-id="6c08b-220">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="6c08b-221">Una cadena vacía, ""</span><span class="sxs-lookup"><span data-stu-id="6c08b-221">An empty string, ""</span></span><br/>              | <span data-ttu-id="6c08b-222">Todas las impresoras y servidores de impresión en el dominio del equipo</span><span class="sxs-lookup"><span data-stu-id="6c08b-222">All printers and print servers in the computer's domain</span></span><br/>                                |
| <span data-ttu-id="6c08b-223">\_enumeración de impresora \_ remota</span><span class="sxs-lookup"><span data-stu-id="6c08b-223">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="6c08b-224">"Proveedor de impresión"</span><span class="sxs-lookup"><span data-stu-id="6c08b-224">"Print Provider"</span></span><br/>                 | <span data-ttu-id="6c08b-225">Igual que \_ el nombre de la enumeración de impresora \_</span><span class="sxs-lookup"><span data-stu-id="6c08b-225">Same as PRINTER\_ENUM\_NAME</span></span><br/>                                                            |
| <span data-ttu-id="6c08b-226">\_enumeración de impresora \_ remota</span><span class="sxs-lookup"><span data-stu-id="6c08b-226">PRINTER\_ENUM\_REMOTE</span></span>                              | <span data-ttu-id="6c08b-227">"Proveedor de impresión! Dominio</span><span class="sxs-lookup"><span data-stu-id="6c08b-227">"Print Provider!Domain"</span></span><br/>          | <span data-ttu-id="6c08b-228">Todas las impresoras y servidores de impresión del dominio del equipo, independientemente del *dominio* especificado.</span><span class="sxs-lookup"><span data-stu-id="6c08b-228">All printers and print servers in computer's domain, regardless of *Domain* specified.</span></span><br/> |
| <span data-ttu-id="6c08b-229">\_Categoría de enumeración de impresora \_ \_ 3D</span><span class="sxs-lookup"><span data-stu-id="6c08b-229">PRINTER\_ENUM\_CATEGORY\_3D</span></span>                        | <span data-ttu-id="6c08b-230">Se omite el parámetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="6c08b-230">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="6c08b-231">Solo se enumeran las impresoras 3D.</span><span class="sxs-lookup"><span data-stu-id="6c08b-231">Only 3D printers are enumerated.</span></span><br/>                                                       |
| <span data-ttu-id="6c08b-232">Categoría de enum de impresora \_ \_ \_ All</span><span class="sxs-lookup"><span data-stu-id="6c08b-232">PRINTER\_ENUM\_CATEGORY\_ALL</span></span>                       | <span data-ttu-id="6c08b-233">Se omite el parámetro *Name* .</span><span class="sxs-lookup"><span data-stu-id="6c08b-233">The *Name* parameter is ignored.</span></span><br/> | <span data-ttu-id="6c08b-234">las impresoras 3D se enumeran, junto con todas las demás impresoras.</span><span class="sxs-lookup"><span data-stu-id="6c08b-234">3D printers are enumerated, along with all other printers.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="6c08b-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c08b-235">Requirements</span></span>



| <span data-ttu-id="6c08b-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c08b-236">Requirement</span></span> | <span data-ttu-id="6c08b-237">Value</span><span class="sxs-lookup"><span data-stu-id="6c08b-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c08b-238">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c08b-238">Minimum supported client</span></span><br/> | <span data-ttu-id="6c08b-239">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6c08b-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6c08b-240">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c08b-240">Minimum supported server</span></span><br/> | <span data-ttu-id="6c08b-241">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c08b-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6c08b-242">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c08b-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c08b-243"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c08b-243"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6c08b-244">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c08b-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c08b-245"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c08b-245"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6c08b-246">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c08b-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c08b-247"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6c08b-247"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6c08b-248">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="6c08b-248">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6c08b-249">**EnumPrintersW** (Unicode) y **EnumPrintersA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6c08b-249">**EnumPrintersW** (Unicode) and **EnumPrintersA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="6c08b-250">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c08b-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c08b-251">Impresión</span><span class="sxs-lookup"><span data-stu-id="6c08b-251">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6c08b-252">Funciones de la API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="6c08b-252">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6c08b-253">**AddPrinter (**</span><span class="sxs-lookup"><span data-stu-id="6c08b-253">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="6c08b-254">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="6c08b-254">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="6c08b-255">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="6c08b-255">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="6c08b-256">**Información de la impresora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6c08b-256">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="6c08b-257">**Información de la impresora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6c08b-257">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="6c08b-258">**Información de la impresora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="6c08b-258">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="6c08b-259">**Información de la impresora \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="6c08b-259">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> <dt>

[<span data-ttu-id="6c08b-260">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="6c08b-260">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

