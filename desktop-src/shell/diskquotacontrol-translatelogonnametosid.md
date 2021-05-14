---
description: Traduce un nombre de inicio de sesión al identificador de seguridad de usuario correspondiente en formato de cadena.
title: Método DiskQuotaControl.TranslateLogonNameToSID
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
ms.openlocfilehash: 5f0a2591b0f5df6bc0f50994fcbf101b7bfbb36d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841566"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a><span data-ttu-id="91340-103">Método DiskQuotaControl.TranslateLogonNameToSID</span><span class="sxs-lookup"><span data-stu-id="91340-103">DiskQuotaControl.TranslateLogonNameToSID method</span></span>

<span data-ttu-id="91340-104">Traduce un nombre de inicio de sesión al identificador de seguridad de usuario correspondiente en formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="91340-104">Translates a logon name to the corresponding user security ID in string format.</span></span>

## <a name="syntax"></a><span data-ttu-id="91340-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91340-105">Syntax</span></span>


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a><span data-ttu-id="91340-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91340-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91340-107">*logonname*</span><span class="sxs-lookup"><span data-stu-id="91340-107">*logonname*</span></span> 
</dt> <dd>

<span data-ttu-id="91340-108">Tipo: **Cadena**</span><span class="sxs-lookup"><span data-stu-id="91340-108">Type: **String**</span></span>

<span data-ttu-id="91340-109">Valor de cadena que especifica el nombre de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="91340-109">A string value that specifies the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91340-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91340-110">Return value</span></span>

<span data-ttu-id="91340-111">Devuelve el identificador de seguridad de usuario (SID) en formato de cadena correspondiente al nombre de inicio de sesión proporcionado.</span><span class="sxs-lookup"><span data-stu-id="91340-111">Returns the user security ID (SID) in string format corresponding to the provided logon name.</span></span> <span data-ttu-id="91340-112">La cadena devuelta incluye las llaves de cierre estándar.</span><span class="sxs-lookup"><span data-stu-id="91340-112">The returned string includes the standard enclosing braces.</span></span> <span data-ttu-id="91340-113">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="91340-113">For example:</span></span>

<span data-ttu-id="91340-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span><span class="sxs-lookup"><span data-stu-id="91340-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span></span>

## <a name="remarks"></a><span data-ttu-id="91340-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91340-115">Remarks</span></span>

<span data-ttu-id="91340-116">La cadena SID devuelta se puede pasar al [**método FindUser**](diskquotacontrol-finduser.md) en lugar de un nombre de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="91340-116">The returned SID string can be passed to the [**FindUser**](diskquotacontrol-finduser.md) method in place of a logon name.</span></span>

<span data-ttu-id="91340-117">Cuando se produce un error en una llamada al método [**FindUser**](diskquotacontrol-finduser.md)( *logonname*), podría deberse a una discrepancia entre el formulario (por ejemplo, compatible con SAM del Administrador de cuentas de seguridad y el UPN de nombre principal de usuario) del nombre de inicio de sesión proporcionado y el formulario almacenado en la caché \[ de nombres de \] \[ \] SID.</span><span class="sxs-lookup"><span data-stu-id="91340-117">When a call to the [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) method fails, it could be due to a mismatch between the form (for example, Security Account Manager \[SAM\] compatible and User Principal Name \[UPN\]) of the logon name provided and the form stored in the SID-name cache.</span></span> <span data-ttu-id="91340-118">En tales casos, el nombre de inicio de sesión se puede convertir en un SID y la llamada a **FindUser se repite.**</span><span class="sxs-lookup"><span data-stu-id="91340-118">In such cases, the logon name can be converted to a SID and the call to **FindUser** repeated.</span></span> <span data-ttu-id="91340-119">**FindUser** reconoce una cadena de SID y omitirá la búsqueda de caché de nombres de SID.</span><span class="sxs-lookup"><span data-stu-id="91340-119">**FindUser** recognizes a SID string and will bypass the SID-name cache lookup.</span></span> <span data-ttu-id="91340-120">El siguiente código Visual Basic Scripting Edition Microsoft (VBScript) ilustra esta técnica.</span><span class="sxs-lookup"><span data-stu-id="91340-120">The following Microsoft Visual Basic Scripting Edition (VBScript) code illustrates this technique.</span></span>


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



<span data-ttu-id="91340-121">La traducción de nombre a SID puede ser un proceso lento en comparación con las búsquedas en la caché de nombres de SID.</span><span class="sxs-lookup"><span data-stu-id="91340-121">Name-to-SID translation can be a slow process when compared to lookups in the SID-name cache.</span></span> <span data-ttu-id="91340-122">Por lo tanto, se recomienda llamar primero a [**FindUser**](diskquotacontrol-finduser.md) con un nombre de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="91340-122">Therefore, it is recommended that [**FindUser**](diskquotacontrol-finduser.md) first be called with a logon name.</span></span> <span data-ttu-id="91340-123">En el ejemplo anterior se usa esta técnica.</span><span class="sxs-lookup"><span data-stu-id="91340-123">The example above uses this technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="91340-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91340-124">Requirements</span></span>



| <span data-ttu-id="91340-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="91340-125">Requirement</span></span> | <span data-ttu-id="91340-126">Value</span><span class="sxs-lookup"><span data-stu-id="91340-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91340-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91340-127">Minimum supported client</span></span><br/> | <span data-ttu-id="91340-128">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="91340-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91340-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91340-129">Minimum supported server</span></span><br/> | <span data-ttu-id="91340-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="91340-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="91340-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91340-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91340-132"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="91340-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91340-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="91340-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91340-134">**DiskQuotaControl (objeto)**</span><span class="sxs-lookup"><span data-stu-id="91340-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




