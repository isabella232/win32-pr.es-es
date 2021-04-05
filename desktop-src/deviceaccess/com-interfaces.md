---
title: 'Interfaces COM: acceso a dispositivos'
description: Interfaces del modelo de objetos componentes (COM) en la API de acceso del dispositivo.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 07abbfd15f8383bbbd9cd9d1f5fc4c9fb1f42b9e
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078565"
---
# <a name="com-interfaces---device-access"></a><span data-ttu-id="f344d-103">Interfaces COM: acceso a dispositivos</span><span class="sxs-lookup"><span data-stu-id="f344d-103">COM Interfaces - Device Access</span></span>

<span data-ttu-id="f344d-104">Interfaces del modelo de objetos componentes (COM) en la API de acceso del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f344d-104">Component Object Model (COM)interfaces in the Device Access API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f344d-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f344d-105">In this section</span></span>

| <span data-ttu-id="f344d-106">Tema</span><span class="sxs-lookup"><span data-stu-id="f344d-106">Topic</span></span> | <span data-ttu-id="f344d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f344d-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="f344d-108">**ICreateDeviceAccessAsync**</span><span class="sxs-lookup"><span data-stu-id="f344d-108">**ICreateDeviceAccessAsync**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | <span data-ttu-id="f344d-109">La interfaz [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) se devuelve de una llamada a CreateDeviceAccessInstance.</span><span class="sxs-lookup"><span data-stu-id="f344d-109">The [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) interface is returned from a call to CreateDeviceAccessInstance.</span></span> <span data-ttu-id="f344d-110">Permite que el llamador controle la operación de enlace a una instancia de un dispositivo con el fin de recuperar otra interfaz que pueda usarse para interactuar con ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f344d-110">It enables the caller to control the operation of binding to an instance of a device in order to retrieve another interface that can be used to interact with that device.</span></span><br/> |
| [<span data-ttu-id="f344d-111">**IDeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="f344d-111">**IDeviceIoControl**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | <span data-ttu-id="f344d-112">Envía un código de control a un controlador de dispositivo. Esta acción hace que el dispositivo realice la operación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f344d-112">Sends a control code to a device driver.This action causes the device to perform the corresponding operation.</span></span> <br/> |
| [<span data-ttu-id="f344d-113">**IDeviceRequestCompletionCallback**</span><span class="sxs-lookup"><span data-stu-id="f344d-113">**IDeviceRequestCompletionCallback**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | <span data-ttu-id="f344d-114">Proporciona un método para controlar la finalización de las llamadas al método [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync).</span><span class="sxs-lookup"><span data-stu-id="f344d-114">Provides a method to handle the completion of calls to the [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)method.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="f344d-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f344d-115">Related topics</span></span>

<span data-ttu-id="f344d-116">[Ejemplo de acceso a controladores personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [aplicaciones para dispositivos UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [centro de desarrollo de hardware](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="f344d-116">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
