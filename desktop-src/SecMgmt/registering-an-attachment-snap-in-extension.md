---
description: Después de crear una extensión de complemento de datos adjuntos, debe registrarla para que MMC y los complementos de configuración de seguridad la encuentren y lo usen.
ms.assetid: 176a658c-b1fd-40c5-a2ac-c9a2b7060c55
title: Registrar una extensión de complemento de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7726131325433aa920ff22c9b71a4f7184000a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686676"
---
# <a name="registering-an-attachment-snap-in-extension"></a><span data-ttu-id="566ce-103">Registrar una extensión de complemento de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="566ce-103">Registering an Attachment Snap-in Extension</span></span>

<span data-ttu-id="566ce-104">Después de crear una extensión de complemento de datos adjuntos, debe registrarla para que MMC y los complementos de configuración de seguridad la encuentren y lo usen.</span><span class="sxs-lookup"><span data-stu-id="566ce-104">After you create an attachment snap-in extension, you must register it in order for the MMC and the Security Configuration snap-ins to locate and use it.</span></span>

<span data-ttu-id="566ce-105">El complemento de datos adjuntos debe extender el espacio de nombres de los complementos de configuración de seguridad mediante la adición de su propio nodo, tal como se describe en el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="566ce-105">Your attachment snap-in must extend the Security Configuration snap-ins namespace by adding its own node as described in the following procedure.</span></span>

<span data-ttu-id="566ce-106">**Para instalar y registrar la extensión del complemento de datos adjuntos**</span><span class="sxs-lookup"><span data-stu-id="566ce-106">**To install and register the attachment snap-in extension**</span></span>

1.  <span data-ttu-id="566ce-107">Registre la extensión del complemento en la siguiente clave del registro.</span><span class="sxs-lookup"><span data-stu-id="566ce-107">Register the snap-in extension under the following registry key.</span></span> <span data-ttu-id="566ce-108">No cree una clave independiente en el complemento; las extensiones de complementos de datos adjuntos solo deben ser extensiones.</span><span class="sxs-lookup"><span data-stu-id="566ce-108">Do not create a StandAlone key under the snap-in; attachment snap-ins extensions must only be extensions.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             MMC
                SnapIns
    ```

2.  <span data-ttu-id="566ce-109">Registre la extensión del complemento de datos adjuntos en las siguientes subclaves.</span><span class="sxs-lookup"><span data-stu-id="566ce-109">Register the attachment snap-in extension under the following subkeys.</span></span> <span data-ttu-id="566ce-110">Esto puede realizarse como parte de las implementaciones de la función **DllRegisterServer** y **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="566ce-110">This can be done as part of your **DllRegisterServer** and **DllUnregisterServer** function implementations.</span></span>

    <span data-ttu-id="566ce-111">Espacio de nombres de [plantillas de seguridad](security-templates.md) :</span><span class="sxs-lookup"><span data-stu-id="566ce-111">[Security Templates](security-templates.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   24a7f717-1f0c-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

    <span data-ttu-id="566ce-112">Espacio [de nombres de configuración y análisis de seguridad](security-configuration-and-analysis.md) :</span><span class="sxs-lookup"><span data-stu-id="566ce-112">[Security Configuration and Analysis](security-configuration-and-analysis.md) namespace:</span></span>

    ```
    HKLM
       SOFTWARE
          Microsoft
             MMC
                NodeTypes
                   678050c7-1ff8-11d1-affb-00c04fb984f9
                      Extensions
                         NameSpace
    ```

 

 



