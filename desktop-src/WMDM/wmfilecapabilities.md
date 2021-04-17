---
title: Estructura WMFILECAPABILITIES
description: La estructura WMFILECAPABILITIES describe el tipo MIME.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- Estructura WMFILECAPABILITIES Administrador de dispositivos Windows Media
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7657ddd15a4219a0d5f56dbadeffba2a9547bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698640"
---
# <a name="wmfilecapabilities-structure"></a><span data-ttu-id="39d67-104">Estructura WMFILECAPABILITIES</span><span class="sxs-lookup"><span data-stu-id="39d67-104">WMFILECAPABILITIES structure</span></span>

<span data-ttu-id="39d67-105">La estructura **WMFILECAPABILITIES** describe el tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="39d67-105">The **WMFILECAPABILITIES** structure describes the MIME type.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d67-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39d67-106">Syntax</span></span>


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a><span data-ttu-id="39d67-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="39d67-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="39d67-108">**pwszMimeType**</span><span class="sxs-lookup"><span data-stu-id="39d67-108">**pwszMimeType**</span></span>
</dt> <dd>

<span data-ttu-id="39d67-109">Tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="39d67-109">MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="39d67-110">**dwReserved**</span><span class="sxs-lookup"><span data-stu-id="39d67-110">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="39d67-111">**DWORD** reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="39d67-111">**DWORD** reserved for future use.</span></span> <span data-ttu-id="39d67-112">Se establece en cero (0).</span><span class="sxs-lookup"><span data-stu-id="39d67-112">Set to zero (0).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39d67-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39d67-113">Requirements</span></span>



| <span data-ttu-id="39d67-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="39d67-114">Requirement</span></span> | <span data-ttu-id="39d67-115">Value</span><span class="sxs-lookup"><span data-stu-id="39d67-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="39d67-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39d67-116">Header</span></span><br/> | <dl> <span data-ttu-id="39d67-117"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39d67-117"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39d67-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="39d67-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d67-119">**IWMDMDevice2::GetFormatSupport2**</span><span class="sxs-lookup"><span data-stu-id="39d67-119">**IWMDMDevice2::GetFormatSupport2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[<span data-ttu-id="39d67-120">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="39d67-120">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





