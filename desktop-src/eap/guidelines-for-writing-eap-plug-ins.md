---
title: Directrices para escribir archivos DLL de EAP
description: Los archivos DLL o complementos de EAP se pueden escribir para optimizar su rendimiento en distintos escenarios.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c786da1ca026039ffd052f1213b2904dbfa602ee67c6d74aed7a0fe11fd9d566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499160"
---
# <a name="guidelines-for-writing-eap-dlls"></a>Directrices para escribir archivos DLL de EAP

Los archivos DLL o complementos de EAP se pueden escribir para optimizar su rendimiento en distintos escenarios.

## <a name="general-guidelines"></a>Directrices generales

-   Para crear una conexión cifrada, los complementos EAP deben generar claves de cifrado y devolverlas a través de los atributos RADIUS específicos del proveedor de Microsoft MS-MPPE-Send-Keys y MS-MPPE-Recv-Keys. Para obtener más información, consulte la sección Comentarios [**de PPP \_ EAP \_ OUTPUT.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output)

## <a name="wireless-guidelines"></a>Directrices inalámbricas

A continuación se incluyen instrucciones y recomendaciones para escribir un complemento EAP que admita la autenticación de máquinas en escenarios inalámbricos (802.1X). Esta sección no se aplica a los escenarios de VPN y acceso telefónico.

-   Para no bloquear la ejecución de sistemas desatendidos, los complementos EAP no deben realizar ninguna llamada a la interfaz de usuario.
-   La implementación del complemento EAP del paso de autenticación de la máquina debe completarse lo antes posible para que no impida el inicio del sistema operativo.
    > [!Note]  
    > Si el protocolo EAP no admite la autenticación de máquina, debe comprobar la marca de autenticación de la máquina, RAS **\_ EAP FLAG MACHINE \_ \_ \_ AUTH** usada en el campo **fFlags** en [**PPP EAP \_ \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)y devolver un error.

     

 

 




