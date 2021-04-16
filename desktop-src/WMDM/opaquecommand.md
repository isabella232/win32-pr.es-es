---
title: Estructura OPAQUECOMMAND
description: La estructura OPAQUECOMMAND contiene los datos de los comandos que se pasan a través de Windows Media Administrador de dispositivos a un dispositivo, pero que no están diseñados para ser actuados por Windows Media Administrador de dispositivos.
ms.assetid: 5b39cf07-2816-4615-a754-e3f0c57bf4ce
keywords:
- Estructura OPAQUECOMMAND Administrador de dispositivos Windows Media
- estructura Administrador de dispositivos Windows Media
topic_type:
- apiref
api_name:
- OPAQUECOMMAND
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672147cb99336f95a1ced88a3cc6b8df977aec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699732"
---
# <a name="opaquecommand-structure"></a><span data-ttu-id="f4c5b-105">Estructura OPAQUECOMMAND</span><span class="sxs-lookup"><span data-stu-id="f4c5b-105">OPAQUECOMMAND structure</span></span>

<span data-ttu-id="f4c5b-106">La estructura **OPAQUECOMMAND** contiene los datos de los comandos que se pasan a través de windows media administrador de dispositivos a un dispositivo, pero que no están diseñados para ser actuados por windows media administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-106">The **OPAQUECOMMAND** structure contains data for commands that are passed through Windows Media Device Manager to a device but are not intended to be acted upon by Windows Media Device Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c5b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4c5b-107">Syntax</span></span>


```C++
typedef struct OPAQUECOMMAND {
  GUID  guidCommand;
  DWORD dwDataLen;
  BYTE  *pData;
  BYTE  abMAC[20];
} ;
```



## <a name="members"></a><span data-ttu-id="f4c5b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f4c5b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4c5b-109">**guidCommand**</span><span class="sxs-lookup"><span data-stu-id="f4c5b-109">**guidCommand**</span></span>
</dt> <dd>

<span data-ttu-id="f4c5b-110">**GUID** que representa el comando solicitado.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-110">**GUID** representing the requested command.</span></span>

</dd> <dt>

<span data-ttu-id="f4c5b-111">**dwDataLen**</span><span class="sxs-lookup"><span data-stu-id="f4c5b-111">**dwDataLen**</span></span>
</dt> <dd>

<span data-ttu-id="f4c5b-112">Longitud de los datos a los que se redirige *pdata* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-112">Length of the data to which *pData* points, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f4c5b-113">**pData**</span><span class="sxs-lookup"><span data-stu-id="f4c5b-113">**pData**</span></span>
</dt> <dd>

<span data-ttu-id="f4c5b-114">Datos necesarios para ejecutar el comando o los datos devueltos por el comando.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-114">Data required to execute the command, and/or data returned by the command.</span></span>

</dd> <dt>

<span data-ttu-id="f4c5b-115">**abMAC \[ 20\]**</span><span class="sxs-lookup"><span data-stu-id="f4c5b-115">**abMAC\[20\]**</span></span>
</dt> <dd>

<span data-ttu-id="f4c5b-116">Este código de autenticación de mensajes (MAC) debe incluir el miembro **guidCommand** , los datos a los que apunta *pdwDataLen* y los datos a los que se señala *pdata* , si los hay.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-116">This message authentication code (MAC) should include the **guidCommand** member, the data to which *pdwDataLen* points, and the data to which *pData* points, if any.</span></span> <span data-ttu-id="f4c5b-117">Si *pdata* es **null**, no se debe incluir en el equipo Mac.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-117">If *pData* is **NULL**, it must not be included in the MAC.</span></span> <span data-ttu-id="f4c5b-118">La \_ \_ longitud de Mac de WMDM se define como 20.</span><span class="sxs-lookup"><span data-stu-id="f4c5b-118">WMDM\_MAC\_LENGTH is defined as 20.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4c5b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4c5b-119">Requirements</span></span>



| <span data-ttu-id="f4c5b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4c5b-120">Requirement</span></span> | <span data-ttu-id="f4c5b-121">Value</span><span class="sxs-lookup"><span data-stu-id="f4c5b-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c5b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4c5b-122">Header</span></span><br/> | <dl> <span data-ttu-id="f4c5b-123"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4c5b-123"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4c5b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4c5b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c5b-125">**IMDSPDevice::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="f4c5b-125">**IMDSPDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="f4c5b-126">**IMDSPStorage::SendOpaqueCommands**</span><span class="sxs-lookup"><span data-stu-id="f4c5b-126">**IMDSPStorage::SendOpaqueCommands**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="f4c5b-127">**IWMDMDevice::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="f4c5b-127">**IWMDMDevice::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="f4c5b-128">**IWMDMStorage::SendOpaqueCommand**</span><span class="sxs-lookup"><span data-stu-id="f4c5b-128">**IWMDMStorage::SendOpaqueCommand**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)
</dt> <dt>

[<span data-ttu-id="f4c5b-129">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="f4c5b-129">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





