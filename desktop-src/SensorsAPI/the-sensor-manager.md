---
description: El objeto de administrador de sensor proporciona acceso a los sensores que están disponibles para su uso.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: El objeto de administrador de sensores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154057"
---
# <a name="the-sensor-manager-object"></a><span data-ttu-id="1330b-103">El objeto de administrador de sensores</span><span class="sxs-lookup"><span data-stu-id="1330b-103">The Sensor Manager Object</span></span>

<span data-ttu-id="1330b-104">El objeto de administrador de sensor proporciona acceso a los sensores que están disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="1330b-104">The sensor manager object provides access to the sensors that are available for your use.</span></span>

<span data-ttu-id="1330b-105">Para usar la API de sensor, primero debe llamar al método **CoCreateInstance** de com para crear una instancia del objeto de administrador de sensor y recuperar un puntero a su interfaz, denominada [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span><span class="sxs-lookup"><span data-stu-id="1330b-105">To use the Sensor API, you must first call the COM **CoCreateInstance** method to create an instance of the sensor manager object and retrieve a pointer to its interface, named [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span></span> <span data-ttu-id="1330b-106">El administrador del sensor mantiene la lista de sensores disponibles.</span><span class="sxs-lookup"><span data-stu-id="1330b-106">The sensor manager maintains the list of available sensors.</span></span> <span data-ttu-id="1330b-107">Puede usar **ISensorManager** para llamar a métodos que recuperen grupos de sensores por categoría o por tipo, o puede llamar a un método para recuperar un sensor determinado mediante su identificador único.</span><span class="sxs-lookup"><span data-stu-id="1330b-107">You can use **ISensorManager** to call methods that retrieve groups of sensors by category or by type, or you can call a method to retrieve a particular sensor by using its unique ID.</span></span> <span data-ttu-id="1330b-108">El administrador del sensor también le permite registrarse para recibir un evento que le informa cuando se ha conectado un nuevo sensor a la plataforma.</span><span class="sxs-lookup"><span data-stu-id="1330b-108">The sensor manager also enables you to register to receive an event that notifies you when a new sensor has been connected to the platform.</span></span>

<span data-ttu-id="1330b-109">A veces, el administrador del sensor proporciona un puntero a un sensor, pero el usuario no ha habilitado el sensor.</span><span class="sxs-lookup"><span data-stu-id="1330b-109">Sometimes, the sensor manager provides a pointer to a sensor, but the user has not enabled the sensor.</span></span> <span data-ttu-id="1330b-110">Por ejemplo, a menudo puede recuperar los valores de las propiedades del sensor no privado, como el fabricante o el modelo del sensor, antes de que el usuario habilite el sensor.</span><span class="sxs-lookup"><span data-stu-id="1330b-110">For example, you can often retrieve values for non-private sensor properties, such as the sensor manufacturer or model, before the user enables the sensor.</span></span> <span data-ttu-id="1330b-111">Esta información puede ayudarle a decidir si desea solicitar al usuario permiso para usar el sensor.</span><span class="sxs-lookup"><span data-stu-id="1330b-111">This information can help you to decide whether to ask the user for permission to use the sensor.</span></span> <span data-ttu-id="1330b-112">Puede llamar a [**ISensorManager:: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) para solicitar al usuario que habilite un sensor determinado o una colección de sensores.</span><span class="sxs-lookup"><span data-stu-id="1330b-112">You can call [**ISensorManager::RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) to prompt the user to enable a particular sensor or collection of sensors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1330b-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1330b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1330b-114">Administrar permisos de usuario</span><span class="sxs-lookup"><span data-stu-id="1330b-114">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> <dt>

[<span data-ttu-id="1330b-115">Solicitar permisos de usuario</span><span class="sxs-lookup"><span data-stu-id="1330b-115">Requesting User Permissions</span></span>](requesting-user-permissions.md)
</dt> </dl>

 

 
