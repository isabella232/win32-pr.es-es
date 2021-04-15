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
# <a name="guidelines-for-writing-eap-dlls"></a>Instrucciones para escribir archivos dll EAP

Se pueden escribir archivos dll o complementos EAP para optimizar su rendimiento en diferentes escenarios.

## <a name="general-guidelines"></a>Instrucciones generales

-   Con el fin de crear una conexión cifrada, los complementos EAP deben generar claves de cifrado y devolverlas a través de los atributos RADIUS específicos del proveedor de Microsoft MS-MPPE-send-keys y MS-MPPE-recv-keys. Para obtener más información, consulte la sección Comentarios en [**\_ \_ salida de EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) .

## <a name="wireless-guidelines"></a>Directrices inalámbricas

A continuación se incluyen instrucciones y recomendaciones para escribir un complemento EAP que admita la autenticación de máquinas en escenarios inalámbricos (802.1 X). Esta sección no se aplica a los escenarios de VPN y de acceso telefónico.

-   Para no bloquear la ejecución de sistemas desatendidos, los complementos EAP no deben realizar ninguna llamada a la interfaz de usuario.
-   La implementación del complemento EAP del paso de autenticación de la máquina debe completarse lo más rápido posible para que no dificulte el inicio del sistema operativo.
    > [!Note]  
    > Si el protocolo EAP no admite la autenticación de equipo, debe comprobar la marca de autenticación de la máquina, autenticación de **equipo de \_ \_ marca EAP \_ \_ ras** usada en el campo **fFlags** en [**\_ \_ entrada EAP de PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)y devolver un error.

     

 

 




