---
description: En la tabla siguiente se enumeran todos los valores HRESULT que pueden ser devueltos por los métodos de la API de firma digital XPS.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: Errores de la API de firma digital XPS (XpsDigitalSignature. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361241"
---
# <a name="xps-digital-signature-api-errors"></a><span data-ttu-id="33885-103">Errores de la API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="33885-103">XPS Digital Signature API Errors</span></span>

<span data-ttu-id="33885-104">En la tabla siguiente se enumeran todos los valores **HRESULT** que pueden ser devueltos por los métodos de la API de firma digital XPS.</span><span class="sxs-lookup"><span data-stu-id="33885-104">The following table lists all **HRESULT** values that can be returned by the methods in the XPS Digital Signature API.</span></span> <span data-ttu-id="33885-105">Tenga en cuenta que no todos los métodos pueden devolver todos los valores devueltos que se enumeran en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="33885-105">Note that not every method can return every return value listed in this table.</span></span>



| <span data-ttu-id="33885-106">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33885-106">Return code/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="33885-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="33885-107">Description</span></span>                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="33885-108"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="33885-108"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                                                                                 | <span data-ttu-id="33885-109">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="33885-109">The method succeeded.</span></span><br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <span data-ttu-id="33885-110"><dt>**XPS \_ E \_ no válido \_ SIGNATUREBLOCK \_ Markup**</dt> <dt>0x8052038b</dt></span><span class="sxs-lookup"><span data-stu-id="33885-110"><dt>**XPS\_E\_INVALID\_SIGNATUREBLOCK\_MARKUP**</dt> <dt>0x8052038b</dt></span></span> </dl> | <span data-ttu-id="33885-111">Se encontró un error en el marcado XML del bloque de firma mientras se estaba leyendo el marcado de la firma.</span><span class="sxs-lookup"><span data-stu-id="33885-111">Encountered an error in the XML markup of the signature block while the signature markup was being read.</span></span><br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <span data-ttu-id="33885-112"><dt>**XPS \_ \_Elementos de \_ compatibilidad \_ de marcado E**</dt> <dt>0x80520389</dt></span><span class="sxs-lookup"><span data-stu-id="33885-112"><dt>**XPS\_E\_MARKUP\_COMPATIBILITY\_ELEMENTS**</dt> <dt>0x80520389</dt></span></span> </dl> | <span data-ttu-id="33885-113">El valor de [**\_ \_ marcas de signo de XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) especificó que no se esperaba ningún elemento de compatibilidad de marcado; sin embargo, se encontraron elementos de compatibilidad de marcado.</span><span class="sxs-lookup"><span data-stu-id="33885-113">The [**XPS\_SIGN\_FLAGS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) value specified that no markup compatibility elements were expected; however, markup compatibility elements were found.</span></span><br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <span data-ttu-id="33885-114"><dt>**XPS \_ Objeto E 0x8052038a \_ \_ desasociados**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="33885-114"><dt>**XPS\_E\_OBJECT\_DETACHED**</dt> <dt>0x8052038a</dt></span></span> </dl>                                            | <span data-ttu-id="33885-115">La interfaz no está asociada al administrador de firmas.</span><span class="sxs-lookup"><span data-stu-id="33885-115">The interface is not associated with the signature manager.</span></span><br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <span data-ttu-id="33885-116"><dt>**XPS \_ El \_ paquete E \_ ya está \_ abierto**</dt> <dt>0x80520387</dt></span><span class="sxs-lookup"><span data-stu-id="33885-116"><dt>**XPS\_E\_PACKAGE\_ALREADY\_OPENED**</dt> <dt>0x80520387</dt></span></span> </dl>                      | <span data-ttu-id="33885-117">Ya se ha abierto un paquete XPS en el administrador de firmas.</span><span class="sxs-lookup"><span data-stu-id="33885-117">An XPS package has already been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <span data-ttu-id="33885-118"><dt>**XPS \_ E \_ paquete \_ no \_ abierto**</dt> <dt>0x80520386</dt></span><span class="sxs-lookup"><span data-stu-id="33885-118"><dt>**XPS\_E\_PACKAGE\_NOT\_OPENED**</dt> <dt>0x80520386</dt></span></span> </dl>                                  | <span data-ttu-id="33885-119">Todavía no se ha abierto un paquete XPS en el administrador de firmas.</span><span class="sxs-lookup"><span data-stu-id="33885-119">An XPS package has not yet been opened in the signature manager.</span></span> <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <span data-ttu-id="33885-120"><dt>**XPS \_ E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt></span><span class="sxs-lookup"><span data-stu-id="33885-120"><dt>**XPS\_E\_SIGNATUREID\_DUP**</dt> <dt>0x80520388</dt></span></span> </dl>                                            | <span data-ttu-id="33885-121">Dos o más firmas tienen el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="33885-121">Two or more signatures have the same ID.</span></span><br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <span data-ttu-id="33885-122"><dt>**XPS \_ E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt></span><span class="sxs-lookup"><span data-stu-id="33885-122"><dt>**XPS\_E\_SIGREQUESTID\_DUP**</dt> <dt>0x80520385</dt></span></span> </dl>                                         | <span data-ttu-id="33885-123">El identificador de solicitud de firma no es único dentro del bloque de firma.</span><span class="sxs-lookup"><span data-stu-id="33885-123">The signature request ID is not unique within the signature block.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="33885-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33885-124">Remarks</span></span>

<span data-ttu-id="33885-125">Algunos métodos de la API de firma digital XPS realizan llamadas a la API de [empaquetado](/previous-versions/windows/desktop/opc/packaging) .</span><span class="sxs-lookup"><span data-stu-id="33885-125">Some XPS digital signature API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="33885-126">Para obtener información sobre los valores devueltos de la API de empaquetado, consulte [errores de empaquetado](/previous-versions/windows/desktop/opc/packaging-errors).</span><span class="sxs-lookup"><span data-stu-id="33885-126">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="33885-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33885-127">Requirements</span></span>



| <span data-ttu-id="33885-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="33885-128">Requirement</span></span> | <span data-ttu-id="33885-129">Value</span><span class="sxs-lookup"><span data-stu-id="33885-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33885-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33885-130">Minimum supported client</span></span><br/> | <span data-ttu-id="33885-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="33885-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="33885-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33885-132">Minimum supported server</span></span><br/> | <span data-ttu-id="33885-133">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="33885-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="33885-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33885-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="33885-135"><dt>XpsDigitalSignature. h</dt></span><span class="sxs-lookup"><span data-stu-id="33885-135"><dt>Xpsdigitalsignature.h</dt></span></span> </dl>   |
| <span data-ttu-id="33885-136">IDL</span><span class="sxs-lookup"><span data-stu-id="33885-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33885-137"><dt>XpsDigitalSignature. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33885-137"><dt>XpsDigitalSignature.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33885-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="33885-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33885-139">Control de errores en COM</span><span class="sxs-lookup"><span data-stu-id="33885-139">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="33885-140">Errores de empaquetado</span><span class="sxs-lookup"><span data-stu-id="33885-140">Packaging Errors</span></span>](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[<span data-ttu-id="33885-141">Valores devueltos de criptografía</span><span class="sxs-lookup"><span data-stu-id="33885-141">Cryptography Return Values</span></span>](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

