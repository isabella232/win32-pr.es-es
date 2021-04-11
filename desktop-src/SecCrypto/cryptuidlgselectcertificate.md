---
description: Muestra un cuadro de diálogo que permite al usuario seleccionar un certificado.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: Función CryptUIDlgSelectCertificate
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 65d9993cd1e035473e731056d33b7a391ef47b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278993"
---
# <a name="cryptuidlgselectcertificate-function"></a><span data-ttu-id="e599f-103">Función CryptUIDlgSelectCertificate</span><span class="sxs-lookup"><span data-stu-id="e599f-103">CryptUIDlgSelectCertificate function</span></span>

<span data-ttu-id="e599f-104">La función **CryptUIDlgSelectCertificate** muestra un cuadro de diálogo que permite al usuario seleccionar un certificado.</span><span class="sxs-lookup"><span data-stu-id="e599f-104">The **CryptUIDlgSelectCertificate** function displays a dialog box that allows a user to select a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="e599f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e599f-105">Syntax</span></span>


```C++
);
```



## <a name="parameters"></a><span data-ttu-id="e599f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e599f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e599f-107">*PCSC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e599f-107">*pcsc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e599f-108">Puntero a una estructura de estructura [**CRYPTUI \_ SELECTCERTIFICATE \_**](cryptui-selectcertificate-struct.md) que contiene información sobre el cuadro de diálogo que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="e599f-108">A pointer to a [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure that contains information about the dialog box to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e599f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e599f-109">Return value</span></span>

<span data-ttu-id="e599f-110">Puntero a una estructura [**de \_ contexto de certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) que representa el certificado seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="e599f-110">A pointer to a [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate selected by the user.</span></span> <span data-ttu-id="e599f-111">Cuando haya terminado de utilizar este certificado, debe pasar este puntero a la función [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) para reducir el recuento de referencias del contexto de certificado.</span><span class="sxs-lookup"><span data-stu-id="e599f-111">When you have finished using this certificate, you must pass this pointer to the [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function to decrement the reference count of the certificate context.</span></span>

<span data-ttu-id="e599f-112">Si el miembro **dwFlags** de la estructura *PCSC* no contiene el marcador **de \_ \_ selección MultiSelect CRYPTUI SELECTCERT** , un valor devuelto de **null** significa que el usuario ha cerrado el cuadro de diálogo sin seleccionar ningún certificado.</span><span class="sxs-lookup"><span data-stu-id="e599f-112">If the **dwFlags** member of the *pcsc* structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, a return value of **NULL** means that the user closed the dialog box without selecting a certificate.</span></span>

<span data-ttu-id="e599f-113">Si el miembro **dwFlags** de la estructura *PCSC* contiene el marcador **de \_ \_ selección MultiSelect CRYPTUI SELECTCERT** , esta función siempre devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="e599f-113">If the **dwFlags** member of the *pcsc* structure does contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, this function always returns **NULL**.</span></span> <span data-ttu-id="e599f-114">Los certificados seleccionados se incluirán en el almacén de certificados representado por el miembro **hSelectedCertStore** de *PCSC*.</span><span class="sxs-lookup"><span data-stu-id="e599f-114">The selected certificates will be contained in the certificate store that is represented by the **hSelectedCertStore** member of *pcsc*.</span></span> <span data-ttu-id="e599f-115">Si el número de certificados en el almacén es el mismo antes y después de llamar a **CryptUIDlgSelectCertificate**, el usuario ha cerrado el cuadro de diálogo sin seleccionar ningún certificado.</span><span class="sxs-lookup"><span data-stu-id="e599f-115">If the number of certificates in the store is the same before and after calling **CryptUIDlgSelectCertificate**, the user closed the dialog box without selecting any certificates.</span></span>

## <a name="remarks"></a><span data-ttu-id="e599f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e599f-116">Remarks</span></span>

<span data-ttu-id="e599f-117">Si el miembro **dwFlags** de la estructura de [**\_ \_ struct Cryptui SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) se establece **en \_ cryptui SELECTCERT \_ Legacy**, se muestra el cuadro de diálogo heredado.</span><span class="sxs-lookup"><span data-stu-id="e599f-117">If the **dwFlags** member of the [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure is set to **CRYPTUI\_SELECTCERT\_LEGACY**, the legacy dialog is displayed.</span></span> <span data-ttu-id="e599f-118">De lo contrario, se muestra el cuadro de diálogo de selección de certificado actual.</span><span class="sxs-lookup"><span data-stu-id="e599f-118">Otherwise, the current certificate selection dialog is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e599f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e599f-119">Requirements</span></span>



| <span data-ttu-id="e599f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e599f-120">Requirement</span></span> | <span data-ttu-id="e599f-121">Value</span><span class="sxs-lookup"><span data-stu-id="e599f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e599f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e599f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e599f-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e599f-123">Windows�XP \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e599f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e599f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e599f-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e599f-125">Windows Server�2003 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e599f-126">Finalización del soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e599f-126">End of support</span></span><br/> | <span data-ttu-id="e599f-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e599f-127">Windows�7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e599f-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e599f-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="e599f-129"><dt>Cryptui. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e599f-129"><dt>Cryptui.lib</dt></span></span> </dl>            |
| <span data-ttu-id="e599f-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e599f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e599f-131"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e599f-131"><dt>Cryptui.dll</dt></span></span> </dl>            |
| <span data-ttu-id="e599f-132">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="e599f-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e599f-133">**CryptUIDlgSelectCertificateW** (Unicode) y **CryptUIDlgSelectCertificateA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e599f-133">**CryptUIDlgSelectCertificateW** (Unicode) and **CryptUIDlgSelectCertificateA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e599f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e599f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e599f-135">**CRYPTUI \_ SELECTCERTIFICATE \_ struct**</span><span class="sxs-lookup"><span data-stu-id="e599f-135">**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**</span></span>](cryptui-selectcertificate-struct.md)
</dt> </dl>

<span data-ttu-id="e599f-136">�</span><span class="sxs-lookup"><span data-stu-id="e599f-136">�</span></span>

<span data-ttu-id="e599f-137">�</span><span class="sxs-lookup"><span data-stu-id="e599f-137">�</span></span>




