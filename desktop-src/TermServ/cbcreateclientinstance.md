---
title: Función CBCreateClientInstance (Cbclient. h)
description: Crea una instancia del cliente RPC de Conexión a Escritorio remoto Broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función CBCreateClientInstance
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681232"
---
# <a name="cbcreateclientinstance-function"></a><span data-ttu-id="21ed5-104">CBCreateClientInstance función)</span><span class="sxs-lookup"><span data-stu-id="21ed5-104">CBCreateClientInstance function</span></span>

<span data-ttu-id="21ed5-105">Crea una instancia del cliente RPC de Conexión a Escritorio remoto Broker.</span><span class="sxs-lookup"><span data-stu-id="21ed5-105">Creates an instance of the Remote Desktop Connection Broker RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="21ed5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21ed5-106">Syntax</span></span>


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a><span data-ttu-id="21ed5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21ed5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21ed5-108">*Versión* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="21ed5-108">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21ed5-109">Especifica la versión de la interfaz de cliente de Conexión a Escritorio remoto Broker que se solicita.</span><span class="sxs-lookup"><span data-stu-id="21ed5-109">Specifies the version of the Remote Desktop Connection Broker client interface being requested.</span></span> <span data-ttu-id="21ed5-110">Debe ser el siguiente valor.</span><span class="sxs-lookup"><span data-stu-id="21ed5-110">This must be the following value.</span></span>

<dt>

<span data-ttu-id="21ed5-111">1</span><span class="sxs-lookup"><span data-stu-id="21ed5-111">1</span></span>
</dt> <dd>

<span data-ttu-id="21ed5-112">Versión 1 del cliente del agente de Conexión a Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="21ed5-112">Version 1 of the Remote Desktop Connection Broker client.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="21ed5-113">*ppCbClient* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="21ed5-113">*ppCbClient* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21ed5-114">Dirección de un puntero de interfaz [**IConnectionBrokerClient**](iconnectionbrokerclient.md) que recibe el objeto de cliente de conexión a escritorio remoto Broker.</span><span class="sxs-lookup"><span data-stu-id="21ed5-114">The address of an [**IConnectionBrokerClient**](iconnectionbrokerclient.md) interface pointer that receives the Remote Desktop Connection Broker client object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21ed5-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21ed5-115">Return value</span></span>

<span data-ttu-id="21ed5-116">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="21ed5-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21ed5-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21ed5-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="21ed5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21ed5-118">Requirements</span></span>



| <span data-ttu-id="21ed5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="21ed5-119">Requirement</span></span> | <span data-ttu-id="21ed5-120">Value</span><span class="sxs-lookup"><span data-stu-id="21ed5-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21ed5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21ed5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="21ed5-122"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="21ed5-122"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="21ed5-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21ed5-123">Library</span></span><br/> | <dl> <span data-ttu-id="21ed5-124"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21ed5-124"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="21ed5-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21ed5-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="21ed5-126"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21ed5-126"><dt>Cbclient.dll</dt></span></span> </dl> |



 

 





