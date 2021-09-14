---
description: Explica cómo crear un paquete de seguridad personalizado.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Crear paquetes de seguridad personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2136775d18e9d33f59d1b1f44fd817b3f3271ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160999"
---
# <a name="creating-custom-security-packages"></a>Crear paquetes de seguridad personalizados

## <a name="ssp-security-packages"></a>Paquetes de seguridad SSP

Si un paquete de seguridad del proveedor de soporte técnico de seguridad (SSP) personalizado se usará exclusivamente para la compatibilidad de seguridad de cliente/servidor, puede implementar la interfaz del proveedor de soporte técnico de seguridad [de](sspi.md)Microsoft .

El ejemplo de KitsSSP incluido con Platform Software Development Kit (SDK) contiene una implementación de paquete de seguridad SSP de ejemplo.

## <a name="sspap-security-packages"></a>Paquetes de seguridad SSP/AP

Los [*paquetes de*](/windows/desktop/SecGloss/s-gly)autenticación del proveedor de compatibilidad de seguridad personalizada / [](/windows/desktop/SecGloss/a-gly) (SSP/AP) contienen paquetes de seguridad que funcionan como paquetes de autenticación (AP) y proveedores de soporte técnico de seguridad (SSP). Estos paquetes implementan API independientes para admitir cada rol.

Dado que funciona como UN AP, un [](/windows/desktop/SecGloss/s-gly) paquete de seguridad SSP/AP personalizado debe proporcionar implementaciones para todas las funciones implementadas por paquetes [de autenticación](authentication-functions.md).

Para proporcionar compatibilidad de seguridad integrada, un paquete de seguridad SSP/AP personalizado debe proporcionar implementaciones para las funciones implementadas por [SSP/AP](authentication-functions.md). Funciones LSA llamadas por [SSP/AP](authentication-functions.md) describe las funciones de soporte técnico disponibles para los desarrolladores de SSP/AP que desean interactuar con el LSA.

Los paquetes de seguridad SSP/AP, con el fin de realizarse como UN AP y un SSP, pueden ejecutarse como parte del sistema operativo y como parte de una aplicación de usuario. Estos dos modos de ejecución se conocen como modo LSA y modo de usuario, respectivamente. Para obtener más información sobre los paquetes de seguridad personalizados en el modo LSA, vea [Inicialización del modo LSA.](lsa-mode-initialization.md) Para obtener más información sobre el modo de usuario, vea [Inicialización del modo de usuario](user-mode-initialization.md).

Si un paquete de seguridad SSP/AP personalizado ofrece servicios para aplicaciones cliente/servidor, debe proporcionar implementaciones para las funciones descritas en Funciones implementadas por [SSP/AP](authentication-functions.md)en modo de usuario. Las funciones LSA llamadas por [SSP/AP](authentication-functions.md) en modo de usuario describen las funciones de compatibilidad disponibles para un SSP/AP que se ejecuta en un proceso de cliente o servidor.

Para obtener información sobre cómo registrar un archivo DLL de SSP/AP, vea Registrar archivos DLL [de SSP/AP.](registering-ssp-ap-dlls.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones en torno al registro e instalación de un paquete de seguridad](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
