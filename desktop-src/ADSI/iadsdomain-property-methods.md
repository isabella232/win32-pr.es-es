---
title: Métodos de la propiedad IADsDomain (iAds. h)
description: Los métodos de la interfaz IADsDomain leen y escriben las propiedades descritas en este tema. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: ff2c4cbc-a8d5-4db5-85d4-da3367f27fa0
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsDomain ADSI
topic_type:
- apiref
api_name:
- IADsDomain Property Methods
- IADsDomain.AutoUnlockInterval
- IADsDomain.get_AutoUnlockInterval
- IADsDomain.put_AutoUnlockInterval
- IADsDomain.IsWorkgroup
- IADsDomain.get_IsWorkgroup
- IADsDomain.LockoutObservationInterval
- IADsDomain.get_LockoutObservationInterval
- IADsDomain.put_LockoutObservationInterval
- IADsDomain.MinPasswordAge
- IADsDomain.get_MinPasswordAge
- IADsDomain.put_MinPasswordAge
- IADsDomain.MinPasswordLength
- IADsDomain.get_MinPasswordLength
- IADsDomain.put_MinPasswordLength
- IADsDomain.MaxBadPasswordsAllowed
- IADsDomain.get_MaxBadPasswordsAllowed
- IADsDomain.put_MaxBadPasswordsAllowed
- IADsDomain.MaxPasswordAge
- IADsDomain.get_MaxPasswordAge
- IADsDomain.put_MaxPasswordAge
- IADsDomain.PasswordAttributes
- IADsDomain.get_PasswordAttributes
- IADsDomain.put_PasswordAttributes
- IADsDomain.PasswordHistoryLength
- IADsDomain.get_PasswordHistoryLength
- IADsDomain.put_PasswordHistoryLength
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a10c6377c7e97f83046f60d46312a03db68cadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996836"
---
# <a name="iadsdomain-property-methods"></a><span data-ttu-id="105ed-105">Métodos de propiedad IADsDomain</span><span class="sxs-lookup"><span data-stu-id="105ed-105">IADsDomain Property Methods</span></span>

<span data-ttu-id="105ed-106">Los métodos de la interfaz [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) leen y escriben las propiedades descritas en este tema.</span><span class="sxs-lookup"><span data-stu-id="105ed-106">The [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="105ed-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="105ed-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="105ed-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="105ed-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="105ed-109">**AutoUnlockInterval**</span><span class="sxs-lookup"><span data-stu-id="105ed-109">**AutoUnlockInterval**</span></span>
<span data-ttu-id="105ed-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="105ed-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="105ed-111">Indica el tiempo mínimo que debe transcurrir antes de que la cuenta se rehabilite automáticamente.</span><span class="sxs-lookup"><span data-stu-id="105ed-111">Indicates the minimum time that must elapse before the account is automatically reenabled.</span></span>

<dt>

<span data-ttu-id="105ed-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="105ed-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="105ed-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="105ed-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AutoUnlockInterval(
  [out] LONG* plAutoUnlockInterval
);
HRESULT put_AutoUnlockInterval(
  [in] LONG lAutoUnlockInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="105ed-114">**IsWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="105ed-114">**IsWorkgroup**</span></span>
<span data-ttu-id="105ed-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="105ed-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="105ed-116">Esta propiedad ya no se implementa.</span><span class="sxs-lookup"><span data-stu-id="105ed-116">This property is no longer implemented.</span></span>

<dt>

<span data-ttu-id="105ed-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="105ed-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="105ed-118">Tipo de datos de scripting: **variante \_ bool**</span><span class="sxs-lookup"><span data-stu-id="105ed-118">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsWorkgroup(
  [out] VARIANT_BOOL* retval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="105ed-119">**LockoutObservationInterval**</span><span class="sxs-lookup"><span data-stu-id="105ed-119">**LockoutObservationInterval**</span></span>
<span data-ttu-id="105ed-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="105ed-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="105ed-121">Indica el período de tiempo durante el cual el recuento de contraseñas no válidas se supervisa y acumula antes de determinar si es necesario bloquear la cuenta. Por ejemplo, si el número de intentos de contraseña incorrecta en una cuenta supera el umbral (número máximo de contraseñas no válidas permitidas) durante el período de tiempo especificado (intervalo de observación de bloqueo), la cuenta se bloqueará estableciendo la propiedad adecuada en el conjunto de propiedades de parámetro login.</span><span class="sxs-lookup"><span data-stu-id="105ed-121">Indicates the time window during which the bad password count is monitored and accumulated before determining whether the account needs to be locked out. For example, if the number of bad password attempts on an account exceed the threshold (Maximum Bad Passwords Allowed) during the specified time period (Lockout Observation Interval) the account will be locked out by setting the appropriate property in the Login Parameter property set.</span></span>

<dt>

<span data-ttu-id="105ed-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="105ed-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="105ed-123">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="105ed-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockoutObservationInterval(
  [out] LONG* plLockoutObservationInterval
);
HRESULT put_LockoutObservationInterval(
  [in] LONG lLockoutObservationInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="105ed-124">**MaxBadPasswordsAllowed**</span><span class="sxs-lookup"><span data-stu-id="105ed-124">**MaxBadPasswordsAllowed**</span></span>
<span data-ttu-id="105ed-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="105ed-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="105ed-126">Indica el número máximo de inicios de sesión de contraseñas no válidos permitidos antes de que se bloquee la cuenta.</span><span class="sxs-lookup"><span data-stu-id="105ed-126">Indicates the maximum number of bad password logins allowed before an account lockout.</span></span>

<dt>

<span data-ttu-id="105ed-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="105ed-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="105ed-128">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="105ed-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxBadPasswordsAllowed(
  [out] LONG* plMaxBadPasswordsAllowed
);
HRESULT put_MaxBadPasswordsAllowed(
  [in] LONG lMaxBadPasswordsAllowed
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="105ed-129">**MaxPasswordAge**</span><span class="sxs-lookup"><span data-stu-id="105ed-129">**MaxPasswordAge**</span></span>
<span data-ttu-id="105ed-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="105ed-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="105ed-131">Indica el intervalo de tiempo máximo, en segundos, tras el cual el usuario debe cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="105ed-131">Indicates the maximum time interval, in seconds, after which the password must be changed by the user.</span></span>

<dt>

<span data-ttu-id="105ed-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="105ed-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="105ed-133">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="105ed-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxPasswordAge(
  [out] LONG* plMaxPasswordAge
);
RESULT put_MaxPasswordAge(
  [in] LONG lMaxPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="105ed-134">**MinPasswordAge**</span><span class="sxs-lookup"><span data-stu-id="105ed-134">**MinPasswordAge**</span></span>
<span data-ttu-id="105ed-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="105ed-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="105ed-136">Indica el intervalo de tiempo mínimo, en segundos, antes de que se pueda cambiar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="105ed-136">Indicates the minimum time interval, in seconds, before the password can be changed.</span></span>

<dt>

<span data-ttu-id="105ed-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="105ed-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="105ed-138">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="105ed-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordAge(
  [out] LONG* plMinPasswordAge
);
HRESULT put_MinPasswordAge(
  [in] LONG lMinPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="105ed-139">**MinPasswordLength**</span><span class="sxs-lookup"><span data-stu-id="105ed-139">**MinPasswordLength**</span></span>
<span data-ttu-id="105ed-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="105ed-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="105ed-141">Indica el número mínimo de caracteres que se deben usar para una contraseña.</span><span class="sxs-lookup"><span data-stu-id="105ed-141">Indicates the minimum number of characters that must be used for a password.</span></span>

<dt>

<span data-ttu-id="105ed-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="105ed-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="105ed-143">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="105ed-143">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordLength(
  [out] LONG* plMinPasswordLength
);
HRESULT put_MinPasswordLength(
  [in] LONG lMinPasswordLength
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="105ed-144">**PasswordAttributes**</span><span class="sxs-lookup"><span data-stu-id="105ed-144">**PasswordAttributes**</span></span>
<span data-ttu-id="105ed-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="105ed-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="105ed-146">Indica las restricciones en las contraseñas, tal y como se define en la siguiente lista de atributos y valores.</span><span class="sxs-lookup"><span data-stu-id="105ed-146">Indicates restrictions on passwords, as defined by the following list of attributes and values.</span></span>

> [!Note]  
> <span data-ttu-id="105ed-147">En el caso de \_ los atributos de contraseña \_ complejos, la contraseña debe incluir al menos un signo de puntuación o un carácter no imprimible.</span><span class="sxs-lookup"><span data-stu-id="105ed-147">For PASSWORD\_ATTR\_COMPLEX, the password must include at least one punctuation mark or non-printable character.</span></span>

 

<dt>

<span id="PASSWORD_ATTR_NONE"></span><span id="password_attr_none"></span>

<span data-ttu-id="105ed-148">**Contraseña \_ de ATTR \_ ninguno** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="105ed-148">**PASSWORD\_ATTR\_NONE** (0x00000000)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_MIXED_CASE"></span><span id="password_attr_mixed_case"></span>

<span data-ttu-id="105ed-149">**Contraseña \_ de \_ \_ Caso mezclado de ATTR** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="105ed-149">**PASSWORD\_ATTR\_MIXED\_CASE** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_COMPLEX"></span><span id="password_attr_complex"></span>

<span data-ttu-id="105ed-150">**Contraseña \_ de ATTR \_ Complex** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="105ed-150">**PASSWORD\_ATTR\_COMPLEX** (0x00000002)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="105ed-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="105ed-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="105ed-152">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="105ed-152">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordAttributes(
  [out] LONG* plPasswordAttributes
);
HRESULT put_PasswordAttributes(
  [in] LONG lPasswordAttributes
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="105ed-153">**PasswordHistoryLength**</span><span class="sxs-lookup"><span data-stu-id="105ed-153">**PasswordHistoryLength**</span></span>
<span data-ttu-id="105ed-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="105ed-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="105ed-155">Indica el número de contraseñas anteriores guardadas en la lista de historial.</span><span class="sxs-lookup"><span data-stu-id="105ed-155">Indicates the number of previous passwords saved in the history list.</span></span> <span data-ttu-id="105ed-156">El usuario no puede volver a usar una contraseña en la lista de historial.</span><span class="sxs-lookup"><span data-stu-id="105ed-156">The user cannot reuse a password in the history list.</span></span>

<dt>

<span data-ttu-id="105ed-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="105ed-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="105ed-158">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="105ed-158">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordHistoryLength(
  [out] LONG* plPasswordHistoryLength
);
HRESULT put_PasswordHistoryLength(
  [in] LONG lPasswordHistoryLength
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="105ed-159">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="105ed-159">Examples</span></span>

<span data-ttu-id="105ed-160">En el ejemplo de código siguiente se muestra el valor de la propiedad **PasswordHistoryLength** .</span><span class="sxs-lookup"><span data-stu-id="105ed-160">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```VB
Dim dom As IADsDomain
On Error Resume Next

Set dom = GetObject("WinNT://myDomain")

debug.print "PasswordHistoryLength" & dom.PasswordHistoryLength
```



<span data-ttu-id="105ed-161">En el ejemplo de código siguiente se muestra el valor de la propiedad **PasswordHistoryLength** .</span><span class="sxs-lookup"><span data-stu-id="105ed-161">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```C++
LPWSTR adsPath = L"WinNT://myDomain";
LONG nPasswordHistoryLength = 0;

// Bind to the domain object.
hr = ADsGetObject(adsPath,IID_IADsDomain,(void**)&pDomain);
if(FAILED(hr)) {goto Cleanup;}

hr = pDomain->get_PasswordHistoryLength(&nPasswordHistoryLength);
if(FAILED(hr)) {goto Cleanup;}
printf("Password history length: %d",nPasswordHistoryLength);

Cleanup:
    if(pDomain) pDomain->Release();
```



## <a name="requirements"></a><span data-ttu-id="105ed-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="105ed-162">Requirements</span></span>



| <span data-ttu-id="105ed-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="105ed-163">Requirement</span></span> | <span data-ttu-id="105ed-164">Value</span><span class="sxs-lookup"><span data-stu-id="105ed-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="105ed-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="105ed-165">Minimum supported client</span></span><br/> | <span data-ttu-id="105ed-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="105ed-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="105ed-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="105ed-167">Minimum supported server</span></span><br/> | <span data-ttu-id="105ed-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="105ed-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="105ed-169">Encabezado</span><span class="sxs-lookup"><span data-stu-id="105ed-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="105ed-170"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="105ed-170"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="105ed-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="105ed-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="105ed-172"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="105ed-172"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="105ed-173">IID</span><span class="sxs-lookup"><span data-stu-id="105ed-173">IID</span></span><br/>                      | <span data-ttu-id="105ed-174">IID \_ IADsDomain se define como 00E4C220-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="105ed-174">IID\_IADsDomain is defined as 00E4C220-FD16-11CE-ABC4-02608C9E7553</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="105ed-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="105ed-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="105ed-176">**IADsDomain**</span><span class="sxs-lookup"><span data-stu-id="105ed-176">**IADsDomain**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdomain)
</dt> <dt>

[<span data-ttu-id="105ed-177">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="105ed-177">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





