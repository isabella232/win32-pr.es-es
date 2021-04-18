---
description: La clase de dispositivo NDIS se compone de dispositivos que se pueden asociar a los controladores de Media Access Control (MAC) de la especificación de interfaz de controlador de red (NDIS) para admitir las comunicaciones de red. Puede tener acceso a estos dispositivos mediante funciones.
ms.assetid: 98cdd929-0bd7-4509-b2f5-4edd8d6a8080
title: NDIS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0be1a69f98f9a4ff8cdc2f8ea173b208c0011d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677475"
---
# <a name="ndis"></a><span data-ttu-id="188df-104">NDIS</span><span class="sxs-lookup"><span data-stu-id="188df-104">ndis</span></span>

<span data-ttu-id="188df-105">La clase de dispositivo NDIS se compone de dispositivos que se pueden asociar a los controladores de Media Access Control (MAC) de la especificación de interfaz de controlador de red (NDIS) para admitir las comunicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="188df-105">The ndis device class consists of devices that can be associated with network driver interface specification (NDIS) media access control (MAC) drivers to support network communications.</span></span> <span data-ttu-id="188df-106">Puede tener acceso a estos dispositivos mediante funciones.</span><span class="sxs-lookup"><span data-stu-id="188df-106">You access these devices by using functions.</span></span>

<span data-ttu-id="188df-107">Las funciones [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando estos miembros adicionales:</span><span class="sxs-lookup"><span data-stu-id="188df-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending these additional members:</span></span>

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

<span data-ttu-id="188df-108">El miembro **hDevice** es el identificador que se va a pasar a un equipo Mac, como el equipo Mac asincrónico para las redes de acceso telefónico, para asociar una conexión de red con la conexión de llamada o módem.</span><span class="sxs-lookup"><span data-stu-id="188df-108">The **hDevice** member is the identifier to pass to a MAC, such as the asynchronous MAC for dial-up networking, to associate a network connection with the call/modem connection.</span></span> <span data-ttu-id="188df-109">El miembro **szDeviceType** es una cadena terminada en null que especifica el nombre del dispositivo asociado al identificador.</span><span class="sxs-lookup"><span data-stu-id="188df-109">The **szDeviceType** member is a null-terminated string specifying the name of the device associated with the identifier.</span></span>

 

 



