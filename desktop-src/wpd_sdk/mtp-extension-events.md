---
description: Eventos de extensión MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: Eventos de extensión MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720748"
---
# <a name="mtp-extension-events"></a><span data-ttu-id="e3277-103">Eventos de extensión MTP</span><span class="sxs-lookup"><span data-stu-id="e3277-103">MTP Extension Events</span></span>

<span data-ttu-id="e3277-104">Los eventos notifican a una aplicación que se han producido cambios en un dispositivo o con él.</span><span class="sxs-lookup"><span data-stu-id="e3277-104">Events notify an application that changes have occurred on, or with, a device.</span></span> <span data-ttu-id="e3277-105">Por ejemplo, una aplicación puede registrarse para recibir notfications de que se ha quitado un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3277-105">For example, an application can register to receive notfications that a device has been removed .</span></span>

## <a name="vendor-extended-event-codes"></a><span data-ttu-id="e3277-106">Códigos de eventos extendidos de proveedor</span><span class="sxs-lookup"><span data-stu-id="e3277-106">Vendor-Extended Event Codes</span></span>

<span data-ttu-id="e3277-107">Cuando un fabricante de dispositivos admite un evento extendido de proveedor, el controlador combina el código de evento del proveedor (UINT16) con los 16 bits más altos del GUID de **\_ \_ \_ \_ \_ eventos extendidos del evento de WPD** .</span><span class="sxs-lookup"><span data-stu-id="e3277-107">When a device manufacturer supports a vendor-extended event, their driver combines the vendor's event code (UINT16) with the highest 16 bits of the **WPD\_EVENT\_MTP\_VENDOR\_EXTENDED\_EVENTS** GUID.</span></span>

<span data-ttu-id="e3277-108">Por ejemplo, si el código extendido del proveedor es 0xC001, el GUID resultante sería como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e3277-108">For example, if the vendor-extended code is 0xC001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a><span data-ttu-id="e3277-109">Parámetros de eventos extendidos de proveedor</span><span class="sxs-lookup"><span data-stu-id="e3277-109">Vendor-Extended Event Parameters</span></span>

<span data-ttu-id="e3277-110">Los parámetros de un evento extendido de proveedor se indican mediante el **\_ identificador de \_ \_ evento del \_ parámetro de evento WPD** GUID y la propiedad de WPD parámetros de **\_ \_ \_ \_ evento ext ext \_**, que es una colección de **PROPVARIANTS**.</span><span class="sxs-lookup"><span data-stu-id="e3277-110">The parameters for a vendor-extended event are reported by the **WPD\_EVENT\_PARAMETER\_EVENT\_ID** GUID and the **WPD\_PROPERTY\_MTP\_EXT\_EVENT\_PARAMS**, which is a collection of **PROPVARIANTS**.</span></span> <span data-ttu-id="e3277-111">Estos **PROPVARIANTS** se corresponden con los parámetros de evento.</span><span class="sxs-lookup"><span data-stu-id="e3277-111">These **PROPVARIANTS** correspond to the event parameters.</span></span> <span data-ttu-id="e3277-112">Si no hay ningún parámetro, esta colección está vacía.</span><span class="sxs-lookup"><span data-stu-id="e3277-112">If there are no parameters, this collection is empty.</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a><span data-ttu-id="e3277-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3277-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3277-114">Compatibilidad con extensiones MTP</span><span class="sxs-lookup"><span data-stu-id="e3277-114">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



