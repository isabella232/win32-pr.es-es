---
title: Instrucciones para escribir archivos dll EAP
description: Se pueden escribir archivos dll o complementos EAP para optimizar su rendimiento en diferentes escenarios.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc2d437df61811e6fb24b3a9b4ff406ced4905
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105714311"
---
# <a name="guidelines-for-writing-eap-dlls"></a><span data-ttu-id="7d335-103">Instrucciones para escribir archivos dll EAP</span><span class="sxs-lookup"><span data-stu-id="7d335-103">Guidelines for Writing EAP DLLs</span></span>

<span data-ttu-id="7d335-104">Se pueden escribir archivos dll o complementos EAP para optimizar su rendimiento en diferentes escenarios.</span><span class="sxs-lookup"><span data-stu-id="7d335-104">EAP DLLs or Plug-ins can be written to optimize their performance in different scenarios.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="7d335-105">Instrucciones generales</span><span class="sxs-lookup"><span data-stu-id="7d335-105">General Guidelines</span></span>

-   <span data-ttu-id="7d335-106">Con el fin de crear una conexión cifrada, los complementos EAP deben generar claves de cifrado y devolverlas a través de los atributos RADIUS específicos del proveedor de Microsoft MS-MPPE-send-keys y MS-MPPE-recv-keys.</span><span class="sxs-lookup"><span data-stu-id="7d335-106">In order to create an encrypted connection, EAP plug-ins must generate encryption keys and return them through the Microsoft vendor-specific RADIUS Attributes MS-MPPE-Send-Keys and MS-MPPE-Recv-Keys.</span></span> <span data-ttu-id="7d335-107">Para obtener más información, consulte la sección Comentarios en [**\_ \_ salida de EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) .</span><span class="sxs-lookup"><span data-stu-id="7d335-107">See the Remarks section in [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) for more information.</span></span>

## <a name="wireless-guidelines"></a><span data-ttu-id="7d335-108">Directrices inalámbricas</span><span class="sxs-lookup"><span data-stu-id="7d335-108">Wireless Guidelines</span></span>

<span data-ttu-id="7d335-109">A continuación se incluyen instrucciones y recomendaciones para escribir un complemento EAP que admita la autenticación de máquinas en escenarios inalámbricos (802.1 X).</span><span class="sxs-lookup"><span data-stu-id="7d335-109">The following are guidelines and recommendations for writing an EAP Plug-in that supports authenticating machines in wireless (802.1X) scenarios.</span></span> <span data-ttu-id="7d335-110">Esta sección no se aplica a los escenarios de VPN y de acceso telefónico.</span><span class="sxs-lookup"><span data-stu-id="7d335-110">This section does not apply to VPN and Dial-up scenarios.</span></span>

-   <span data-ttu-id="7d335-111">Para no bloquear la ejecución de sistemas desatendidos, los complementos EAP no deben realizar ninguna llamada a la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7d335-111">In order not to block unattended systems' execution, EAP plug-ins must not make any user interface calls.</span></span>
-   <span data-ttu-id="7d335-112">La implementación del complemento EAP del paso de autenticación de la máquina debe completarse lo más rápido posible para que no dificulte el inicio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7d335-112">The EAP Plug-in implementation of the machine authentication step must complete as quickly as possible so it does not hinder operating system startup.</span></span>
    > [!Note]  
    > <span data-ttu-id="7d335-113">Si el protocolo EAP no admite la autenticación de equipo, debe comprobar la marca de autenticación de la máquina, autenticación de **equipo de \_ \_ marca EAP \_ \_ ras** usada en el campo **fFlags** en [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)y devolver un error.</span><span class="sxs-lookup"><span data-stu-id="7d335-113">If your EAP protocol does not support machine authentication, it must check for the machine authentication flag, **RAS\_EAP\_FLAG\_MACHINE\_AUTH** used in the **fFlags** field in [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), and return an error.</span></span>

     

 

 




