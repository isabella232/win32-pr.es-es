---
description: 'Libera los identificadores de Plug and Play (PnP) recuperados por los métodos IPortableDeviceManager:: GetDevices o IPortableDeviceServiceManager:: GetDeviceServices.'
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: Función FreePortableDevicePnPIDs (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 58bb5fa33007ed0e167226edf7078d08c2e5c3de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278005"
---
# <a name="freeportabledevicepnpids-function"></a><span data-ttu-id="ba8a2-103">FreePortableDevicePnPIDs función)</span><span class="sxs-lookup"><span data-stu-id="ba8a2-103">FreePortableDevicePnPIDs function</span></span>

<span data-ttu-id="ba8a2-104">La función auxiliar **FreePortableDevicePnPIDs** libera los identificadores plug and Play (PNP) recuperados por los métodos IPortableDeviceManager: [**: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) o [**IPortableDeviceServiceManager:: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .</span><span class="sxs-lookup"><span data-stu-id="ba8a2-104">The **FreePortableDevicePnPIDs** helper function frees the Plug and Play (PnP) identifiers that are retrieved by the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) or [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba8a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba8a2-105">Syntax</span></span>


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a><span data-ttu-id="ba8a2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba8a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba8a2-107">*pPnPIDs*</span><span class="sxs-lookup"><span data-stu-id="ba8a2-107">*pPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="ba8a2-108">Matriz de identificadores de Plug and Play (PnP) que se van a liberar.</span><span class="sxs-lookup"><span data-stu-id="ba8a2-108">The array of Plug and Play (PnP) identifiers to be freed.</span></span>

</dd> <dt>

<span data-ttu-id="ba8a2-109">*cPnPIDs*</span><span class="sxs-lookup"><span data-stu-id="ba8a2-109">*cPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="ba8a2-110">El número de identificadores de la matriz especificado por el parámetro *pPnPIDs* .</span><span class="sxs-lookup"><span data-stu-id="ba8a2-110">The number of identifiers in the array specified by the *pPnPIDs* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba8a2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba8a2-111">Return value</span></span>

<span data-ttu-id="ba8a2-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ba8a2-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba8a2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba8a2-113">Remarks</span></span>

<span data-ttu-id="ba8a2-114">La aplicación es responsable de liberar la matriz de punteros que asigna.</span><span class="sxs-lookup"><span data-stu-id="ba8a2-114">The application is responsible for freeing the array of pointers that it allocates.</span></span>

## <a name="examples"></a><span data-ttu-id="ba8a2-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ba8a2-115">Examples</span></span>


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a><span data-ttu-id="ba8a2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba8a2-116">Requirements</span></span>



| <span data-ttu-id="ba8a2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba8a2-117">Requirement</span></span> | <span data-ttu-id="ba8a2-118">Value</span><span class="sxs-lookup"><span data-stu-id="ba8a2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba8a2-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba8a2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ba8a2-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="ba8a2-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="ba8a2-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba8a2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ba8a2-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ba8a2-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ba8a2-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba8a2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba8a2-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba8a2-124"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




