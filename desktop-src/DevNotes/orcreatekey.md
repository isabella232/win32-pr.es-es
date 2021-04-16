---
description: Crea la clave del registro especificada en un subárbol del registro sin conexión. Si la clave ya existe, la función la abre.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Función ORCreateKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671489"
---
# <a name="orcreatekey-function"></a><span data-ttu-id="18d1f-104">ORCreateKey función)</span><span class="sxs-lookup"><span data-stu-id="18d1f-104">ORCreateKey function</span></span>

<span data-ttu-id="18d1f-105">Crea la clave del registro especificada en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="18d1f-105">Creates the specified registry key in an offline registry hive.</span></span> <span data-ttu-id="18d1f-106">Si la clave ya existe, la función la abre.</span><span class="sxs-lookup"><span data-stu-id="18d1f-106">If the key already exists, the function opens it.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d1f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18d1f-107">Syntax</span></span>


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a><span data-ttu-id="18d1f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18d1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18d1f-109">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="18d1f-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18d1f-110">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="18d1f-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="18d1f-111">*lpSubKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18d1f-111">*lpSubKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18d1f-112">Puntero a una cadena Unicode que contiene el nombre de una subclave que esta función abre o crea.</span><span class="sxs-lookup"><span data-stu-id="18d1f-112">A pointer to a Unicode string that contains the name of a subkey that this function opens or creates.</span></span> <span data-ttu-id="18d1f-113">El parámetro *lpSubKey* debe especificar una subclave de la clave identificada por el parámetro *Handle* . puede tener hasta 32 niveles de profundidad en el árbol del registro.</span><span class="sxs-lookup"><span data-stu-id="18d1f-113">The *lpSubKey* parameter must specify a subkey of the key identified by the *Handle* parameter; it can be up to 32 levels deep in the registry tree.</span></span> <span data-ttu-id="18d1f-114">Para obtener más información sobre los nombres de clave, vea [estructura del registro](../sysinfo/structure-of-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="18d1f-114">For more information about key names, see [Structure of the Registry](../sysinfo/structure-of-the-registry.md).</span></span>

<span data-ttu-id="18d1f-115">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="18d1f-115">This parameter cannot be **NULL**.</span></span>

<span data-ttu-id="18d1f-116">Los nombres de clave no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="18d1f-116">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="18d1f-117">*lpClass* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="18d1f-117">*lpClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18d1f-118">La clase (tipo de objeto) de esta clave.</span><span class="sxs-lookup"><span data-stu-id="18d1f-118">The class (object type) of this key.</span></span> <span data-ttu-id="18d1f-119">Este parámetro se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="18d1f-119">This parameter may be ignored.</span></span> <span data-ttu-id="18d1f-120">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="18d1f-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="18d1f-121">*dwOptions* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="18d1f-121">*dwOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18d1f-122">Este parámetro puede ser 0 o uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="18d1f-122">This parameter can be 0 or one of the following values.</span></span>



| <span data-ttu-id="18d1f-123">Value</span><span class="sxs-lookup"><span data-stu-id="18d1f-123">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="18d1f-124">Significado</span><span class="sxs-lookup"><span data-stu-id="18d1f-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <span data-ttu-id="18d1f-125"><dt>**Reg \_ . OPCIÓN de \_ creación de \_ vínculo**</dt> <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="18d1f-125"><dt>**REG\_OPTION\_CREATE\_LINK**</dt> <dt>0x00000002L</dt></span></span> </dl>    | <span data-ttu-id="18d1f-126">La clave es un vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="18d1f-126">The key is a symbolic link.</span></span> <span data-ttu-id="18d1f-127">La ruta de acceso de destino se asigna al valor de L "SymbolicLinkValue" de la clave.</span><span class="sxs-lookup"><span data-stu-id="18d1f-127">The target path is assigned to the L"SymbolicLinkValue" value of the key.</span></span> <span data-ttu-id="18d1f-128">La ruta de acceso de destino debe ser una ruta de acceso absoluta del registro.</span><span class="sxs-lookup"><span data-stu-id="18d1f-128">The target path must be an absolute registry path.</span></span> <span data-ttu-id="18d1f-129">Si se establece esta opción, también se debe establecer la **opción de reg \_ \_ no \_ volátil** .</span><span class="sxs-lookup"><span data-stu-id="18d1f-129">If this option is set, **REG\_OPTION\_NON\_VOLATILE** must also be set.</span></span> <br/> <span data-ttu-id="18d1f-130">Si el parámetro *lpSubKey* especifica una clave existente, se debe haber creado con la **\_ opción reg \_ Create \_ Link**.</span><span class="sxs-lookup"><span data-stu-id="18d1f-130">If the *lpSubKey* parameter specifies an existing key, it must have been created with **REG\_OPTION\_CREATE\_LINK**.</span></span><br/> <span data-ttu-id="18d1f-131">Los vínculos simbólicos del registro solo deben usarse cuando sea absolutamente necesario para la compatibilidad de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="18d1f-131">Registry symbolic links should be used only when absolutely necessary for application compatibility.</span></span> <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <span data-ttu-id="18d1f-132"><dt>**Reg \_ . OPCIÓN \_ 0x00000000L no \_ volátil**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="18d1f-132"><dt>**REG\_OPTION\_NON\_VOLATILE**</dt> <dt>0x00000000L</dt></span></span> </dl> | <span data-ttu-id="18d1f-133">La clave no es volátil; Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="18d1f-133">The key is not volatile; this is the default.</span></span> <span data-ttu-id="18d1f-134">La información se almacena en un archivo y se conserva cuando se reinicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="18d1f-134">The information is stored in a file and is preserved when the system is restarted.</span></span> <span data-ttu-id="18d1f-135">La función [**ORSaveHive**](orsavehive.md) guarda las claves que no son volátiles.</span><span class="sxs-lookup"><span data-stu-id="18d1f-135">The [**ORSaveHive**](orsavehive.md) function saves keys that are not volatile.</span></span><br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="18d1f-136">*pSecurityDescriptor* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="18d1f-136">*pSecurityDescriptor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18d1f-137">Puntero a una estructura [de \_ descriptores de seguridad](/windows/win32/api/winnt/ns-winnt-security_descriptor) que contiene un descriptor de seguridad para la nueva clave.</span><span class="sxs-lookup"><span data-stu-id="18d1f-137">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that contains a security descriptor for the new key.</span></span> <span data-ttu-id="18d1f-138">Si *pSecurityDescriptor* es **null**, la clave obtiene un descriptor de seguridad predeterminado.</span><span class="sxs-lookup"><span data-stu-id="18d1f-138">If *pSecurityDescriptor* is **NULL**, the key gets a default security descriptor.</span></span> <span data-ttu-id="18d1f-139">Las ACL de un descriptor de seguridad predeterminado para una clave se heredan de su clave primaria directa.</span><span class="sxs-lookup"><span data-stu-id="18d1f-139">The ACLs in a default security descriptor for a key are inherited from its direct parent key.</span></span>

</dd> <dt>

<span data-ttu-id="18d1f-140">*phkResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="18d1f-140">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18d1f-141">Puntero a una variable que recibe un identificador de la clave abierta o creada.</span><span class="sxs-lookup"><span data-stu-id="18d1f-141">A pointer to a variable that receives a handle to the opened or created key.</span></span> <span data-ttu-id="18d1f-142">Utilice la función [**ORCloseKey**](orclosekey.md) para cerrar la clave después de haber terminado de usar el identificador.</span><span class="sxs-lookup"><span data-stu-id="18d1f-142">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> <dt>

<span data-ttu-id="18d1f-143">*pdwDisposition* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="18d1f-143">*pdwDisposition* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18d1f-144">Puntero a una variable que recibe uno de los siguientes valores de disposición.</span><span class="sxs-lookup"><span data-stu-id="18d1f-144">A pointer to a variable that receives one of the following disposition values.</span></span>



| <span data-ttu-id="18d1f-145">Value</span><span class="sxs-lookup"><span data-stu-id="18d1f-145">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="18d1f-146">Significado</span><span class="sxs-lookup"><span data-stu-id="18d1f-146">Meaning</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <span data-ttu-id="18d1f-147"><dt>**Reg \_ . Se creó la \_ nueva \_ clave**</dt> <dt>0x00000001L</dt></span><span class="sxs-lookup"><span data-stu-id="18d1f-147"><dt>**REG\_CREATED\_NEW\_KEY**</dt> <dt>0x00000001L</dt></span></span> </dl>             | <span data-ttu-id="18d1f-148">La clave no existía y se creó.</span><span class="sxs-lookup"><span data-stu-id="18d1f-148">The key did not exist and was created.</span></span><br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <span data-ttu-id="18d1f-149"><dt>**Reg \_ . Se abrió la \_ \_ clave existente**</dt> <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="18d1f-149"><dt>**REG\_OPENED\_EXISTING\_KEY**</dt> <dt>0x00000002L</dt></span></span> </dl> | <span data-ttu-id="18d1f-150">La clave existía y se abrió simplemente sin cambiarse.</span><span class="sxs-lookup"><span data-stu-id="18d1f-150">The key existed and was simply opened without being changed.</span></span><br/> |



 

<span data-ttu-id="18d1f-151">Si *pdwDisposition* es **null**, no se devuelve ninguna información de disposición.</span><span class="sxs-lookup"><span data-stu-id="18d1f-151">If *pdwDisposition* is **NULL**, no disposition information is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18d1f-152">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18d1f-152">Return value</span></span>

<span data-ttu-id="18d1f-153">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="18d1f-153">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="18d1f-154">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="18d1f-154">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="18d1f-155">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="18d1f-155">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="18d1f-156">Si el parámetro *dwOptions* está establecido con **la \_ opción reg \_ Create \_ Link** , pero la **opción reg \_ \_ no \_ volatile** está clara o si el identificador que se va a devolver es un identificador de la clave raíz del subárbol, la función devuelve un parámetro de error \_ no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="18d1f-156">If the *dwOptions* parameter is set with **REG\_OPTION\_CREATE\_LINK** but **REG\_OPTION\_NON\_VOLATILE** is clear, or if the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="18d1f-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18d1f-157">Remarks</span></span>

<span data-ttu-id="18d1f-158">La clave que crea la función **ORCreateKey** no tiene valores.</span><span class="sxs-lookup"><span data-stu-id="18d1f-158">The key that the **ORCreateKey** function creates has no values.</span></span> <span data-ttu-id="18d1f-159">Una aplicación puede usar la función [**ORSetValue**](orsetvalue.md) para establecer los valores de clave.</span><span class="sxs-lookup"><span data-stu-id="18d1f-159">An application can use the [**ORSetValue**](orsetvalue.md) function to set key values.</span></span>

<span data-ttu-id="18d1f-160">No se puede usar la función **ORCreateKey** para crear la clave raíz en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="18d1f-160">The **ORCreateKey** function cannot be used to create the root key in an offline registry hive.</span></span> <span data-ttu-id="18d1f-161">Utilice la función [**ORCreateHive**](orcreatehive.md) para crear la clave raíz y obtener un identificador para la clave.</span><span class="sxs-lookup"><span data-stu-id="18d1f-161">Use the [**ORCreateHive**](orcreatehive.md) function to create the root key and obtain a handle to the key.</span></span>

<span data-ttu-id="18d1f-162">El registro sin conexión no admite el guardado de claves individuales.</span><span class="sxs-lookup"><span data-stu-id="18d1f-162">The offline registry does not support saving individual keys.</span></span> <span data-ttu-id="18d1f-163">Use la función [**ORSaveHive**](orsavehive.md) para guardar una clave y sus subclaves en un subárbol.</span><span class="sxs-lookup"><span data-stu-id="18d1f-163">Use the [**ORSaveHive**](orsavehive.md) function to save a key and its subkeys in a hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="18d1f-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18d1f-164">Requirements</span></span>



| <span data-ttu-id="18d1f-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="18d1f-165">Requirement</span></span> | <span data-ttu-id="18d1f-166">Value</span><span class="sxs-lookup"><span data-stu-id="18d1f-166">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18d1f-167">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="18d1f-167">Redistributable</span></span><br/> | <span data-ttu-id="18d1f-168">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="18d1f-168">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="18d1f-169">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18d1f-169">Header</span></span><br/>          | <dl> <span data-ttu-id="18d1f-170"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="18d1f-170"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="18d1f-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18d1f-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="18d1f-172"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18d1f-172"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18d1f-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="18d1f-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d1f-174">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="18d1f-174">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="18d1f-175">**ORCreateHive**</span><span class="sxs-lookup"><span data-stu-id="18d1f-175">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="18d1f-176">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="18d1f-176">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="18d1f-177">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="18d1f-177">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="18d1f-178">descriptor de seguridad \_</span><span class="sxs-lookup"><span data-stu-id="18d1f-178">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
