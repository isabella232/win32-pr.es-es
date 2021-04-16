---
description: Recupera las marcas virtuales de la clave del registro abierta especificada en un subárbol del registro sin conexión.
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: Función ORGetVirtualFlags (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 36c41bb9e510a107689790162e03e3bb86c8de1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649919"
---
# <a name="orgetvirtualflags-function"></a><span data-ttu-id="8925e-103">ORGetVirtualFlags función)</span><span class="sxs-lookup"><span data-stu-id="8925e-103">ORGetVirtualFlags function</span></span>

<span data-ttu-id="8925e-104">Recupera las marcas virtuales de la clave del registro abierta especificada en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8925e-104">Retrieves the virtual flags on the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="8925e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8925e-105">Syntax</span></span>


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8925e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8925e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8925e-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8925e-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8925e-108">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8925e-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="8925e-109">*pdwFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8925e-109">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8925e-110">Un puntero a una variable para recibir las marcas de virtualización establecidas para la clave.</span><span class="sxs-lookup"><span data-stu-id="8925e-110">A pointer to a variable to receive the virtualization flags set for the key.</span></span> <span data-ttu-id="8925e-111">Una vez que la función devuelve un valor, este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8925e-111">After the function returns, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="8925e-112">Value</span><span class="sxs-lookup"><span data-stu-id="8925e-112">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="8925e-113">Significado</span><span class="sxs-lookup"><span data-stu-id="8925e-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <span data-ttu-id="8925e-114"><dt>**Reg \_ . \_Error de \_ clave \_ no silenciosa**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8925e-114"><dt>**REG\_KEY\_DONT\_SILENT\_FAIL**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="8925e-115">Si se establece esta marca y se produce un error en una operación de apertura en una clave que tiene habilitada la virtualización, el registro no intenta volver a abrir la clave.</span><span class="sxs-lookup"><span data-stu-id="8925e-115">If this flag is set and an Open operation fails on a key that has virtualization enabled, the registry does not attempt to reopen the key.</span></span> <span data-ttu-id="8925e-116">Si esta marca está desactivada, el registro intenta volver a abrir la clave con el \_ acceso máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="8925e-116">If this flag is clear, the registry attempts to reopen the key with MAXIMUM\_ALLOWED access.</span></span><br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <span data-ttu-id="8925e-117"><dt>**Reg \_ . CLAVE \_ no \_ virtualizar**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8925e-117"><dt>**REG\_KEY\_DONT\_VIRTUALIZE**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="8925e-118">Si se establece esta marca y se produce un error en una operación de creación de clave porque el autor de la llamada no tiene el \_ derecho de creación \_ de clave \_ en la clave primaria, el registro produce un error en la operación de creación.</span><span class="sxs-lookup"><span data-stu-id="8925e-118">If this flag is set and a Create Key operation fails because the caller does not have the KEY\_CREATE\_SUB\_KEY right on the parent key, the registry fails the Create operation.</span></span> <span data-ttu-id="8925e-119">Si esta marca está desactivada, el registro intenta crear la clave en el almacén virtual.</span><span class="sxs-lookup"><span data-stu-id="8925e-119">If this flag is clear, the registry attempts to create the key in the virtual store.</span></span> <span data-ttu-id="8925e-120">El autor de la llamada debe tener el \_ derecho de lectura de la clave en la clave primaria.</span><span class="sxs-lookup"><span data-stu-id="8925e-120">The caller must have the KEY\_READ right on the parent key.</span></span><br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <span data-ttu-id="8925e-121"><dt>**Reg \_ . \_ \_ Marca de recursividad de clave**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="8925e-121"><dt>**REG\_KEY\_RECURSE\_FLAG**</dt> <dt>8</dt></span></span> </dl>              | <span data-ttu-id="8925e-122">Si se establece esta marca, las marcas de virtualización del registro se propagan desde la clave primaria.</span><span class="sxs-lookup"><span data-stu-id="8925e-122">If this flag is set, registry virtualization flags are propagated from the parent key.</span></span> <span data-ttu-id="8925e-123">Si esta marca está desactivada, las marcas de virtualización del registro no se propagan.</span><span class="sxs-lookup"><span data-stu-id="8925e-123">If this flag is clear, registry virtualization flags are not propagated.</span></span><br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8925e-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8925e-124">Return value</span></span>

<span data-ttu-id="8925e-125">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8925e-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="8925e-126">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="8925e-126">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="8925e-127">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="8925e-127">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8925e-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8925e-128">Remarks</span></span>

<span data-ttu-id="8925e-129">La virtualización del registro es una tecnología de compatibilidad de aplicaciones provisional que permite realizar operaciones de escritura en el registro que tienen un impacto global en las ubicaciones por usuario.</span><span class="sxs-lookup"><span data-stu-id="8925e-129">Registry virtualization is an interim application compatibility technology that enables registry write operations that have global impact to be redirected to per-user locations.</span></span> <span data-ttu-id="8925e-130">Esta redirección es transparente para las aplicaciones que leen o escriben en el registro.</span><span class="sxs-lookup"><span data-stu-id="8925e-130">This redirection is transparent to applications reading from or writing to the registry.</span></span>

<span data-ttu-id="8925e-131">La virtualización del registro se admite a partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8925e-131">Registry virtualization is supported starting with Windows Vista.</span></span> <span data-ttu-id="8925e-132">Sin embargo, Microsoft pretende quitarlo de versiones futuras del sistema operativo Windows a medida que se realizan más aplicaciones compatibles con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8925e-132">However, Microsoft intends to remove it from future versions of the Windows operating system as more applications are made compatible with Windows Vista.</span></span> <span data-ttu-id="8925e-133">Por lo tanto, las aplicaciones no deben depender del comportamiento de la virtualización del registro en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8925e-133">Therefore, applications should not depend on the behavior of registry virtualization in the system.</span></span>

<span data-ttu-id="8925e-134">La virtualización del registro solo está habilitada para lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8925e-134">Registry virtualization is enabled only for the following:</span></span>

-   <span data-ttu-id="8925e-135">procesos interactivos de 32 bits</span><span class="sxs-lookup"><span data-stu-id="8925e-135">32-bit interactive processes</span></span>
-   <span data-ttu-id="8925e-136">Claves en **el \_ \_ \\ software de máquina local HKEY**</span><span class="sxs-lookup"><span data-stu-id="8925e-136">Keys in **HKEY\_LOCAL\_MACHINE\\Software**</span></span>
-   <span data-ttu-id="8925e-137">Claves en las que un administrador puede escribir</span><span class="sxs-lookup"><span data-stu-id="8925e-137">Keys that an administrator can write to</span></span>

<span data-ttu-id="8925e-138">Para obtener más información, consulte [virtualización del registro](../sysinfo/registry-virtualization.md).</span><span class="sxs-lookup"><span data-stu-id="8925e-138">For more information, see [Registry Virtualization](../sysinfo/registry-virtualization.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8925e-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8925e-139">Requirements</span></span>



| <span data-ttu-id="8925e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8925e-140">Requirement</span></span> | <span data-ttu-id="8925e-141">Value</span><span class="sxs-lookup"><span data-stu-id="8925e-141">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8925e-142">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="8925e-142">Redistributable</span></span><br/> | <span data-ttu-id="8925e-143">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8925e-143">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="8925e-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8925e-144">Header</span></span><br/>          | <dl> <span data-ttu-id="8925e-145"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8925e-145"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="8925e-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8925e-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="8925e-147"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8925e-147"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8925e-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="8925e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8925e-149">**ORSetVirtualFlags**</span><span class="sxs-lookup"><span data-stu-id="8925e-149">**ORSetVirtualFlags**</span></span>](orsetvirtualflags.md)
</dt> <dt>

[<span data-ttu-id="8925e-150">Virtualización del registro</span><span class="sxs-lookup"><span data-stu-id="8925e-150">Registry Virtualization</span></span>](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
