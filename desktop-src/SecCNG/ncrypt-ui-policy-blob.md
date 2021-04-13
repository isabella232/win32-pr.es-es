---
description: Se usa con la \_ \_ \_ propiedad de la propiedad de directiva de interfaz de usuario NCRYPT para contener información de la interfaz de usuario para una clave.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: Estructura de NCRYPT_UI_POLICY_BLOB (ncrypt \_ Provider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: c45b53e051f021ab3dcce6dab4e2317572338624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544995"
---
# <a name="ncrypt_ui_policy_blob-structure"></a><span data-ttu-id="0ebff-103">\_Estructura de \_ BLOB de directiva de interfaz de usuario NCRYPT \_</span><span class="sxs-lookup"><span data-stu-id="0ebff-103">NCRYPT\_UI\_POLICY\_BLOB structure</span></span>

<span data-ttu-id="0ebff-104">La estructura de **\_ \_ \_ blobs** de la Directiva de la interfaz de usuario de ncrypt se usa con la propiedad de la propiedad de directiva de interfaz de usuario ncrypt para contener información de la interfaz de usuario [**\_ \_ \_**](key-storage-property-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="0ebff-104">The **NCRYPT\_UI\_POLICY\_BLOB** structure is used with the [**NCRYPT\_UI\_POLICY\_PROPERTY**](key-storage-property-identifiers.md) property to contain user interface information for a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ebff-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ebff-105">Syntax</span></span>


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a><span data-ttu-id="0ebff-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ebff-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ebff-107">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="0ebff-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="0ebff-108">Número de versión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="0ebff-108">The version number of the structure.</span></span> <span data-ttu-id="0ebff-109">Este miembro debe contener 1.</span><span class="sxs-lookup"><span data-stu-id="0ebff-109">This member must contain 1.</span></span>

</dd> <dt>

<span data-ttu-id="0ebff-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="0ebff-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="0ebff-111">Conjunto de marcas que proporcionan información o requisitos adicionales de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="0ebff-111">A set of flags that provide additional user interface information or requirements.</span></span>



| <span data-ttu-id="0ebff-112">Value</span><span class="sxs-lookup"><span data-stu-id="0ebff-112">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="0ebff-113">Significado</span><span class="sxs-lookup"><span data-stu-id="0ebff-113">Meaning</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <span data-ttu-id="0ebff-114"><dt>**NCRYPT \_ \_Marca de \_ clave \_ de protección de IU**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0ebff-114"><dt>**NCRYPT\_UI\_PROTECT\_KEY\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="0ebff-115">Muestre la interfaz de usuario de clave segura según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="0ebff-115">Display the strong key user interface as needed.</span></span><br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <span data-ttu-id="0ebff-116"><dt>**NCRYPT \_ Marca de IU \_ forzada de \_ alta \_ protección \_**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="0ebff-116"><dt>**NCRYPT\_UI\_FORCE\_HIGH\_PROTECTION\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="0ebff-117">Forzar la alta protección.</span><span class="sxs-lookup"><span data-stu-id="0ebff-117">Force high protection.</span></span><br/>                           |



 

</dd> <dt>

<span data-ttu-id="0ebff-118">**cbCreationTitle**</span><span class="sxs-lookup"><span data-stu-id="0ebff-118">**cbCreationTitle**</span></span>
</dt> <dd>

<span data-ttu-id="0ebff-119">La longitud, en bytes, del título de creación.</span><span class="sxs-lookup"><span data-stu-id="0ebff-119">The length, in bytes, of the creation title.</span></span> <span data-ttu-id="0ebff-120">El título de creación es una cadena Unicode terminada en null que especifica el texto que se utiliza como título del cuadro de diálogo clave segura cuando se completa la clave.</span><span class="sxs-lookup"><span data-stu-id="0ebff-120">The creation title is a null-terminated Unicode string that specifies the text that is used as the title of the strong key dialog box when the key is completed.</span></span> <span data-ttu-id="0ebff-121">El título de creación debe colocarse inmediatamente después de la estructura de BLOB de la **Directiva de interfaz de usuario de NCRYPT \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="0ebff-121">The creation title must be placed immediately following the **NCRYPT\_UI\_POLICY\_BLOB** structure.</span></span> <span data-ttu-id="0ebff-122">Si el valor del miembro **cbCreationTitle** se establece en 0, se usa un título de creación predeterminado para el título del cuadro de diálogo clave segura.</span><span class="sxs-lookup"><span data-stu-id="0ebff-122">If the value of the **cbCreationTitle** member is set to 0, a default creation title is used for the title of the strong key dialog box.</span></span> <span data-ttu-id="0ebff-123">Este miembro solo se usa en la finalización de la clave.</span><span class="sxs-lookup"><span data-stu-id="0ebff-123">This member is only used on key finalization.</span></span>

</dd> <dt>

<span data-ttu-id="0ebff-124">**cbFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="0ebff-124">**cbFriendlyName**</span></span>
</dt> <dd>

<span data-ttu-id="0ebff-125">Longitud, en bytes, del nombre descriptivo de la clave.</span><span class="sxs-lookup"><span data-stu-id="0ebff-125">The length, in bytes, of the friendly name of the key.</span></span> <span data-ttu-id="0ebff-126">El nombre descriptivo es una cadena Unicode terminada en null que contiene el texto que se muestra en el cuadro de diálogo clave segura como el nombre de la clave.</span><span class="sxs-lookup"><span data-stu-id="0ebff-126">The friendly name is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the name of the key.</span></span> <span data-ttu-id="0ebff-127">El nombre descriptivo debe colocarse inmediatamente después del título de creación en este BLOB.</span><span class="sxs-lookup"><span data-stu-id="0ebff-127">The friendly name must be placed immediately following the creation title in this BLOB.</span></span> <span data-ttu-id="0ebff-128">Si el valor del miembro **cbFriendlyName** se establece en 0, se usa un nombre predeterminado en el cuadro de diálogo clave segura.</span><span class="sxs-lookup"><span data-stu-id="0ebff-128">If the value of the **cbFriendlyName** member is set to 0, a default name is used in the strong key dialog box.</span></span> <span data-ttu-id="0ebff-129">Este miembro se usa cuando se completa la clave y cuando se usa la clave.</span><span class="sxs-lookup"><span data-stu-id="0ebff-129">This member is used both when the key is completed and when the key is used.</span></span>

</dd> <dt>

<span data-ttu-id="0ebff-130">**cbDescription**</span><span class="sxs-lookup"><span data-stu-id="0ebff-130">**cbDescription**</span></span>
</dt> <dd>

<span data-ttu-id="0ebff-131">La longitud, en bytes, de la descripción de la clave.</span><span class="sxs-lookup"><span data-stu-id="0ebff-131">The length, in bytes, of the key description.</span></span> <span data-ttu-id="0ebff-132">La descripción de la clave es una cadena Unicode terminada en null que contiene el texto que se muestra en el cuadro de diálogo clave segura como la descripción de la clave.</span><span class="sxs-lookup"><span data-stu-id="0ebff-132">The key description is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the description of the key.</span></span> <span data-ttu-id="0ebff-133">El valor de descripción debe colocarse inmediatamente después del nombre descriptivo de este BLOB.</span><span class="sxs-lookup"><span data-stu-id="0ebff-133">The description value must be placed immediately following the friendly name in this BLOB.</span></span> <span data-ttu-id="0ebff-134">Si el valor del miembro **cbDescription** se establece en 0, se usa una descripción predeterminada en el cuadro de diálogo clave segura.</span><span class="sxs-lookup"><span data-stu-id="0ebff-134">If the value of the **cbDescription** member is set to 0, a default description is used in the strong key dialog box.</span></span> <span data-ttu-id="0ebff-135">Este miembro se usa cuando se completa la clave y cuando se usa la clave.</span><span class="sxs-lookup"><span data-stu-id="0ebff-135">This member is used both when the key is completed and when the key is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0ebff-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ebff-136">Remarks</span></span>

<span data-ttu-id="0ebff-137">Esta estructura se incluye en el \_ encabezado del proveedor ncrypt. h.</span><span class="sxs-lookup"><span data-stu-id="0ebff-137">This structure is included in the Ncrypt\_provider.h header.</span></span> <span data-ttu-id="0ebff-138">Para usar la estructura, debe descargar el [Kit de desarrollo de proveedores de servicios criptográficos](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) de Microsoft Connect.</span><span class="sxs-lookup"><span data-stu-id="0ebff-138">To use the structure, you must download the [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) from Microsoft Connect.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebff-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ebff-139">Requirements</span></span>



| <span data-ttu-id="0ebff-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ebff-140">Requirement</span></span> | <span data-ttu-id="0ebff-141">Value</span><span class="sxs-lookup"><span data-stu-id="0ebff-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebff-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ebff-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0ebff-143">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0ebff-143">Windows Vista \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0ebff-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ebff-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0ebff-145">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ebff-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0ebff-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ebff-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ebff-147"><dt>Ncrypt \_ Provider. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ebff-147"><dt>Ncrypt\_provider.h</dt></span></span> </dl> |



 

