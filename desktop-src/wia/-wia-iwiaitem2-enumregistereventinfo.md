---
description: 'El método IWiaItem2:: EnumRegisterEventInfo crea un enumerador que puede usar para obtener información sobre los eventos para los que se registra una aplicación.'
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'IWiaItem2:: EnumRegisterEventInfo (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154401"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a><span data-ttu-id="9a251-103">IWiaItem2:: EnumRegisterEventInfo (método)</span><span class="sxs-lookup"><span data-stu-id="9a251-103">IWiaItem2::EnumRegisterEventInfo method</span></span>

<span data-ttu-id="9a251-104">El método **IWiaItem2:: EnumRegisterEventInfo** crea un enumerador que puede usar para obtener información sobre los eventos para los que se registra una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9a251-104">The **IWiaItem2::EnumRegisterEventInfo** method creates an enumerator that you can use to obtain information about events for which an application is registered.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a251-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a251-105">Syntax</span></span>


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="9a251-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a251-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a251-107">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9a251-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a251-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="9a251-108">Type: **LONG**</span></span>

<span data-ttu-id="9a251-109">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9a251-109">Not used.</span></span> <span data-ttu-id="9a251-110">Establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="9a251-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9a251-111">*pEventGUID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9a251-111">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a251-112">Tipo: \**const GUID \** _</span><span class="sxs-lookup"><span data-stu-id="9a251-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="9a251-113">Puntero a un identificador que especifica el evento de hardware para el que desea obtener información de registro.</span><span class="sxs-lookup"><span data-stu-id="9a251-113">Pointer to an identifier that specifies the hardware event for which you want to obtain registration information.</span></span>

</dd> <dt>

<span data-ttu-id="9a251-114">_ppIEnum \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9a251-114">_ppIEnum\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a251-115">Tipo: **[ **IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="9a251-115">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="9a251-116">La dirección de un puntero a la interfaz [**IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .</span><span class="sxs-lookup"><span data-stu-id="9a251-116">The address of a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a251-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a251-117">Return value</span></span>

<span data-ttu-id="9a251-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9a251-118">Type: **HRESULT**</span></span>

<span data-ttu-id="9a251-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9a251-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a251-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a251-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a251-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a251-121">Remarks</span></span>

<span data-ttu-id="9a251-122">Una aplicación llama a este método para crear un objeto de enumerador para la información de evento.</span><span class="sxs-lookup"><span data-stu-id="9a251-122">An application calls this method to create an enumerator object for the event information.</span></span> <span data-ttu-id="9a251-123">**IWiaItem2:: EnumRegisterEventInfo** almacena la dirección de la interfaz [**IEnumWIA \_ dev \_ caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) del objeto enumerador en el parámetro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="9a251-123">**IWiaItem2::EnumRegisterEventInfo** stores the address of the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface of the enumerator object in the *ppIEnum* parameter.</span></span> <span data-ttu-id="9a251-124">Después, el programa usa el puntero de interfaz para enumerar las propiedades del evento para el que se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="9a251-124">The program then uses the interface pointer to enumerate the properties of the event for which it is registered.</span></span>

<span data-ttu-id="9a251-125">Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="9a251-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a251-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a251-126">Requirements</span></span>



| <span data-ttu-id="9a251-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a251-127">Requirement</span></span> | <span data-ttu-id="9a251-128">Value</span><span class="sxs-lookup"><span data-stu-id="9a251-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9a251-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a251-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9a251-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9a251-130">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9a251-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a251-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9a251-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a251-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9a251-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a251-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a251-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a251-134"><dt>Wia.h</dt></span></span> </dl> |



 

 
