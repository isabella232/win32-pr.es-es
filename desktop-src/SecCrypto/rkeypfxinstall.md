---
description: No se admite la función RKeyPFXInstall.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: Función RKeyPFXInstall (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001159"
---
# <a name="rkeypfxinstall-function"></a><span data-ttu-id="d7e80-103">RKeyPFXInstall función)</span><span class="sxs-lookup"><span data-stu-id="d7e80-103">RKeyPFXInstall function</span></span>

<span data-ttu-id="d7e80-104">No se admite la función **RKeyPFXInstall** .</span><span class="sxs-lookup"><span data-stu-id="d7e80-104">The **RKeyPFXInstall** function is not supported.</span></span>

<span data-ttu-id="d7e80-105">**Windows Server 2003:** La función **RKeyPFXInstall** instala un certificado en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="d7e80-105">**Windows Server 2003:** The **RKeyPFXInstall** function installs a certificate on a remote computer.</span></span> <span data-ttu-id="d7e80-106">Tenga en cuenta que este comportamiento ha cambiado con Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d7e80-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7e80-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7e80-107">Syntax</span></span>


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d7e80-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7e80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7e80-109">*hKeySvcCli* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7e80-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7e80-110">Identificador [**de \_ controlador de KEYSVCC**](keysvcc-handle.md) abierto previamente por [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span><span class="sxs-lookup"><span data-stu-id="d7e80-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="d7e80-111">El identificador representa el equipo remoto que recibirá el certificado.</span><span class="sxs-lookup"><span data-stu-id="d7e80-111">The handle represents the remote computer that will receive the certificate.</span></span> <span data-ttu-id="d7e80-112">Este valor no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="d7e80-112">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d7e80-113">*pPFX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7e80-113">*pPFX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7e80-114">Puntero a una estructura [**de \_ blobs de KEYSVC**](keysvc-blob.md) que representa el certificado que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="d7e80-114">A pointer to a [**KEYSVC\_BLOB**](keysvc-blob.md) structure that represents the certificate to install.</span></span> <span data-ttu-id="d7e80-115">El BLOB está en formato [*PKCS \# 12*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d7e80-115">The BLOB is in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> <dt>

<span data-ttu-id="d7e80-116">*pPassword* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7e80-116">*pPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7e80-117">Puntero a una estructura [**de \_ \_ cadena Unicode KEYSVC**](keysvc-unicode-string.md) que representa la contraseña del BLOB.</span><span class="sxs-lookup"><span data-stu-id="d7e80-117">A pointer to a [**KEYSVC\_UNICODE\_STRING**](keysvc-unicode-string.md) structure that represents the password for the BLOB.</span></span> <span data-ttu-id="d7e80-118">Cuando haya terminado de usar la contraseña, borre la contraseña de la memoria mediante una llamada a la función [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d7e80-118">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="d7e80-119">Para obtener más información sobre cómo proteger las contraseñas, consulte [Administrar contraseñas](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="d7e80-119">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7e80-120">*ulFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7e80-120">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7e80-121">Marcas que especifican las opciones de instalación del certificado.</span><span class="sxs-lookup"><span data-stu-id="d7e80-121">Flags that specify the certificate installation options.</span></span> <span data-ttu-id="d7e80-122">Este parámetro puede ser un cero o una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d7e80-122">This parameter can be a zero or a combination of the following values.</span></span>



| <span data-ttu-id="d7e80-123">Value</span><span class="sxs-lookup"><span data-stu-id="d7e80-123">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="d7e80-124">Significado</span><span class="sxs-lookup"><span data-stu-id="d7e80-124">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <span data-ttu-id="d7e80-125"><dt>**Cifrado \_ Exportable**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="d7e80-125"><dt>**CRYPT\_EXPORTABLE**</dt> <dt></dt></span></span> </dl>              | <span data-ttu-id="d7e80-126">Las claves importadas se marcan como exportables.</span><span class="sxs-lookup"><span data-stu-id="d7e80-126">Imported keys are marked as exportable.</span></span><br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <span data-ttu-id="d7e80-127"><dt>**Cifrado \_ \_conjunto de claves de equipo**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="d7e80-127"><dt>**CRYPT\_MACHINE\_KEYSET**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="d7e80-128">Las claves privadas se almacenan en el equipo remoto y no en el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="d7e80-128">Private keys are stored under the remote computer and not under the current user.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7e80-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7e80-129">Return value</span></span>

<span data-ttu-id="d7e80-130">Si la función se realiza correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d7e80-130">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="d7e80-131">Si se produce un error en la función, el valor devuelto es un **ULong** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="d7e80-131">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7e80-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7e80-132">Requirements</span></span>



| <span data-ttu-id="d7e80-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7e80-133">Requirement</span></span> | <span data-ttu-id="d7e80-134">Value</span><span class="sxs-lookup"><span data-stu-id="d7e80-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e80-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7e80-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d7e80-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d7e80-136">None supported</span></span><br/>                                                             |
| <span data-ttu-id="d7e80-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7e80-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d7e80-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7e80-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7e80-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7e80-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7e80-140"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7e80-140"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7e80-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7e80-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7e80-142">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="d7e80-142">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="d7e80-143">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="d7e80-143">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> </dl>

 

 
