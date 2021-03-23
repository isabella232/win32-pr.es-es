---
title: Control de errores y eliminación de dispositivos en DirectML
description: En este tema se describe cómo depurar la eliminación de dispositivos DirectML y otras condiciones de error.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104549116"
---
# <a name="handling-errors-and-device-removal-in-directml"></a><span data-ttu-id="3c24d-103">Control de errores y eliminación de dispositivos en DirectML</span><span class="sxs-lookup"><span data-stu-id="3c24d-103">Handling errors and device-removal in DirectML</span></span>

## <a name="device-removal"></a><span data-ttu-id="3c24d-104">Eliminación de dispositivos</span><span class="sxs-lookup"><span data-stu-id="3c24d-104">Device-removal</span></span>

<span data-ttu-id="3c24d-105">Si se produce un error irrecuperable, el dispositivo DirectML puede entrar en el estado "quitado del dispositivo".</span><span class="sxs-lookup"><span data-stu-id="3c24d-105">If an unrecoverable error occurs, the DirectML device may enter a "device-removed" state.</span></span> <span data-ttu-id="3c24d-106">Los errores irrecuperables que causan la eliminación del dispositivo incluyen el uso no válido de la API (para los métodos que no devuelven un [**valor HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), los errores de controlador, los errores de hardware o las condiciones de memoria insuficiente (OOM).</span><span class="sxs-lookup"><span data-stu-id="3c24d-106">Unrecoverable errors that cause device-removal include invalid API usage (for methods that don't return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), driver error, hardware fault, or out-of-memory (OOM) conditions.</span></span>

<span data-ttu-id="3c24d-107">Cuando se quita un dispositivo DirectML, todas las llamadas a métodos en el dispositivo y todos los objetos creados por ese dispositivo se convierten en no operaciones.</span><span class="sxs-lookup"><span data-stu-id="3c24d-107">When a DirectML device is removed, all method calls on the device, and every object created by that device, become no-ops.</span></span> <span data-ttu-id="3c24d-108">En el caso de los métodos que devuelven un [**valor HRESULT**](/windows/desktop/com/structure-of-com-error-codes), se devuelve un código de error [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) .</span><span class="sxs-lookup"><span data-stu-id="3c24d-108">For methods that return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), a [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) error code is returned.</span></span> <span data-ttu-id="3c24d-109">Puede usar el método [ **IDMLDevice:: GetDeviceRemovedReason**](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) para comprobar si se ha quitado el dispositivo DirectML y para recuperar un código de error más detallado.</span><span class="sxs-lookup"><span data-stu-id="3c24d-109">You can use the [**IDMLDevice::GetDeviceRemovedReason** method](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) to check whether the DirectML device has been removed, and to retrieve a more detailed error code.</span></span>

<span data-ttu-id="3c24d-110">No se puede recuperar de la eliminación del dispositivo, excepto si se libera el dispositivo afectado y todos sus elementos secundarios y, a continuación, se vuelve a crear el dispositivo DirectML desde cero.</span><span class="sxs-lookup"><span data-stu-id="3c24d-110">You can't recover from device-removal except by releasing the affected device and all its children, then re-creating the DirectML device from scratch.</span></span>

<span data-ttu-id="3c24d-111">La eliminación de dispositivos del dispositivo Direct3D 12 subyacente también hace que se quite el dispositivo DirectML.</span><span class="sxs-lookup"><span data-stu-id="3c24d-111">Device-removal of the underlying Direct3D 12 device also causes the DirectML device to be removed.</span></span> <span data-ttu-id="3c24d-112">Sin embargo, esto no es aplicable a la inversa.</span><span class="sxs-lookup"><span data-stu-id="3c24d-112">However, the reverse is not true.</span></span> <span data-ttu-id="3c24d-113">La eliminación del dispositivo de DirectML puede no hacer que se quite el dispositivo de Direct3D 12 subyacente.</span><span class="sxs-lookup"><span data-stu-id="3c24d-113">DirectML device-removal may not necessarily cause the underlying Direct3D 12 device to become removed.</span></span>

## <a name="debugging-directml-device-removal-and-other-errors"></a><span data-ttu-id="3c24d-114">Depuración de dispositivos DirectML: eliminación y otros errores</span><span class="sxs-lookup"><span data-stu-id="3c24d-114">Debugging DirectML device-removal, and other errors</span></span>

<span data-ttu-id="3c24d-115">La causa más común de los errores de DirectML es el uso no válido de la API.</span><span class="sxs-lookup"><span data-stu-id="3c24d-115">The most common cause of DirectML errors is invalid API usage.</span></span> <span data-ttu-id="3c24d-116">El uso de API no válido podría dar lugar a un código de error de **E_INVALIDARG** HRESULT o podría dar lugar a la eliminación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c24d-116">Invalid API usage might result in an **E_INVALIDARG** HRESULT error code, or it might result in device-removal.</span></span>

<span data-ttu-id="3c24d-117">Se recomienda encarecidamente que habilite la [capa de depuración DirectML](dml-debug-layer.md) durante el desarrollo para detectar y depurar estos errores.</span><span class="sxs-lookup"><span data-stu-id="3c24d-117">We strongly recommend that you enable the [DirectML debug layer](dml-debug-layer.md) during your development, in order to catch and debug such errors.</span></span> <span data-ttu-id="3c24d-118">La capa de depuración DirectML realiza una validación exhaustiva de los parámetros del método y el uso de la API, y emitirá mensajes de salida de depuración para ayudarle a depurar.</span><span class="sxs-lookup"><span data-stu-id="3c24d-118">The DirectML debug layer performs extensive validation of method parameters and API usage, and it will emit debug output messages to help you debug.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c24d-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3c24d-119">See also</span></span>

* [<span data-ttu-id="3c24d-120">Usar la capa de depuración DirectML</span><span class="sxs-lookup"><span data-stu-id="3c24d-120">Using the DirectML debug layer</span></span>](dml-debug-layer.md)
