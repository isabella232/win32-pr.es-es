---
description: Muestra un cuadro de diálogo que permite a un usuario seleccionar un certificado.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: Función CryptUIDlgSelectCertificate
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 8f015796671990491407d91cbd51761816c5434b
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925698"
---
# <a name="cryptuidlgselectcertificate-function"></a><span data-ttu-id="0a6fa-103">Función CryptUIDlgSelectCertificate</span><span class="sxs-lookup"><span data-stu-id="0a6fa-103">CryptUIDlgSelectCertificate function</span></span>

<span data-ttu-id="0a6fa-104">La **función CryptUIDlgSelectCertificate** muestra un cuadro de diálogo que permite a un usuario seleccionar un certificado.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-104">The **CryptUIDlgSelectCertificate** function displays a dialog box that allows a user to select a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a6fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a6fa-105">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI CryptUIDlgSelectCertificate(
  _In_  PCCRYPTUI_SELECTCERTIFICATE_STRUCT pcsc
);
```



## <a name="parameters"></a><span data-ttu-id="0a6fa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a6fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a6fa-107">*pcsc* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0a6fa-107">*pcsc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a6fa-108">Puntero a una [**estructura CRYPTUI \_ SELECTCERTIFICATE \_ STRUCT**](cryptui-selectcertificate-struct.md) que contiene información sobre el cuadro de diálogo que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-108">A pointer to a [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure that contains information about the dialog box to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a6fa-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a6fa-109">Return value</span></span>

<span data-ttu-id="0a6fa-110">Puntero a una [**estructura CERT \_ CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) que representa el certificado seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-110">A pointer to a [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate selected by the user.</span></span> <span data-ttu-id="0a6fa-111">Cuando haya terminado de usar este certificado, debe pasar este puntero a la función [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) para disminuir el recuento de referencias del contexto del certificado.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-111">When you have finished using this certificate, you must pass this pointer to the [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function to decrement the reference count of the certificate context.</span></span>

<span data-ttu-id="0a6fa-112">Si el **miembro dwFlags** de la estructura *pcsc* no contiene la marca **CRYPTUI \_ SELECTCERT \_ MULTISELECT,** un valor devuelto de **NULL** significa que el usuario cerró el cuadro de diálogo sin seleccionar un certificado.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-112">If the **dwFlags** member of the *pcsc* structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, a return value of **NULL** means that the user closed the dialog box without selecting a certificate.</span></span>

<span data-ttu-id="0a6fa-113">Si el **miembro dwFlags** de la estructura *pcsc* contiene la marca **CRYPTUI \_ SELECTCERT \_ MULTISELECT,** esta función siempre devuelve **NULL.**</span><span class="sxs-lookup"><span data-stu-id="0a6fa-113">If the **dwFlags** member of the *pcsc* structure does contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, this function always returns **NULL**.</span></span> <span data-ttu-id="0a6fa-114">Los certificados seleccionados se incluirán en el almacén de certificados representado por el **miembro hSelectedCertStore** de *pcsc*.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-114">The selected certificates will be contained in the certificate store that is represented by the **hSelectedCertStore** member of *pcsc*.</span></span> <span data-ttu-id="0a6fa-115">Si el número de certificados del almacén es el mismo antes y después de llamar a **CryptUIDlgSelectCertificate,** el usuario cerró el cuadro de diálogo sin seleccionar ningún certificado.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-115">If the number of certificates in the store is the same before and after calling **CryptUIDlgSelectCertificate**, the user closed the dialog box without selecting any certificates.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a6fa-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a6fa-116">Remarks</span></span>

<span data-ttu-id="0a6fa-117">Si el **miembro dwFlags** de la estructura [**CRYPTUI \_ SELECTCERTIFICATE \_ STRUCT**](cryptui-selectcertificate-struct.md) se establece en **CRYPTUI \_ SELECTCERT \_ LEGACY,** se muestra el cuadro de diálogo heredado.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-117">If the **dwFlags** member of the [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure is set to **CRYPTUI\_SELECTCERT\_LEGACY**, the legacy dialog is displayed.</span></span> <span data-ttu-id="0a6fa-118">De lo contrario, se muestra el cuadro de diálogo de selección de certificado actual.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-118">Otherwise, the current certificate selection dialog is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a6fa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a6fa-119">Requirements</span></span>



| <span data-ttu-id="0a6fa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a6fa-120">Requirement</span></span> | <span data-ttu-id="0a6fa-121">Value</span><span class="sxs-lookup"><span data-stu-id="0a6fa-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a6fa-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a6fa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0a6fa-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0a6fa-123">Windows�XP \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0a6fa-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a6fa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0a6fa-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a6fa-125">Windows Server�2003 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="0a6fa-126">Finalización del soporte técnico</span><span class="sxs-lookup"><span data-stu-id="0a6fa-126">End of support</span></span><br/> | <span data-ttu-id="0a6fa-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a6fa-127">Windows�7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0a6fa-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a6fa-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a6fa-129"><dt>Cryptui.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a6fa-129"><dt>Cryptui.lib</dt></span></span> </dl>            |
| <span data-ttu-id="0a6fa-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a6fa-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a6fa-131"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a6fa-131"><dt>Cryptui.dll</dt></span></span> </dl>            |
| <span data-ttu-id="0a6fa-132">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="0a6fa-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0a6fa-133">**CryptUIDlgSelectCertificateW** (Unicode) y **CryptUIDlgSelectCertificateA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0a6fa-133">**CryptUIDlgSelectCertificateW** (Unicode) and **CryptUIDlgSelectCertificateA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a6fa-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0a6fa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6fa-135">**CRYPTUI \_ SELECTCERTIFICATE \_ STRUCT**</span><span class="sxs-lookup"><span data-stu-id="0a6fa-135">**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**</span></span>](cryptui-selectcertificate-struct.md)
</dt> </dl>






