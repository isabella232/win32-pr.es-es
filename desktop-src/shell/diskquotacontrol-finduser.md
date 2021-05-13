---
description: Busca la entrada de un usuario, por nombre, en el archivo de cuota del volumen.
title: Método DiskQuotaControl.FindUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: eab539a5ec5a360ae28fc87d5ffbb9dd4f9f1cc8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841526"
---
# <a name="diskquotacontrolfinduser-method"></a><span data-ttu-id="85602-103">Método DiskQuotaControl.FindUser</span><span class="sxs-lookup"><span data-stu-id="85602-103">DiskQuotaControl.FindUser method</span></span>

<span data-ttu-id="85602-104">Busca la entrada de un usuario, por nombre, en el archivo de cuota del volumen.</span><span class="sxs-lookup"><span data-stu-id="85602-104">Finds a user's entry, by name, in the volume's quota file.</span></span>

## <a name="syntax"></a><span data-ttu-id="85602-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85602-105">Syntax</span></span>


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="85602-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85602-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85602-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="85602-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="85602-108">Tipo: **Cadena**</span><span class="sxs-lookup"><span data-stu-id="85602-108">Type: **String**</span></span>

<span data-ttu-id="85602-109">Valor de cadena que contiene el nombre de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="85602-109">A string value that contains the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85602-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85602-110">Return value</span></span>

<span data-ttu-id="85602-111">Devuelve una expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser del**](didiskquotauser-object.md) usuario.</span><span class="sxs-lookup"><span data-stu-id="85602-111">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="85602-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85602-112">Remarks</span></span>

<span data-ttu-id="85602-113">Este método devuelve un [**objeto DIDiskQuotaUser**](didiskquotauser-object.md) incluso si no hay ninguna entrada para el usuario en el archivo de cuota.</span><span class="sxs-lookup"><span data-stu-id="85602-113">This method returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object even if there is no entry for the user in the quota file.</span></span> <span data-ttu-id="85602-114">El objeto de usuario devuelto tiene límites de umbral de advertencia y cuota fija establecidos en los valores predeterminados del volumen.</span><span class="sxs-lookup"><span data-stu-id="85602-114">The returned user object has warning threshold and hard quota limits set to the volume's default values.</span></span>

<span data-ttu-id="85602-115">La cadena devuelta por [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) se puede pasar en lugar del *parámetro sLogonName.*</span><span class="sxs-lookup"><span data-stu-id="85602-115">The string returned from [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) may be passed in place of the *sLogonName* parameter.</span></span> <span data-ttu-id="85602-116">Cuando **FindUser** recibe una cadena SID, usa el SID correspondiente para la búsqueda directa del registro de cuota del usuario en el volumen.</span><span class="sxs-lookup"><span data-stu-id="85602-116">When **FindUser** receives a SID string it uses the corresponding SID for direct lookup of the user's quota record on the volume.</span></span> <span data-ttu-id="85602-117">Esto omite la caché de nombres de SID.</span><span class="sxs-lookup"><span data-stu-id="85602-117">This bypasses the SID-name cache.</span></span> <span data-ttu-id="85602-118">En los casos en los que **FindUser** produce un error debido a una discrepancia de formato (por ejemplo, compatible con SAM y UPN) del nombre de inicio de sesión proporcionado y el nombre de inicio de sesión almacenado en caché, el nombre de inicio de sesión se puede traducir a una cadena SID mediante **TranslateLogonNameToSID** y, a continuación, pasar de nuevo a **FindUser**.</span><span class="sxs-lookup"><span data-stu-id="85602-118">In cases where **FindUser** fails due to a mismatch in format (for example, SAM-compatible and UPN) of the logon name provided and the logon name cached, the logon name can be translated to a SID string using **TranslateLogonNameToSID** then passed again to **FindUser**.</span></span> <span data-ttu-id="85602-119">El siguiente código VBScript ilustra esta técnica.</span><span class="sxs-lookup"><span data-stu-id="85602-119">The following VBScript code illustrates this technique.</span></span>


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



## <a name="requirements"></a><span data-ttu-id="85602-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85602-120">Requirements</span></span>



| <span data-ttu-id="85602-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="85602-121">Requirement</span></span> | <span data-ttu-id="85602-122">Value</span><span class="sxs-lookup"><span data-stu-id="85602-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85602-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85602-123">Minimum supported client</span></span><br/> | <span data-ttu-id="85602-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="85602-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85602-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85602-125">Minimum supported server</span></span><br/> | <span data-ttu-id="85602-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="85602-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="85602-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85602-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85602-128"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="85602-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85602-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="85602-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85602-130">**DiskQuotaControl (objeto)**</span><span class="sxs-lookup"><span data-stu-id="85602-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




