---
title: Estructura WMDMRIGHTS
description: La estructura WMDMRIGHTS describe los derechos de uso de contenido.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Estructura WMDMRIGHTS Administrador de dispositivos Windows Media
- Puntero de estructura PWMDMRIGHTS Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698689"
---
# <a name="wmdmrights-structure"></a><span data-ttu-id="5d8b1-105">Estructura WMDMRIGHTS</span><span class="sxs-lookup"><span data-stu-id="5d8b1-105">WMDMRIGHTS structure</span></span>

<span data-ttu-id="5d8b1-106">La estructura **WMDMRIGHTS** describe los derechos de uso de contenido.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-106">The **WMDMRIGHTS** structure describes content-use rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d8b1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d8b1-107">Syntax</span></span>


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a><span data-ttu-id="5d8b1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5d8b1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d8b1-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="5d8b1-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="5d8b1-110">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-110">Size of the structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5d8b1-111">**dwContentType**</span><span class="sxs-lookup"><span data-stu-id="5d8b1-111">**dwContentType**</span></span>
</dt> <dd>

<span data-ttu-id="5d8b1-112">**DWORD** que contiene el tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-112">**DWORD** containing the type of content.</span></span>

</dd> <dt>

<span data-ttu-id="5d8b1-113">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="5d8b1-113">**fuFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5d8b1-114">Campo de bits que especifica las opciones de derechos que se usan para el contenido.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-114">Bit field specifying the rights options in use for the content.</span></span>



| <span data-ttu-id="5d8b1-115">Value</span><span class="sxs-lookup"><span data-stu-id="5d8b1-115">Value</span></span>                        | <span data-ttu-id="5d8b1-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d8b1-116">Description</span></span>                                  |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="5d8b1-117">derechos de WMDM \_ \_ PLAYBACKCOUNT</span><span class="sxs-lookup"><span data-stu-id="5d8b1-117">WMDM\_RIGHTS\_PLAYBACKCOUNT</span></span>  | <span data-ttu-id="5d8b1-118">Número de veces que se puede reproducir el archivo.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-118">Number of times that the file can be played.</span></span> |
| <span data-ttu-id="5d8b1-119">\_EXPIRATIONDATE Rights de WMDM \_</span><span class="sxs-lookup"><span data-stu-id="5d8b1-119">WMDM\_RIGHTS\_EXPIRATIONDATE</span></span> | <span data-ttu-id="5d8b1-120">Fecha de expiración del archivo.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-120">Expiration date of the file.</span></span>                 |
| <span data-ttu-id="5d8b1-121">derechos de WMDM \_ \_ FREESERIALIDS</span><span class="sxs-lookup"><span data-stu-id="5d8b1-121">WMDM\_RIGHTS\_FREESERIALIDS</span></span>  | <span data-ttu-id="5d8b1-122">Identificador de serie libre del archivo.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-122">Free serial identifier of the file.</span></span>          |
| <span data-ttu-id="5d8b1-123">Grupo del GROUPID de \_ derechos de WMDM \_</span><span class="sxs-lookup"><span data-stu-id="5d8b1-123">WMDM\_RIGHTS\_GROUPID Group</span></span>  | <span data-ttu-id="5d8b1-124">Identificador del archivo.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-124">Identifier of the file.</span></span>                      |
| <span data-ttu-id="5d8b1-125">derechos de WMDM \_ \_ NAMEDSERIALIDS</span><span class="sxs-lookup"><span data-stu-id="5d8b1-125">WMDM\_RIGHTS\_NAMEDSERIALIDS</span></span> | <span data-ttu-id="5d8b1-126">Identificador de serie con nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-126">Named serial identifier of the file.</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5d8b1-127">**fuRights**</span><span class="sxs-lookup"><span data-stu-id="5d8b1-127">**fuRights**</span></span>
</dt> <dd>

<span data-ttu-id="5d8b1-128">Campo de bits que contiene los bits de derechos para el contenido.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-128">Bit field containing the rights bits for the content.</span></span>



| <span data-ttu-id="5d8b1-129">Value</span><span class="sxs-lookup"><span data-stu-id="5d8b1-129">Value</span></span>                                     | <span data-ttu-id="5d8b1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d8b1-130">Description</span></span>                                   |
|-------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="5d8b1-131">\_ \_ juego de derechos \_ de WMDM en \_ PC</span><span class="sxs-lookup"><span data-stu-id="5d8b1-131">WMDM\_RIGHTS\_PLAY\_ON\_PC</span></span>                | <span data-ttu-id="5d8b1-132">El contenido se puede reproducir en un equipo personal.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-132">Content can be played on a personal computer.</span></span> |
| <span data-ttu-id="5d8b1-133">\_ \_ copia de derechos \_ de WMDM en un \_ dispositivo que no es de \_ SDMI \_</span><span class="sxs-lookup"><span data-stu-id="5d8b1-133">WMDM\_RIGHTS\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="5d8b1-134">El contenido se puede copiar en un dispositivo que no es de SDMI.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-134">Content can be copied to a non-SDMI device.</span></span>   |
| <span data-ttu-id="5d8b1-135">\_ \_ copia de derechos \_ de WMDM en \_ CD</span><span class="sxs-lookup"><span data-stu-id="5d8b1-135">WMDM\_RIGHTS\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="5d8b1-136">El contenido se puede copiar en un CD.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-136">Content can be copied to a CD.</span></span>                |
| <span data-ttu-id="5d8b1-137">\_ \_ copia de derechos \_ de WMDM en el \_ dispositivo de SDMI \_</span><span class="sxs-lookup"><span data-stu-id="5d8b1-137">WMDM\_RIGHTS\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="5d8b1-138">El contenido se puede copiar en un dispositivo de SDMI.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-138">Content can be copied to an SDMI device.</span></span>      |



 

</dd> <dt>

<span data-ttu-id="5d8b1-139">**dwAppSec**</span><span class="sxs-lookup"><span data-stu-id="5d8b1-139">**dwAppSec**</span></span>
</dt> <dd>

<span data-ttu-id="5d8b1-140">Matriz de bytes que especifica el nivel mínimo de seguridad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-140">Byte array that specifies the minimum level of application security.</span></span>

</dd> <dt>

<span data-ttu-id="5d8b1-141">**dwPlaybackCount**</span><span class="sxs-lookup"><span data-stu-id="5d8b1-141">**dwPlaybackCount**</span></span>
</dt> <dd>

<span data-ttu-id="5d8b1-142">**DWORD** que contiene el número de veces que se puede representar el contenido.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-142">**DWORD** containing the number of remaining times that the content can be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="5d8b1-143">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="5d8b1-143">**ExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="5d8b1-144">Estructura [**WMDMDATETIME**](wmdmdatetime.md) que contiene la fecha y hora de expiración del contenido.</span><span class="sxs-lookup"><span data-stu-id="5d8b1-144">[**WMDMDATETIME**](wmdmdatetime.md) structure containing the expiration date and time for the content.</span></span> <span data-ttu-id="5d8b1-145">Si la licencia no tiene fecha de expiración, el miembro **wYear** se establece en 0xFFFF y se omiten todos los demás miembros de **WMDMDATETIME** .</span><span class="sxs-lookup"><span data-stu-id="5d8b1-145">If the license has no expiration date, the **wYear** member is set to 0xFFFF, and all other members of **WMDMDATETIME** are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d8b1-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d8b1-146">Requirements</span></span>



| <span data-ttu-id="5d8b1-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d8b1-147">Requirement</span></span> | <span data-ttu-id="5d8b1-148">Value</span><span class="sxs-lookup"><span data-stu-id="5d8b1-148">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5d8b1-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d8b1-149">Header</span></span><br/> | <dl> <span data-ttu-id="5d8b1-150"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d8b1-150"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d8b1-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d8b1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d8b1-152">**IMDSPStorage::GetRights**</span><span class="sxs-lookup"><span data-stu-id="5d8b1-152">**IMDSPStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[<span data-ttu-id="5d8b1-153">**IWMDMStorage::GetRights**</span><span class="sxs-lookup"><span data-stu-id="5d8b1-153">**IWMDMStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[<span data-ttu-id="5d8b1-154">**WMDMDATETIME**</span><span class="sxs-lookup"><span data-stu-id="5d8b1-154">**WMDMDATETIME**</span></span>](wmdmdatetime.md)
</dt> <dt>

[<span data-ttu-id="5d8b1-155">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="5d8b1-155">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





