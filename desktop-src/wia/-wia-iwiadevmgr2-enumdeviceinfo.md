---
description: Crea un enumerador de información de propiedad para cada dispositivo de adquisición de imágenes de Windows (WIA) 2,0 disponible.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'IWiaDevMgr2:: EnumDeviceInfo (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bd9e9281b625f4cec5377537d82a304045b95a3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810778"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a><span data-ttu-id="10120-103">IWiaDevMgr2:: EnumDeviceInfo (método)</span><span class="sxs-lookup"><span data-stu-id="10120-103">IWiaDevMgr2::EnumDeviceInfo method</span></span>

<span data-ttu-id="10120-104">Crea un enumerador de información de propiedad para cada dispositivo de adquisición de imágenes de Windows (WIA) 2,0 disponible.</span><span class="sxs-lookup"><span data-stu-id="10120-104">Creates an enumerator of property information for each available Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="10120-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10120-105">Syntax</span></span>


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="10120-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10120-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10120-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="10120-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10120-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="10120-108">Type: **LONG**</span></span>

<span data-ttu-id="10120-109">Especifica el tipo de dispositivos WIA 2,0 que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="10120-109">Specifies the type of WIA 2.0 devices to enumerate.</span></span>

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span data-ttu-id="10120-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**\_ \_ enumeración local de la DevInfo de WIA \_**</span><span class="sxs-lookup"><span data-stu-id="10120-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA\_DEVINFO\_ENUM\_LOCAL**</span></span>


</dt> <dd>

<span data-ttu-id="10120-111">Solo se enumeran los dispositivos de analizador activos conectados localmente.</span><span class="sxs-lookup"><span data-stu-id="10120-111">Only locally connected active scanner devices are enumerated.</span></span>

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span data-ttu-id="10120-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**\_ \_ enumeración todo en la DevInfo de WIA \_**</span><span class="sxs-lookup"><span data-stu-id="10120-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA\_DEVINFO\_ENUM\_ALL**</span></span>


</dt> <dd>

<span data-ttu-id="10120-113">Todos los dispositivos se enumeran, tanto de forma local como remota, incluidos los dispositivos inactivos (desconectados) y los dispositivos solo de STI heredados.</span><span class="sxs-lookup"><span data-stu-id="10120-113">All devices are enumerated, both locally and remote, including inactive (disconnected) devices and legacy STI-only devices.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="10120-114">*ppIEnum* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="10120-114">*ppIEnum* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="10120-115">Tipo: **[ **IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="10120-115">Type: **[**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span></span>

<span data-ttu-id="10120-116">Recibe la dirección de un puntero a la interfaz de [**\_ \_ información de desarrollo de IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="10120-116">Receives the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10120-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10120-117">Return value</span></span>

<span data-ttu-id="10120-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="10120-118">Type: **HRESULT**</span></span>

<span data-ttu-id="10120-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="10120-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="10120-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="10120-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="10120-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10120-121">Remarks</span></span>

<span data-ttu-id="10120-122">El método **IWiaDevMgr2:: EnumDeviceInfo** crea un objeto de enumerador que admite la interfaz de [**información de \_ desarrollo \_ de IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="10120-122">The **IWiaDevMgr2::EnumDeviceInfo** method creates an enumerator object that supports the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span> <span data-ttu-id="10120-123">El método almacena un puntero a la interfaz **IEnumWIA \_ dev \_ info** en el parámetro *ppIEnum*.</span><span class="sxs-lookup"><span data-stu-id="10120-123">The method stores a pointer to the **IEnumWIA\_DEV\_INFO** interface in the parameter *ppIEnum*.</span></span> <span data-ttu-id="10120-124">Las aplicaciones pueden usar el puntero de la interfaz de **IEnumWIA \_ dev \_ info** para enumerar las propiedades de cada dispositivo WIA 2,0 conectado al equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="10120-124">Applications can use the **IEnumWIA\_DEV\_INFO** interface pointer to enumerate the properties of each WIA 2.0 device attached to the user's computer.</span></span>

<span data-ttu-id="10120-125">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="10120-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="10120-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10120-126">Requirements</span></span>



| <span data-ttu-id="10120-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="10120-127">Requirement</span></span> | <span data-ttu-id="10120-128">Value</span><span class="sxs-lookup"><span data-stu-id="10120-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="10120-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10120-129">Minimum supported client</span></span><br/> | <span data-ttu-id="10120-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="10120-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="10120-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10120-131">Minimum supported server</span></span><br/> | <span data-ttu-id="10120-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="10120-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="10120-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10120-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="10120-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="10120-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="10120-135">IDL</span><span class="sxs-lookup"><span data-stu-id="10120-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="10120-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10120-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
