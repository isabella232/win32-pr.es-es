---
description: Recupera los siguientes objetos IPortableDeviceConnector en la secuencia de enumeración.
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
title: 'IEnumPortableDeviceConnectors:: Next (método) (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Next
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 709e938c28f9bf09e34d918eea7be3029c7a11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716883"
---
# <a name="ienumportabledeviceconnectorsnext-method"></a><span data-ttu-id="cb6d0-103">IEnumPortableDeviceConnectors:: Next (método)</span><span class="sxs-lookup"><span data-stu-id="cb6d0-103">IEnumPortableDeviceConnectors::Next method</span></span>

<span data-ttu-id="cb6d0-104">El método **siguiente** recupera los siguientes objetos [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-104">The **Next** method retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb6d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb6d0-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      UINT32                   cRequested,
  [out]     IPortableDeviceConnector **pConnectors,
  [in, out] UINT32                   *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="cb6d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb6d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb6d0-107">*cRequested* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb6d0-107">*cRequested* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb6d0-108">El número de dispositivos solicitados.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-108">The number of requested devices.</span></span> <span data-ttu-id="cb6d0-109">Este valor también indica el número de elementos de la matriz asignada por el llamador que especifica el parámetro *pConnectors* .</span><span class="sxs-lookup"><span data-stu-id="cb6d0-109">This value also indicates the number of elements in the caller-allocated array specified by the *pConnectors* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cb6d0-110">*pConnectors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb6d0-110">*pConnectors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb6d0-111">Una matriz de punteros [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , cada uno de los cuales especifica un dispositivo Bluetooth MTP emparejado.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-111">An array of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) pointers, each specifying a paired MTP Bluetooth device.</span></span> <span data-ttu-id="cb6d0-112">El autor de la llamada debe asignar una matriz de punteros **IPortableDeviceConnector** , con la longitud de la matriz especificada por el parámetro *cRequested* .</span><span class="sxs-lookup"><span data-stu-id="cb6d0-112">The caller must allocate an array of **IPortableDeviceConnector** pointers, with the array length specified by the *cRequested* parameter.</span></span> <span data-ttu-id="cb6d0-113">Si la devolución es correcta, el llamador debe liberar tanto la matriz como los punteros devueltos.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-113">On successful return, the caller must free both the array and the returned pointers.</span></span> <span data-ttu-id="cb6d0-114">Las interfaces **IPortableDeviceConnector** se liberan llamando al método **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="cb6d0-114">The **IPortableDeviceConnector** interfaces are freed by calling the **IUnknown::Release** method.</span></span>

</dd> <dt>

<span data-ttu-id="cb6d0-115">*pcFetched* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cb6d0-115">*pcFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb6d0-116">Número de interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) que se recuperan realmente.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-116">The number of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces that are actually retrieved.</span></span> <span data-ttu-id="cb6d0-117">Si no se recupera ninguna interfaz **IPortableDeviceConnector** y el valor devuelto es **S \_ false**, no hay más interfaces **IPortableDeviceConnector** para enumerar.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-117">If no **IPortableDeviceConnector** interfaces are retrieved and the return value is **S\_FALSE**, there are no more **IPortableDeviceConnector** interfaces to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb6d0-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb6d0-118">Return value</span></span>

<span data-ttu-id="cb6d0-119">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cb6d0-120">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cb6d0-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cb6d0-121">Return code</span></span>                                                                             | <span data-ttu-id="cb6d0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb6d0-122">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb6d0-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="cb6d0-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="cb6d0-124">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-124">The method succeeded.</span></span><br/>                                 |
| <dl> <span data-ttu-id="cb6d0-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="cb6d0-125"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="cb6d0-126">No hay más dispositivos Bluetooth MTP para enumerar.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-126">There are no more MTP Bluetooth devices to enumerate.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="cb6d0-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cb6d0-127">Examples</span></span>

<span data-ttu-id="cb6d0-128">En el ejemplo siguiente se muestra el uso de este método para enumerar los dispositivos MTP/Bluetooth emparejados y para enviar una solicitud de conexión asincrónica a cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-128">The following example demonstrates the use of this method to enumerate paired MTP/Bluetooth devices, and to send an asynchronous connection request to each.</span></span>


```C++
IEnumPortableDeviceConnectors* pEnum = NULL;
    HRESULT hrEnum = S_OK;
 HRESULT hr = CoCreateInstance(CLSID_EnumBthMtpConnectors, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pEnum));
    if (SUCCEEDED(hr))
{
  while (S_OK == hrEnum)
    {
       UINT32  uFetched        = 0;
       LPWSTR  wszDevicePnPID  = NULL;
       IPortableDeviceConnector* pDevice = NULL;
       hrEnum = pEnum->Next(1, &spDevice, &uFetched);
       if (hrEnum == S_OK && uFetched == 1)
        {
          // Send an asynchronous connect request.  
          hr = pDevice ->Connect(NULL);
          // Release the device when done
          pDevice->Release();
          pDevice = NULL;
        }
     }  // while S_OK == hrEnum
  // Release the enumerator when done
    if (pEnum)
    {
     pEnum->Release();
     pEnum = NULL;
   }
    }
       
```



## <a name="requirements"></a><span data-ttu-id="cb6d0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb6d0-129">Requirements</span></span>



| <span data-ttu-id="cb6d0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb6d0-130">Requirement</span></span> | <span data-ttu-id="cb6d0-131">Value</span><span class="sxs-lookup"><span data-stu-id="cb6d0-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6d0-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb6d0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cb6d0-133">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb6d0-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="cb6d0-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb6d0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cb6d0-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cb6d0-135">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="cb6d0-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb6d0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb6d0-137"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb6d0-137"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="cb6d0-138">IDL</span><span class="sxs-lookup"><span data-stu-id="cb6d0-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb6d0-139"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb6d0-139"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="cb6d0-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb6d0-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="cb6d0-141"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb6d0-141"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="cb6d0-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb6d0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb6d0-143">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="cb6d0-143">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




