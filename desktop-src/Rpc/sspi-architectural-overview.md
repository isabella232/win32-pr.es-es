---
title: Información general sobre la arquitectura SSPI
description: SSPI es una interfaz de software.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078098"
---
# <a name="sspi-architectural-overview"></a>Información general sobre la arquitectura SSPI

SSPI es una interfaz de software. Las bibliotecas de programación distribuidas, como RPC, pueden usarlas para las comunicaciones autenticadas. Uno o varios módulos de software proporcionan las capacidades de autenticación reales. Cada módulo, denominado proveedor de compatibilidad para seguridad (SSP), se implementa como una biblioteca de vínculos dinámicos (DLL). Un SSP proporciona uno o varios paquetes de seguridad.

Hay disponible una variedad de SSP y paquetes. Windows incluye el paquete de seguridad de NTLM y el paquete de seguridad del protocolo Kerberos de Microsoft. Además, puede optar por instalar el paquete de seguridad de capa de sockets seguros (SSL) o cualquier otro SSP compatible con SSPI.

El uso de SSPI garantiza que, independientemente del SSP que seleccione, la aplicación tenga acceso a las características de autenticación de forma uniforme. Esta capacidad proporciona a la aplicación una mayor independencia de la implementación de la red que estaba disponible en el pasado.

Las aplicaciones distribuidas se comunican a través de la interfaz RPC. El software RPC, a su vez, obtiene acceso a las características de autenticación de un SSP a través de la SSPI.

Para obtener más información, vea [SSPI](/windows/desktop/SecAuthN/sspi).

 

 