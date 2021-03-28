---
description: Traduce un nombre de inicio de sesión al ID. de seguridad de usuario correspondiente en formato de cadena.
title: DiskQuotaControl. TranslateLogonNameToSID, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: ec5e6c0bbd013c8fbd3f6616671ee006109566d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082961"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a><span data-ttu-id="76701-103">DiskQuotaControl. TranslateLogonNameToSID, método</span><span class="sxs-lookup"><span data-stu-id="76701-103">DiskQuotaControl.TranslateLogonNameToSID method</span></span>

<span data-ttu-id="76701-104">Traduce un nombre de inicio de sesión al ID. de seguridad de usuario correspondiente en formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="76701-104">Translates a logon name to the corresponding user security ID in string format.</span></span>

## <a name="syntax"></a><span data-ttu-id="76701-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76701-105">Syntax</span></span>


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a><span data-ttu-id="76701-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76701-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76701-107">*logonname*</span><span class="sxs-lookup"><span data-stu-id="76701-107">*logonname*</span></span> 
</dt> <dd>

<span data-ttu-id="76701-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="76701-108">Type: **String**</span></span>

<span data-ttu-id="76701-109">Valor de cadena que especifica el nombre de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="76701-109">A string value that specifies the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76701-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76701-110">Return value</span></span>

<span data-ttu-id="76701-111">Devuelve el identificador de seguridad (SID) del usuario en formato de cadena que corresponde al nombre de inicio de sesión proporcionado.</span><span class="sxs-lookup"><span data-stu-id="76701-111">Returns the user security ID (SID) in string format corresponding to the provided logon name.</span></span> <span data-ttu-id="76701-112">La cadena devuelta incluye las llaves de inclusión estándar.</span><span class="sxs-lookup"><span data-stu-id="76701-112">The returned string includes the standard enclosing braces.</span></span> <span data-ttu-id="76701-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="76701-113">For example:</span></span>

<span data-ttu-id="76701-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span><span class="sxs-lookup"><span data-stu-id="76701-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span></span>

## <a name="remarks"></a><span data-ttu-id="76701-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76701-115">Remarks</span></span>

<span data-ttu-id="76701-116">La cadena de SID devuelta se puede pasar al método [**FindUser**](diskquotacontrol-finduser.md) en lugar de un nombre de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="76701-116">The returned SID string can be passed to the [**FindUser**](diskquotacontrol-finduser.md) method in place of a logon name.</span></span>

<span data-ttu-id="76701-117">Cuando se produce un error en una llamada al método [**FindUser**](diskquotacontrol-finduser.md)( *logonname*), podría deberse a una falta de coincidencia entre el formulario (por ejemplo, el administrador de cuentas de seguridad \[ Sam \] compatible y el nombre principal \[ de usuario UPN \] ) del nombre de inicio de sesión proporcionado y el formulario almacenado en la caché de nombres de SID.</span><span class="sxs-lookup"><span data-stu-id="76701-117">When a call to the [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) method fails, it could be due to a mismatch between the form (for example, Security Account Manager \[SAM\] compatible and User Principal Name \[UPN\]) of the logon name provided and the form stored in the SID-name cache.</span></span> <span data-ttu-id="76701-118">En tales casos, el nombre de inicio de sesión se puede convertir en un SID y la llamada a **FindUser** se repite.</span><span class="sxs-lookup"><span data-stu-id="76701-118">In such cases, the logon name can be converted to a SID and the call to **FindUser** repeated.</span></span> <span data-ttu-id="76701-119">**FindUser** reconoce una cadena de SID y omitirá la búsqueda de caché de nombres de SID.</span><span class="sxs-lookup"><span data-stu-id="76701-119">**FindUser** recognizes a SID string and will bypass the SID-name cache lookup.</span></span> <span data-ttu-id="76701-120">En el siguiente código de Microsoft Visual Basic Scripting Edition (VBScript) se muestra esta técnica.</span><span class="sxs-lookup"><span data-stu-id="76701-120">The following Microsoft Visual Basic Scripting Edition (VBScript) code illustrates this technique.</span></span>


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



<span data-ttu-id="76701-121">La traducción de nombre a SID puede ser un proceso lento en comparación con las búsquedas en la caché de nombres de SID.</span><span class="sxs-lookup"><span data-stu-id="76701-121">Name-to-SID translation can be a slow process when compared to lookups in the SID-name cache.</span></span> <span data-ttu-id="76701-122">Por lo tanto, se recomienda llamar primero a [**FindUser**](diskquotacontrol-finduser.md) con un nombre de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="76701-122">Therefore, it is recommended that [**FindUser**](diskquotacontrol-finduser.md) first be called with a logon name.</span></span> <span data-ttu-id="76701-123">En el ejemplo anterior se usa esta técnica.</span><span class="sxs-lookup"><span data-stu-id="76701-123">The example above uses this technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="76701-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76701-124">Requirements</span></span>



| <span data-ttu-id="76701-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="76701-125">Requirement</span></span> | <span data-ttu-id="76701-126">Value</span><span class="sxs-lookup"><span data-stu-id="76701-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76701-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76701-127">Minimum supported client</span></span><br/> | <span data-ttu-id="76701-128">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="76701-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76701-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76701-129">Minimum supported server</span></span><br/> | <span data-ttu-id="76701-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="76701-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="76701-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="76701-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76701-132"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="76701-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76701-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="76701-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76701-134">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="76701-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




