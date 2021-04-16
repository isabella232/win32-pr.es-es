---
description: Después de determinar las capacidades de un dispositivo de teléfono, una aplicación debe abrir el dispositivo antes de poder acceder a las funciones de ese teléfono.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Apertura y cierre de dispositivos telefónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677473"
---
# <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="cdcba-103">Apertura y cierre de dispositivos telefónicos</span><span class="sxs-lookup"><span data-stu-id="cdcba-103">Opening and Closing Phone Devices</span></span>

<span data-ttu-id="cdcba-104">Después de determinar las capacidades de un dispositivo de teléfono, una aplicación debe abrir el dispositivo antes de poder acceder a las funciones de ese teléfono.</span><span class="sxs-lookup"><span data-stu-id="cdcba-104">After determining the capabilities of a phone device, an application must open the device before it can access functions on that phone.</span></span> <span data-ttu-id="cdcba-105">Una vez que un dispositivo telefónico se ha abierto correctamente, se devuelve un identificador que representa el teléfono abierto a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdcba-105">After a phone device has been successfully opened, the application is returned a handle representing the open phone.</span></span> <span data-ttu-id="cdcba-106">Un dispositivo telefónico se puede abrir en modos diferentes, lo que proporciona una manera estructurada de compartir un dispositivo telefónico.</span><span class="sxs-lookup"><span data-stu-id="cdcba-106">A phone device can be opened in different modes, thus providing a structured way of sharing a phone device.</span></span>

<span data-ttu-id="cdcba-107">La función [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) abre el dispositivo de teléfono especificado para conceder a la aplicación acceso a las funciones del teléfono.</span><span class="sxs-lookup"><span data-stu-id="cdcba-107">The [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) function opens the specified phone device to give the application access to functions on the phone.</span></span> <span data-ttu-id="cdcba-108">Un dispositivo telefónico se identifica como **phoneOpen** por medio de su identificador de dispositivo, que se pasa como el parámetro *dwDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="cdcba-108">A phone device is identified to **phoneOpen** by means of its device identifier, which is passed as the *dwDeviceID* parameter.</span></span>

 

 



