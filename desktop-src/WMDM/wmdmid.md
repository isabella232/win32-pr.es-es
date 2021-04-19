---
title: Estructura WMDMID
description: La estructura WMDMID describe los números de serie y los ID. de grupo.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Estructura WMDMID Administrador de dispositivos Windows Media
- Puntero de estructura PWMDMID Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700264"
---
# <a name="wmdmid-structure"></a><span data-ttu-id="13107-105">Estructura WMDMID</span><span class="sxs-lookup"><span data-stu-id="13107-105">WMDMID structure</span></span>

<span data-ttu-id="13107-106">La estructura **WMDMID** describe los números de serie y los ID. de grupo.</span><span class="sxs-lookup"><span data-stu-id="13107-106">The **WMDMID** structure describes serial numbers and group IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="13107-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13107-107">Syntax</span></span>


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a><span data-ttu-id="13107-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="13107-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="13107-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="13107-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="13107-110">Tamaño de la estructura **WMDMID** , en bytes.</span><span class="sxs-lookup"><span data-stu-id="13107-110">Size of the **WMDMID** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="13107-111">**dwVendorID**</span><span class="sxs-lookup"><span data-stu-id="13107-111">**dwVendorID**</span></span>
</dt> <dd>

<span data-ttu-id="13107-112">**DWORD** que contiene el número de ID. registrado del proveedor.</span><span class="sxs-lookup"><span data-stu-id="13107-112">**DWORD** containing the registered ID number of the vendor.</span></span> <span data-ttu-id="13107-113">Contiene cero si no está en uso.</span><span class="sxs-lookup"><span data-stu-id="13107-113">Contains zero if not in use.</span></span>

</dd> <dt>

<span data-ttu-id="13107-114">**\[longitud de WMDMID de PID \_\]**</span><span class="sxs-lookup"><span data-stu-id="13107-114">**pID\[WMDMID\_LENGTH\]**</span></span>
</dt> <dd>

<span data-ttu-id="13107-115">Puntero a una matriz de bytes que contiene el número de serie.</span><span class="sxs-lookup"><span data-stu-id="13107-115">Pointer to an array of bytes containing the serial number.</span></span> <span data-ttu-id="13107-116">El número de serie es una cadena de valores de bytes que no tienen ningún formato estándar.</span><span class="sxs-lookup"><span data-stu-id="13107-116">The serial number is a string of byte values that have no standard format.</span></span> <span data-ttu-id="13107-117">Tenga en cuenta que no se trata de un valor de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="13107-117">Note that this is not a wide-character value.</span></span> <span data-ttu-id="13107-118">**WMDMID \_ LENGTH** es un valor constante definido en mswmdm. h.</span><span class="sxs-lookup"><span data-stu-id="13107-118">**WMDMID\_LENGTH** is a constant value defined in mswmdm.h.</span></span>

</dd> <dt>

<span data-ttu-id="13107-119">**SerialNumberLength**</span><span class="sxs-lookup"><span data-stu-id="13107-119">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="13107-120">Longitud real del número de serie devuelto, en bytes.</span><span class="sxs-lookup"><span data-stu-id="13107-120">Actual length of the serial number returned, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13107-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13107-121">Requirements</span></span>



| <span data-ttu-id="13107-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="13107-122">Requirement</span></span> | <span data-ttu-id="13107-123">Value</span><span class="sxs-lookup"><span data-stu-id="13107-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="13107-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13107-124">Header</span></span><br/> | <dl> <span data-ttu-id="13107-125"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13107-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13107-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="13107-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13107-127">**IMDSPDevice::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="13107-127">**IMDSPDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="13107-128">**IMDSPStorageGlobals::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="13107-128">**IMDSPStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="13107-129">**IWMDMDevice::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="13107-129">**IWMDMDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="13107-130">**IWMDMStorageGlobals::GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="13107-130">**IWMDMStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="13107-131">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="13107-131">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





