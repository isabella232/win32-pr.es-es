---
description: Especifica el proveedor de servicios criptográficos (CSP) y la información de clave privada utilizada para crear una firma digital.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: Estructura de SIGNER_PROVIDER_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668197"
---
# <a name="signer_provider_info-structure"></a><span data-ttu-id="ce4e9-103">Estructura de \_ información del proveedor de firmante \_</span><span class="sxs-lookup"><span data-stu-id="ce4e9-103">SIGNER\_PROVIDER\_INFO structure</span></span>

<span data-ttu-id="ce4e9-104">La estructura de **\_ \_ información del proveedor de firmante** especifica el proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) y la información de clave privada que se usa para crear una firma digital.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-104">The **SIGNER\_PROVIDER\_INFO** structure specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="ce4e9-105">Esta estructura no está definida en ningún archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="ce4e9-106">Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ce4e9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce4e9-107">Syntax</span></span>


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a><span data-ttu-id="ce4e9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ce4e9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce4e9-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="ce4e9-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="ce4e9-110">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="ce4e9-111">**pwszProviderName**</span><span class="sxs-lookup"><span data-stu-id="ce4e9-111">**pwszProviderName**</span></span>
</dt> <dd>

<span data-ttu-id="ce4e9-112">Nombre del CSP que se usa para crear la firma digital.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-112">The name of the CSP used to create the digital signature.</span></span> <span data-ttu-id="ce4e9-113">Si el valor de este miembro es **null**, se utiliza el proveedor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-113">If the value of this member is **NULL**, the default provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="ce4e9-114">**dwProviderType**</span><span class="sxs-lookup"><span data-stu-id="ce4e9-114">**dwProviderType**</span></span>
</dt> <dd>

<span data-ttu-id="ce4e9-115">Tipo del CSP especificado por el miembro **pwszProviderName** .</span><span class="sxs-lookup"><span data-stu-id="ce4e9-115">The type of the CSP specified by the **pwszProviderName** member.</span></span>

</dd> <dt>

<span data-ttu-id="ce4e9-116">**dwKeySpec**</span><span class="sxs-lookup"><span data-stu-id="ce4e9-116">**dwKeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="ce4e9-117">Especificación de la clave.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-117">The key specification.</span></span> <span data-ttu-id="ce4e9-118">Si este miembro se establece en cero, se usa la especificación de clave en el miembro **pwszPvkFileName** o **pwszKeyContainer** .</span><span class="sxs-lookup"><span data-stu-id="ce4e9-118">If this member is set to zero, the key specification in the **pwszPvkFileName** or **pwszKeyContainer** member is used.</span></span> <span data-ttu-id="ce4e9-119">Si hay más de una especificación de clave en el miembro **pwszKeyContainer** , se usa **en la \_ firma** .</span><span class="sxs-lookup"><span data-stu-id="ce4e9-119">If there is more than one key specification in the **pwszKeyContainer** member, **AT\_SIGNATURE** is used.</span></span> <span data-ttu-id="ce4e9-120">Si se produce un error, se usa **en \_ KEYEXCHANGE** .</span><span class="sxs-lookup"><span data-stu-id="ce4e9-120">If it fails, **AT\_KEYEXCHANGE** is used.</span></span>

</dd> <dt>

<span data-ttu-id="ce4e9-121">**dwPvkChoice**</span><span class="sxs-lookup"><span data-stu-id="ce4e9-121">**dwPvkChoice**</span></span>
</dt> <dd>

<span data-ttu-id="ce4e9-122">Especifica el tipo de información de clave privada.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-122">Specifies the type of private key information.</span></span> <span data-ttu-id="ce4e9-123">Este miembro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-123">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="ce4e9-124">Value</span><span class="sxs-lookup"><span data-stu-id="ce4e9-124">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="ce4e9-125">Significado</span><span class="sxs-lookup"><span data-stu-id="ce4e9-125">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <span data-ttu-id="ce4e9-126"><dt>**PVK \_ \_ \_ Nombre del archivo de tipo**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ce4e9-126"><dt>**PVK\_TYPE\_FILE\_NAME**</dt> <dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="ce4e9-127">La información de clave privada es un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-127">The private key information is a file name.</span></span><br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <span data-ttu-id="ce4e9-128"><dt>**PVK \_ TIPO \_ keycontainer**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="ce4e9-128"><dt>**PVK\_TYPE\_KEYCONTAINER**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="ce4e9-129">La información de clave privada es un contenedor de claves.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-129">The private key information is a key container.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ce4e9-130">**pwszPvkFileName**</span><span class="sxs-lookup"><span data-stu-id="ce4e9-130">**pwszPvkFileName**</span></span>
</dt> <dd>

<span data-ttu-id="ce4e9-131">Nombre del archivo que contiene la información de la clave privada.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-131">The name of the file that contains the private key information.</span></span>

</dd> <dt>

<span data-ttu-id="ce4e9-132">**pwszKeyContainer**</span><span class="sxs-lookup"><span data-stu-id="ce4e9-132">**pwszKeyContainer**</span></span>
</dt> <dd>

<span data-ttu-id="ce4e9-133">Nombre del contenedor de claves que contiene la información de la clave privada.</span><span class="sxs-lookup"><span data-stu-id="ce4e9-133">The name of the key container that contains the private key information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce4e9-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce4e9-134">Requirements</span></span>



| <span data-ttu-id="ce4e9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce4e9-135">Requirement</span></span> | <span data-ttu-id="ce4e9-136">Value</span><span class="sxs-lookup"><span data-stu-id="ce4e9-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce4e9-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce4e9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ce4e9-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ce4e9-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ce4e9-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce4e9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ce4e9-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce4e9-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce4e9-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce4e9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce4e9-142">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="ce4e9-142">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="ce4e9-143">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="ce4e9-143">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
