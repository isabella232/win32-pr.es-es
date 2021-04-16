---
description: Calidad de servicio (QoS) se implementa en Windows a través de varios componentes de QoS admitidos en Windows Server 2003, Windows XP y Windows 2000.
ms.assetid: e55b085f-6f72-4aa4-a8b0-b7609b9010dc
title: Calidad de servicio en Windows Sockets 2 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87d37f2e30e0a4fb296fc340353e2f4d85b5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706199"
---
# <a name="quality-of-service-in-the-windows-sockets-2-spi"></a><span data-ttu-id="b339c-103">Calidad de servicio en Windows Sockets 2 SPI</span><span class="sxs-lookup"><span data-stu-id="b339c-103">Quality of Service in the Windows Sockets 2 SPI</span></span>

<span data-ttu-id="b339c-104">Calidad de servicio (QoS) se implementa en Windows a través de varios componentes de QoS admitidos en Windows Server 2003, Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b339c-104">Quality of Service (QoS) is implemented in Windows through various QoS components supported on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="b339c-105">Una explicación detallada de QoS y sus componentes se encuentra en una sección dedicada a la calidad del servicio, que se encuentra en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b339c-105">A detailed explanation of QoS and its components is located in a section dedicated to Quality of Service, located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b339c-106">Cada componente de QoS, y el rol que desempeña en la implementación de QoS, se explica en esta sección de QoS, con instrucciones adicionales que se proporcionan para la implementación de aplicaciones y servicios habilitados para QoS.</span><span class="sxs-lookup"><span data-stu-id="b339c-106">Each QoS component, and the role it plays in the QoS implementation, is explained in this QoS section, with additional guidance provided for the implementation of QoS-enabled applications and services.</span></span> <span data-ttu-id="b339c-107">Consulte la sección [calidad de servicio (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) de la Windows SDK para obtener información más detallada.</span><span class="sxs-lookup"><span data-stu-id="b339c-107">Please see the [Quality of Service (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) section of the Windows SDK for more detailed information.</span></span>

<span data-ttu-id="b339c-108">En esta sección se describen las capacidades de calidad de servicio disponibles para los desarrolladores de Winsock.</span><span class="sxs-lookup"><span data-stu-id="b339c-108">This section describes Quality of Service capabilities available to Winsock developers.</span></span> <span data-ttu-id="b339c-109">En la lista siguiente se describen los temas de esta sección:</span><span class="sxs-lookup"><span data-stu-id="b339c-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="b339c-110">Modelo de uso</span><span class="sxs-lookup"><span data-stu-id="b339c-110">Usage Model</span></span>](usage-model-2.md)
-   [<span data-ttu-id="b339c-111">Actualizaciones de QoS</span><span class="sxs-lookup"><span data-stu-id="b339c-111">QoS Updates</span></span>](qos-updates-2.md)
-   [<span data-ttu-id="b339c-112">Valores predeterminados en el SPI</span><span class="sxs-lookup"><span data-stu-id="b339c-112">Default Values in the SPI</span></span>](default-values-in-the-spi-2.md)
-   [<span data-ttu-id="b339c-113">Plantillas de QoS en el SPI</span><span class="sxs-lookup"><span data-stu-id="b339c-113">QoS Templates in the SPI</span></span>](qos-templates-in-the-spi-2.md)

## <a name="related-topics"></a><span data-ttu-id="b339c-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b339c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b339c-115">Calidad de servicio (QoS)</span><span class="sxs-lookup"><span data-stu-id="b339c-115">Quality of Service (QoS)</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> <dt>

<span data-ttu-id="b339c-116">[¿Qué es QoS?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b339c-116">[What Is QoS?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="b339c-117">Extensión QoS de ATM de Winsock</span><span class="sxs-lookup"><span data-stu-id="b339c-117">Winsock ATM QoS Extension</span></span>](winsock-atm-qos-extension.md)
</dt> <dt>

[<span data-ttu-id="b339c-118">**Ioctl de Winsock**</span><span class="sxs-lookup"><span data-stu-id="b339c-118">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
