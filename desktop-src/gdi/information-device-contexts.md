---
description: El controlador de dominio de información se usa para recuperar los datos de dispositivo predeterminados.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Información contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002e9d5ebb6831f9e2251e76049e586ac3e84056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544459"
---
# <a name="information-device-contexts"></a><span data-ttu-id="6aaf7-103">Información contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="6aaf7-103">Information Device Contexts</span></span>

<span data-ttu-id="6aaf7-104">El controlador de dominio de información se usa para recuperar los datos de dispositivo predeterminados.</span><span class="sxs-lookup"><span data-stu-id="6aaf7-104">The information DC is used to retrieve default device data.</span></span> <span data-ttu-id="6aaf7-105">Por ejemplo, una aplicación puede llamar a la función [**created**](/windows/desktop/api/Wingdi/nf-wingdi-createica) para crear un controlador de dominio de información para un modelo determinado de impresora y, a continuación, llamar a las funciones [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) y [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) para recuperar los atributos de pincel o pluma predeterminados.</span><span class="sxs-lookup"><span data-stu-id="6aaf7-105">For example, an application can call the [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica) function to create an information DC for a particular model of printer and then call the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions to retrieve the default pen or brush attributes.</span></span> <span data-ttu-id="6aaf7-106">Dado que el sistema puede recuperar información del dispositivo sin crear las estructuras que normalmente están asociadas a los otros tipos de contextos de dispositivo, un DC de información implica mucho menos sobrecarga y se crea significativamente más rápido que cualquiera de los demás tipos.</span><span class="sxs-lookup"><span data-stu-id="6aaf7-106">Because the system can retrieve device information without creating the structures normally associated with the other types of device contexts, an information DC involves far less overhead and is created significantly faster than any of the other types.</span></span> <span data-ttu-id="6aaf7-107">Una vez que una aplicación finaliza la recuperación de datos mediante un controlador de dominio de información, debe llamar a la función [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .</span><span class="sxs-lookup"><span data-stu-id="6aaf7-107">After an application finishes retrieving data by using an information DC, it must call the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span>

 

 



