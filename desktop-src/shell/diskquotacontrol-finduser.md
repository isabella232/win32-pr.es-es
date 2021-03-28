---
description: Busca la entrada de un usuario, por nombre, en el archivo de cuota del volumen.
title: DiskQuotaControl. FindUser, método
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
ms.openlocfilehash: af1bc9c0398d37f04e47515a2b85cb4520795b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984254"
---
# <a name="diskquotacontrolfinduser-method"></a><span data-ttu-id="e7954-103">DiskQuotaControl. FindUser, método</span><span class="sxs-lookup"><span data-stu-id="e7954-103">DiskQuotaControl.FindUser method</span></span>

<span data-ttu-id="e7954-104">Busca la entrada de un usuario, por nombre, en el archivo de cuota del volumen.</span><span class="sxs-lookup"><span data-stu-id="e7954-104">Finds a user's entry, by name, in the volume's quota file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7954-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7954-105">Syntax</span></span>


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="e7954-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7954-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7954-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="e7954-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="e7954-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="e7954-108">Type: **String**</span></span>

<span data-ttu-id="e7954-109">Valor de cadena que contiene el nombre de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="e7954-109">A string value that contains the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7954-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7954-110">Return value</span></span>

<span data-ttu-id="e7954-111">Devuelve una expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) del usuario.</span><span class="sxs-lookup"><span data-stu-id="e7954-111">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7954-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7954-112">Remarks</span></span>

<span data-ttu-id="e7954-113">Este método devuelve un objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) incluso si no hay ninguna entrada para el usuario en el archivo de cuota.</span><span class="sxs-lookup"><span data-stu-id="e7954-113">This method returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object even if there is no entry for the user in the quota file.</span></span> <span data-ttu-id="e7954-114">El objeto de usuario devuelto tiene el umbral de advertencia y los límites de cuota máxima establecidos en los valores predeterminados del volumen.</span><span class="sxs-lookup"><span data-stu-id="e7954-114">The returned user object has warning threshold and hard quota limits set to the volume's default values.</span></span>

<span data-ttu-id="e7954-115">La cadena devuelta por [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) se puede pasar en lugar del parámetro *sLogonName* .</span><span class="sxs-lookup"><span data-stu-id="e7954-115">The string returned from [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) may be passed in place of the *sLogonName* parameter.</span></span> <span data-ttu-id="e7954-116">Cuando **FindUser** recibe una cadena de SID, utiliza el SID correspondiente para la búsqueda directa del registro de cuota del usuario en el volumen.</span><span class="sxs-lookup"><span data-stu-id="e7954-116">When **FindUser** receives a SID string it uses the corresponding SID for direct lookup of the user's quota record on the volume.</span></span> <span data-ttu-id="e7954-117">Esto omite la memoria caché de nombres de SID.</span><span class="sxs-lookup"><span data-stu-id="e7954-117">This bypasses the SID-name cache.</span></span> <span data-ttu-id="e7954-118">En los casos en los que se produce un error de **FindUser** debido a una falta de coincidencia en el formato (por ejemplo, Sam-compatible y UPN) del nombre de inicio de sesión proporcionado y el nombre de inicio de sesión en caché, el nombre de inicio de sesión se puede traducir a una cadena de SID con **TranslateLogonNameToSID** , que se pasa de nuevo a **FindUser**.</span><span class="sxs-lookup"><span data-stu-id="e7954-118">In cases where **FindUser** fails due to a mismatch in format (for example, SAM-compatible and UPN) of the logon name provided and the logon name cached, the logon name can be translated to a SID string using **TranslateLogonNameToSID** then passed again to **FindUser**.</span></span> <span data-ttu-id="e7954-119">En el código de VBScript siguiente se muestra esta técnica.</span><span class="sxs-lookup"><span data-stu-id="e7954-119">The following VBScript code illustrates this technique.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e7954-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7954-120">Requirements</span></span>



| <span data-ttu-id="e7954-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7954-121">Requirement</span></span> | <span data-ttu-id="e7954-122">Value</span><span class="sxs-lookup"><span data-stu-id="e7954-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7954-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7954-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e7954-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e7954-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7954-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7954-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e7954-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e7954-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e7954-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7954-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7954-128"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e7954-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7954-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7954-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7954-130">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="e7954-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




