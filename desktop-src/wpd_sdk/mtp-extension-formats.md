---
description: Formatos de extensión MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Formatos de extensión MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720581"
---
# <a name="mtp-extension-formats"></a><span data-ttu-id="699e8-103">Formatos de extensión MTP</span><span class="sxs-lookup"><span data-stu-id="699e8-103">MTP Extension Formats</span></span>

<span data-ttu-id="699e8-104">El formato de un archivo en un dispositivo se puede describir mediante un valor GUID.</span><span class="sxs-lookup"><span data-stu-id="699e8-104">The format of a file on a device can be described by a GUID value.</span></span> <span data-ttu-id="699e8-105">Este valor se especifica mediante la \_ propiedad formato de objeto WPD \_ .</span><span class="sxs-lookup"><span data-stu-id="699e8-105">This value is specified by the WPD\_OBJECT\_FORMAT property.</span></span>

## <a name="vendor-extended-formats"></a><span data-ttu-id="699e8-106">Formatos extendidos de proveedor</span><span class="sxs-lookup"><span data-stu-id="699e8-106">Vendor-Extended Formats</span></span>

<span data-ttu-id="699e8-107">Cuando un fabricante de dispositivos admite un formato extendido de proveedor, el controlador combina el código de formato del proveedor (UINT16) con los 16 bits superiores **del \_ formato de objeto WPD sin \_ \_ especificar** .</span><span class="sxs-lookup"><span data-stu-id="699e8-107">When a device manufacturer supports a vendor-extended format, their driver combines the vendor's format code (UINT16) with the highest 16 bits of the **WPD\_OBJECT\_FORMAT\_UNSPECIFIED** GUID.</span></span>

<span data-ttu-id="699e8-108">Por ejemplo, si el código extendido del proveedor es 0xB001, el GUID resultante sería como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="699e8-108">For example, if the vendor-extended code is 0xB001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a><span data-ttu-id="699e8-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="699e8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="699e8-110">Compatibilidad con extensiones MTP</span><span class="sxs-lookup"><span data-stu-id="699e8-110">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



