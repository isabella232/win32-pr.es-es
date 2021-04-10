---
title: Estructura de WINBIO_IDENTITY (Winbio \_ Types. h)
description: Contiene un valor de identificación asociado a una plantilla biométrica.
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- Plataforma de biometría de Windows API de WINBIO_IDENTITY Structure
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150391"
---
# <a name="winbio_identity-structure"></a><span data-ttu-id="fd13a-104">Estructura de identidad de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="fd13a-104">WINBIO\_IDENTITY structure</span></span>

<span data-ttu-id="fd13a-105">La estructura de **\_ identidad de WINBIO** contiene un valor de identificación asociado a una plantilla de biométrica.</span><span class="sxs-lookup"><span data-stu-id="fd13a-105">The **WINBIO\_IDENTITY** structure contains an identifying value associated with a biometric template.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd13a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd13a-106">Syntax</span></span>


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a><span data-ttu-id="fd13a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd13a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd13a-108">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fd13a-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="fd13a-109">Especifica el formato de la información de identidad incluida en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="fd13a-109">Specifies the format of the identity information contained in this structure.</span></span> <span data-ttu-id="fd13a-110">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="fd13a-110">This can be one of the following values:</span></span>



| <span data-ttu-id="fd13a-111">Value</span><span class="sxs-lookup"><span data-stu-id="fd13a-111">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="fd13a-112">Significado</span><span class="sxs-lookup"><span data-stu-id="fd13a-112">Meaning</span></span>                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <span data-ttu-id="fd13a-113"><dt>**WINBIO \_ ID \_ Type \_ null**</dt></span><span class="sxs-lookup"><span data-stu-id="fd13a-113"><dt>**WINBIO\_ID\_TYPE\_NULL**</dt></span></span> </dl>             | <span data-ttu-id="fd13a-114">La plantilla no tiene ningún identificador asociado.</span><span class="sxs-lookup"><span data-stu-id="fd13a-114">The template has no associated ID.</span></span><br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <span data-ttu-id="fd13a-115"><dt>**\_ \_ carácter comodín de tipo de identificador WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd13a-115"><dt>**WINBIO\_ID\_TYPE\_WILDCARD**</dt></span></span> </dl> | <span data-ttu-id="fd13a-116">La estructura coincide con todas las identidades de plantilla.</span><span class="sxs-lookup"><span data-stu-id="fd13a-116">The structure matches all template identities.</span></span><br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <span data-ttu-id="fd13a-117"><dt>**\_GUID de \_ tipo de identificador WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd13a-117"><dt>**WINBIO\_ID\_TYPE\_GUID**</dt></span></span> </dl>             | <span data-ttu-id="fd13a-118">La estructura contiene un GUID asociado a la plantilla.</span><span class="sxs-lookup"><span data-stu-id="fd13a-118">The structure contains a GUID associated with the template.</span></span><br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <span data-ttu-id="fd13a-119"><dt>**identificador de WINBIO de \_ tipo ID. \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd13a-119"><dt>**WINBIO\_ID\_TYPE\_SID**</dt></span></span> </dl>                | <span data-ttu-id="fd13a-120">La estructura contiene el SID de la cuenta asociado a la plantilla.</span><span class="sxs-lookup"><span data-stu-id="fd13a-120">The structure contains the account SID associated with the template.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fd13a-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fd13a-121">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="fd13a-122">Unión que puede contener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="fd13a-122">A union that can contain one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="fd13a-123">**Null**</span><span class="sxs-lookup"><span data-stu-id="fd13a-123">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="fd13a-124">Contiene 1 si el miembro de **tipo** es **WINBIO \_ ID \_ Type \_ null**.</span><span class="sxs-lookup"><span data-stu-id="fd13a-124">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fd13a-125">**Wildcard (Carácter comodín)**</span><span class="sxs-lookup"><span data-stu-id="fd13a-125">**Wildcard**</span></span>
</dt> <dd>

<span data-ttu-id="fd13a-126">Contiene 1 si el miembro de **tipo** es **WINBIO \_ con el tipo de identificador \_ \_ comodín**.</span><span class="sxs-lookup"><span data-stu-id="fd13a-126">Contains 1 if the **Type** member is **WINBIO\_ID\_TYPE\_WILDCARD**.</span></span>

</dd> <dt>

<span data-ttu-id="fd13a-127">**TemplateGuid**</span><span class="sxs-lookup"><span data-stu-id="fd13a-127">**TemplateGuid**</span></span>
</dt> <dd>

<span data-ttu-id="fd13a-128">Contiene un valor GUID de 128 bits que identifica la plantilla si el miembro de **tipo** es el **\_ identificador \_ \_ GUID de tipo WINBIO**.</span><span class="sxs-lookup"><span data-stu-id="fd13a-128">Contains a 128-bit GUID value that identifies the template if the **Type** member is **WINBIO\_ID\_TYPE\_GUID**.</span></span>

</dd> <dt>

<span data-ttu-id="fd13a-129">**AccountSid**</span><span class="sxs-lookup"><span data-stu-id="fd13a-129">**AccountSid**</span></span>
</dt> <dd>

<span data-ttu-id="fd13a-130">Una estructura que contiene un SID de cuenta si el miembro de **tipo** es el **tipo de \_ identificador WINBIO \_ \_ SID**.</span><span class="sxs-lookup"><span data-stu-id="fd13a-130">A structure that contains an account SID if the **Type** member is **WINBIO\_ID\_TYPE\_SID**.</span></span>

<dl> <dt>

<span data-ttu-id="fd13a-131">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="fd13a-131">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="fd13a-132">Número de caracteres del SID.</span><span class="sxs-lookup"><span data-stu-id="fd13a-132">The number of characters in the SID.</span></span>

</dd> <dt>

<span data-ttu-id="fd13a-133">**Data**</span><span class="sxs-lookup"><span data-stu-id="fd13a-133">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="fd13a-134">Matriz de caracteres sin signo que contiene el SID.</span><span class="sxs-lookup"><span data-stu-id="fd13a-134">An array of unsigned characters that contain the SID.</span></span> <span data-ttu-id="fd13a-135">El tamaño máximo actual de la matriz es de 68 caracteres.</span><span class="sxs-lookup"><span data-stu-id="fd13a-135">The current maximum size of the array is 68 characters.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd13a-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd13a-136">Remarks</span></span>

<span data-ttu-id="fd13a-137">Esta estructura se usa en las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="fd13a-137">This structure is used in the following functions:</span></span>

-   [<span data-ttu-id="fd13a-138">**WinBioDeleteTemplate**</span><span class="sxs-lookup"><span data-stu-id="fd13a-138">**WinBioDeleteTemplate**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [<span data-ttu-id="fd13a-139">**WinBioEnrollCommit**</span><span class="sxs-lookup"><span data-stu-id="fd13a-139">**WinBioEnrollCommit**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [<span data-ttu-id="fd13a-140">**WinBioEnumEnrollments**</span><span class="sxs-lookup"><span data-stu-id="fd13a-140">**WinBioEnumEnrollments**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [<span data-ttu-id="fd13a-141">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="fd13a-141">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [<span data-ttu-id="fd13a-142">**WinBioIdentify**</span><span class="sxs-lookup"><span data-stu-id="fd13a-142">**WinBioIdentify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [<span data-ttu-id="fd13a-143">**WinBioRemoveCredential**</span><span class="sxs-lookup"><span data-stu-id="fd13a-143">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [<span data-ttu-id="fd13a-144">**WinBioVerify**</span><span class="sxs-lookup"><span data-stu-id="fd13a-144">**WinBioVerify**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [<span data-ttu-id="fd13a-145">**WinBioVerifyWithCallback**</span><span class="sxs-lookup"><span data-stu-id="fd13a-145">**WinBioVerifyWithCallback**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a><span data-ttu-id="fd13a-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd13a-146">Requirements</span></span>



| <span data-ttu-id="fd13a-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd13a-147">Requirement</span></span> | <span data-ttu-id="fd13a-148">Value</span><span class="sxs-lookup"><span data-stu-id="fd13a-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd13a-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd13a-149">Minimum supported client</span></span><br/> | <span data-ttu-id="fd13a-150">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd13a-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="fd13a-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd13a-151">Minimum supported server</span></span><br/> | <span data-ttu-id="fd13a-152">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd13a-152">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fd13a-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd13a-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd13a-154"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd13a-154"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd13a-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd13a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd13a-156">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="fd13a-156">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





