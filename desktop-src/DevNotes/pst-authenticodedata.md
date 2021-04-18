---
description: Define los datos que se van a usar en la comprobación Authenticode de Microsoft de los datos de los elementos.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: PST_AUTHENTICODEDATA estructura (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: ff53526febcc8eab1a95285ffa3dcb59fe628238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649813"
---
# <a name="pst_authenticodedata-structure"></a><span data-ttu-id="a1021-103">\_Estructura AUTHENTICODEDATA de PST</span><span class="sxs-lookup"><span data-stu-id="a1021-103">PST\_AUTHENTICODEDATA structure</span></span>

<span data-ttu-id="a1021-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a1021-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a1021-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a1021-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a1021-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="a1021-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a1021-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a1021-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a1021-108">Define los datos que se van a usar en la comprobación Authenticode de Microsoft de los datos de los elementos.</span><span class="sxs-lookup"><span data-stu-id="a1021-108">Defines data to be used in Microsoft Authenticode verification of item data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1021-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1021-109">Syntax</span></span>


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a><span data-ttu-id="a1021-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1021-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1021-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="a1021-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="a1021-112">Tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="a1021-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="a1021-113">**dwModifiers**</span><span class="sxs-lookup"><span data-stu-id="a1021-113">**dwModifiers**</span></span>
</dt> <dd>

<span data-ttu-id="a1021-114">Valor que identifica el modificador que debe comprobar una cadena de llamadores.</span><span class="sxs-lookup"><span data-stu-id="a1021-114">A value that identifies the modifier that one of a chain of callers must verify.</span></span>



| <span data-ttu-id="a1021-115">Value</span><span class="sxs-lookup"><span data-stu-id="a1021-115">Value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="a1021-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a1021-116">Meaning</span></span>                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <span data-ttu-id="a1021-117"><dt>**Archivo pst \_ \_Único \_ llamador AC**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a1021-117"><dt>**PST\_AC\_SINGLE\_CALLER**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="a1021-118">Solo un nivel de la cadena de llamadas a PStore.</span><span class="sxs-lookup"><span data-stu-id="a1021-118">Only a single level in the call chain to PStore.</span></span> <span data-ttu-id="a1021-119">El autor de la llamada pasa la comprobación de comprobación.</span><span class="sxs-lookup"><span data-stu-id="a1021-119">The caller passes the verification check.</span></span> <span data-ttu-id="a1021-120">La imagen especificada es el llamador inmediato y es una aplicación (. exe).</span><span class="sxs-lookup"><span data-stu-id="a1021-120">The specified image is the immediate caller, and is an application (.exe).</span></span><br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <span data-ttu-id="a1021-121"><dt>**Archivo pst \_ \_ \_ \_ Llamador de nivel superior AC**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a1021-121"><dt>**PST\_AC\_TOP\_LEVEL\_CALLER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="a1021-122">El autor de la llamada de nivel superior debe superar la comprobación, pero puede haber archivos dll intermedios.</span><span class="sxs-lookup"><span data-stu-id="a1021-122">The top-level caller must pass the check, but there may be intermediate DLLs.</span></span> <span data-ttu-id="a1021-123">La imagen especificada no es necesariamente el llamador inmediato y es una aplicación (. exe).</span><span class="sxs-lookup"><span data-stu-id="a1021-123">The specified image is not necessarily the immediate caller, and is an application (.exe).</span></span><br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <span data-ttu-id="a1021-124"><dt>**Archivo pst \_ \_ \_ Llamador inmediato AC**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a1021-124"><dt>**PST\_AC\_IMMEDIATE\_CALLER**</dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="a1021-125">El autor de la llamada inmediato debe superar la comprobación, pero no es necesario que sea el proceso de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="a1021-125">The immediate caller must pass the check, but need not be the top-level process.</span></span> <span data-ttu-id="a1021-126">La imagen especificada es el llamador inmediato y la imagen puede ser una aplicación (. exe) o un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="a1021-126">The specified image is the immediate caller, and the image can be an application (.exe) or a DLL.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a1021-127">**szRootCA**</span><span class="sxs-lookup"><span data-stu-id="a1021-127">**szRootCA**</span></span>
</dt> <dd>

<span data-ttu-id="a1021-128">Puntero a una cadena de caracteres anchos que representa la entidad de certificación (CA) raíz del certificado; Use **null** para usar cualquier CA disponible.</span><span class="sxs-lookup"><span data-stu-id="a1021-128">A pointer to a wide character string that represents the root certification authority (CA) for the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="a1021-129">**szIssuer**</span><span class="sxs-lookup"><span data-stu-id="a1021-129">**szIssuer**</span></span>
</dt> <dd>

<span data-ttu-id="a1021-130">Puntero a una cadena de caracteres anchos que representa la entidad de certificación que emitió el certificado; Use **null** para usar cualquier CA disponible.</span><span class="sxs-lookup"><span data-stu-id="a1021-130">A pointer to a wide character string that represents the CA that issued the certificate; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="a1021-131">**szPublisher**</span><span class="sxs-lookup"><span data-stu-id="a1021-131">**szPublisher**</span></span>
</dt> <dd>

<span data-ttu-id="a1021-132">Puntero a una cadena de caracteres anchos que representa el editor de software; Use **null** para usar cualquier CA disponible.</span><span class="sxs-lookup"><span data-stu-id="a1021-132">A pointer to a wide character string that represents the software publisher; use **NULL** to use any available CA.</span></span>

</dd> <dt>

<span data-ttu-id="a1021-133">**szProgramName**</span><span class="sxs-lookup"><span data-stu-id="a1021-133">**szProgramName**</span></span>
</dt> <dd>

<span data-ttu-id="a1021-134">Puntero a una cadena de caracteres anchos que representa el nombre del programa; Use **null** para usar cualquier CA disponible.</span><span class="sxs-lookup"><span data-stu-id="a1021-134">A pointer to a wide character string that represents the program name; use **NULL** to use any available CA.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1021-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1021-135">Requirements</span></span>



| <span data-ttu-id="a1021-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1021-136">Requirement</span></span> | <span data-ttu-id="a1021-137">Value</span><span class="sxs-lookup"><span data-stu-id="a1021-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a1021-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1021-138">Header</span></span><br/> | <dl> <span data-ttu-id="a1021-139"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1021-139"><dt>Pstore.h</dt></span></span> </dl> |



 

 
