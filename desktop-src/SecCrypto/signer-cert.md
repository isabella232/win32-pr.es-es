---
description: Especifica un certificado usado para firmar un documento. El certificado se puede almacenar en un archivo de certificado de editor de software (SPC) o en un almacén de certificados.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: Estructura de SIGNER_CERT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278425"
---
# <a name="signer_cert-structure"></a><span data-ttu-id="3b1f4-104">Estructura del \_ certificado del firmante</span><span class="sxs-lookup"><span data-stu-id="3b1f4-104">SIGNER\_CERT structure</span></span>

<span data-ttu-id="3b1f4-105">La estructura del certificado del **firmante \_** especifica un [*certificado*](../secgloss/c-gly.md) usado para firmar un documento.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-105">The **SIGNER\_CERT** structure specifies a [*certificate*](../secgloss/c-gly.md) used to sign a document.</span></span> <span data-ttu-id="3b1f4-106">El certificado se puede almacenar en un archivo de [*certificado de editor de software*](../secgloss/s-gly.md) (SPC) o en un almacén de [*certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3b1f4-106">The certificate can be stored in a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) file or in a [*certificate store*](../secgloss/c-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="3b1f4-107">Esta estructura no está definida en ningún archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="3b1f4-108">Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3b1f4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b1f4-109">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a><span data-ttu-id="3b1f4-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b1f4-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="3b1f4-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="3b1f4-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="3b1f4-112">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="3b1f4-113">**dwCertChoice**</span><span class="sxs-lookup"><span data-stu-id="3b1f4-113">**dwCertChoice**</span></span>
</dt> <dd>

<span data-ttu-id="3b1f4-114">Especifica cómo se almacena el certificado.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-114">Specifies how the certificate is stored.</span></span> <span data-ttu-id="3b1f4-115">Este miembro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="3b1f4-116">Value</span><span class="sxs-lookup"><span data-stu-id="3b1f4-116">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="3b1f4-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3b1f4-117">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <span data-ttu-id="3b1f4-118"><dt>**Firmante \_ \_ \_ Archivo SPC de certificado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3b1f4-118"><dt>**SIGNER\_CERT\_SPC\_FILE**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="3b1f4-119">El certificado se almacena en un archivo SPC.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-119">The certificate is stored in an SPC file.</span></span> <span data-ttu-id="3b1f4-120">El miembro **pwszSpcFile** contiene la ruta de acceso y el nombre del archivo SPC.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-120">The **pwszSpcFile** member contains the path and file name of the SPC file.</span></span><br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <span data-ttu-id="3b1f4-121"><dt>**Firmante \_ \_Almacén de certificados**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3b1f4-121"><dt>**SIGNER\_CERT\_STORE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="3b1f4-122">El certificado se almacena en un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-122">The certificate is stored in a certificate store.</span></span> <span data-ttu-id="3b1f4-123">El miembro **pCertStoreInfo** contiene un puntero a una estructura de [**\_ \_ \_ información del almacén**](signer-cert-store-info.md) de certificados del firmante que especifica el almacén de certificados en el que se almacena el certificado.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-123">The **pCertStoreInfo** member contains a pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span><br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <span data-ttu-id="3b1f4-124"><dt>**Firmante \_ \_ \_ Cadena SPC de CERT**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3b1f4-124"><dt>**SIGNER\_CERT\_SPC\_CHAIN**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="3b1f4-125">El certificado se almacena en un archivo SPC y está asociado a una cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-125">The certificate is stored in an SPC file and is associated with a certificate chain.</span></span> <span data-ttu-id="3b1f4-126">El miembro **pSpcChainInfo** contiene un puntero a una estructura de [**\_ \_ \_ información de cadena SPC de firmante**](signer-spc-chain-info.md) que contiene la información de la cadena para el certificado.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-126">The **pSpcChainInfo** member contains a pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3b1f4-127">**pwszSpcFile**</span><span class="sxs-lookup"><span data-stu-id="3b1f4-127">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="3b1f4-128">Puntero a una cadena Unicode terminada en null que contiene la ruta de acceso y el nombre del archivo SPC en el que se almacena el certificado.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-128">A pointer to a null-terminated Unicode string that contains the path and file name of the SPC file in which the certificate is stored.</span></span> <span data-ttu-id="3b1f4-129">Este miembro solo se utiliza si el miembro **dwCertChoice** contiene el **\_ \_ \_ archivo SPC del certificado del firmante**.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-129">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_FILE**.</span></span>

</dd> <dt>

<span data-ttu-id="3b1f4-130">**pCertStoreInfo**</span><span class="sxs-lookup"><span data-stu-id="3b1f4-130">**pCertStoreInfo**</span></span>
</dt> <dd>

<span data-ttu-id="3b1f4-131">Puntero a una estructura de [**\_ \_ \_ información del almacén**](signer-cert-store-info.md) de certificados del firmante que especifica el almacén de certificados en el que se almacena el certificado.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-131">A pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span> <span data-ttu-id="3b1f4-132">Este miembro solo se utiliza si el miembro **dwCertChoice** contiene el **\_ \_ almacén de certificados del firmante**.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-132">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_STORE**.</span></span>

</dd> <dt>

<span data-ttu-id="3b1f4-133">**pSpcChainInfo**</span><span class="sxs-lookup"><span data-stu-id="3b1f4-133">**pSpcChainInfo**</span></span>
</dt> <dd>

<span data-ttu-id="3b1f4-134">Puntero a una estructura de [**\_ \_ \_ información de cadena SPC de firmante**](signer-spc-chain-info.md) que contiene la información de cadena para el certificado.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-134">A pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span> <span data-ttu-id="3b1f4-135">Este miembro solo se utiliza si el miembro **dwCertChoice** contiene la **\_ \_ \_ cadena SPC del certificado del firmante**.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-135">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_CHAIN**.</span></span>

</dd> <dt>

<span data-ttu-id="3b1f4-136">**identificador**</span><span class="sxs-lookup"><span data-stu-id="3b1f4-136">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="3b1f4-137">Identificador de la ventana que se va a usar como propietario de los cuadros de diálogo que se muestran.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-137">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="3b1f4-138">Este miembro no se utiliza actualmente y se omite.</span><span class="sxs-lookup"><span data-stu-id="3b1f4-138">This member is not currently used and is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b1f4-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b1f4-139">Requirements</span></span>



| <span data-ttu-id="3b1f4-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b1f4-140">Requirement</span></span> | <span data-ttu-id="3b1f4-141">Value</span><span class="sxs-lookup"><span data-stu-id="3b1f4-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3b1f4-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b1f4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3b1f4-143">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3b1f4-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3b1f4-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b1f4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3b1f4-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b1f4-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b1f4-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b1f4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b1f4-147">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="3b1f4-147">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="3b1f4-148">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="3b1f4-148">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
