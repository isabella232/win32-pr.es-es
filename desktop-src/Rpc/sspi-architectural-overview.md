---
title: Información general sobre la arquitectura de SSPI
description: SSPI es una interfaz de software.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473506"
---
# <a name="sspi-architectural-overview"></a>Información general sobre la arquitectura de SSPI

SSPI es una interfaz de software. Las bibliotecas de programación distribuidas, como RPC, pueden usarla para las comunicaciones autenticadas. Uno o varios módulos de software proporcionan las funcionalidades de autenticación reales. Cada módulo, denominado proveedor de compatibilidad de seguridad (SSP), se implementa como una biblioteca de vínculos dinámicos (DLL). Un SSP proporciona uno o varios paquetes de seguridad.

Hay una variedad de SSP y paquetes disponibles. Windows incluye el paquete de seguridad NTLM y el paquete de seguridad del protocolo Kerberos de Microsoft. Además, puede optar por instalar el paquete de seguridad capa de sockets seguros (SSL) o cualquier otro SSP compatible con SSPI.

El uso de SSPI garantiza que, independientemente del SSP que seleccione, la aplicación acceda a las características de autenticación de forma uniforme. Esta funcionalidad proporciona a la aplicación una mayor independencia de la implementación de la red de la que estaba disponible en el pasado.

Las aplicaciones distribuidas se comunican a través de la interfaz RPC. A su vez, el software RPC accede a las características de autenticación de un SSP a través de SSPI.

Para obtener más información, vea [SSPI](/windows/desktop/SecAuthN/sspi).

 

 