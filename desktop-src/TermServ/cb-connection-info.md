---
title: CB_CONNECTION_INFO estructura (Cbclient. h)
description: Contiene información sobre una solicitud de conexión entrante.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- Estructura de CB_CONNECTION_INFO Servicios de Escritorio remoto
- PCB_CONNECTION_INFO puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422090"
---
# <a name="cb_connection_info-structure"></a><span data-ttu-id="0f326-105">Estructura de información de \_ conexión CB \_</span><span class="sxs-lookup"><span data-stu-id="0f326-105">CB\_CONNECTION\_INFO structure</span></span>

<span data-ttu-id="0f326-106">Contiene información sobre una solicitud de conexión entrante.</span><span class="sxs-lookup"><span data-stu-id="0f326-106">Contains information about an incoming connection request.</span></span> <span data-ttu-id="0f326-107">Esta estructura se usa con el método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="0f326-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f326-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f326-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a><span data-ttu-id="0f326-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f326-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f326-110">**UserName**</span><span class="sxs-lookup"><span data-stu-id="0f326-110">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="0f326-111">Nombre del usuario que solicita una sesión.</span><span class="sxs-lookup"><span data-stu-id="0f326-111">The name of the user requesting a session.</span></span>

</dd> <dt>

<span data-ttu-id="0f326-112">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="0f326-112">**Domain**</span></span>
</dt> <dd>

<span data-ttu-id="0f326-113">Nombre del dominio del que es miembro el nombre de **usuario** .</span><span class="sxs-lookup"><span data-stu-id="0f326-113">The name of the domain that **UserName** is a member of.</span></span>

</dd> <dt>

<span data-ttu-id="0f326-114">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="0f326-114">**InitialProgram**</span></span>
</dt> <dd>

<span data-ttu-id="0f326-115">La ruta de acceso completa y el nombre de archivo del programa inicial que se inicia cuando se inicia la sesión.</span><span class="sxs-lookup"><span data-stu-id="0f326-115">The fully qualified path and file name of the initial program that is started when the session is started.</span></span> <span data-ttu-id="0f326-116">Establezca este miembro en una cadena vacía si no se debe iniciar ningún programa inicial.</span><span class="sxs-lookup"><span data-stu-id="0f326-116">Set this member to an empty string if no initial program should be started.</span></span>

</dd> <dt>

<span data-ttu-id="0f326-117">**Recurso**</span><span class="sxs-lookup"><span data-stu-id="0f326-117">**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="0f326-118">Valor de la enumeración del [**\_ \_ tipo de recurso CB**](cb-resource-type.md) que especifica el tipo de recurso al que se está conectando la conexión entrante.</span><span class="sxs-lookup"><span data-stu-id="0f326-118">A value of the [**CB\_RESOURCE\_TYPE**](cb-resource-type.md) enumeration that specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="0f326-119">Si el miembro **plugInName** es **null**, el agente de conexión a escritorio remoto usa este miembro para determinar el complemento que se debe invocar para determinar el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="0f326-119">If the **PluginName** member is **NULL**, this member is used to by the Remote Desktop Connection Broker to determine which plug-in to invoke for determining the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="0f326-120">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="0f326-120">**PluginName**</span></span>
</dt> <dd>

<span data-ttu-id="0f326-121">Nombre del complemento que se va a invocar para determinar el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="0f326-121">The name of the plug-in to invoke to determine the target computer.</span></span> <span data-ttu-id="0f326-122">Si este parámetro es **null**, el miembro de **recurso** se utiliza para determinar el complemento que se va a invocar.</span><span class="sxs-lookup"><span data-stu-id="0f326-122">If this parameter is **NULL**, the **Resource** member is used to determine which plug-in to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="0f326-123">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="0f326-123">**FarmName**</span></span>
</dt> <dd>

<span data-ttu-id="0f326-124">El nombre de la granja que contiene los equipos, uno de los cuales será el equipo de destino al que se redirigirá la conexión.</span><span class="sxs-lookup"><span data-stu-id="0f326-124">The name of the farm that contains the computers, one of which will be the target computer where the connection will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="0f326-125">**dwVendorInfoLength**</span><span class="sxs-lookup"><span data-stu-id="0f326-125">**dwVendorInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="0f326-126">Este miembro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0f326-126">This member is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="0f326-127">**pVendorSpecificInfo**</span><span class="sxs-lookup"><span data-stu-id="0f326-127">**pVendorSpecificInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0f326-128">Este miembro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0f326-128">This member is reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f326-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f326-129">Requirements</span></span>



| <span data-ttu-id="0f326-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f326-130">Requirement</span></span> | <span data-ttu-id="0f326-131">Value</span><span class="sxs-lookup"><span data-stu-id="0f326-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f326-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f326-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0f326-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0f326-133">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="0f326-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f326-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0f326-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f326-135">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="0f326-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f326-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f326-137"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f326-137"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f326-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f326-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f326-139">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="0f326-139">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





