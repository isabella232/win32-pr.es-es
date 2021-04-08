---
description: Explica cómo crear un paquete de seguridad personalizado.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Crear paquetes de seguridad personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2136775d18e9d33f59d1b1f44fd817b3f3271ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910634"
---
# <a name="creating-custom-security-packages"></a>Crear paquetes de seguridad personalizados

## <a name="ssp-security-packages"></a>Paquetes de seguridad de SSP

Si un paquete de seguridad del proveedor de compatibilidad para seguridad (SSP) personalizado se utiliza exclusivamente para la compatibilidad con la seguridad de cliente/servidor, puede implementar la [interfaz del proveedor de compatibilidad para seguridad](sspi.md)de Microsoft.

El ejemplo de SampSSP que se incluye con el kit de desarrollo de software (SDK) de plataforma contiene un ejemplo de implementación de paquete de seguridad de SSP.

## <a name="sspap-security-packages"></a>Paquetes de seguridad SSP/AP

Los paquetes de autenticación del [*proveedor de soporte de seguridad*](/windows/desktop/SecGloss/s-gly)personalizados / [](/windows/desktop/SecGloss/a-gly) (SSP/APS) contienen paquetes de seguridad que funcionan como paquetes de autenticación (APS) y proveedores de compatibilidad para seguridad (SSP). Estos paquetes implementan API independientes para admitir cada rol.

Dado que funciona como un AP, un [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) SSP/AP personalizado debe proporcionar implementaciones para todas las [funciones implementadas por los paquetes de autenticación](authentication-functions.md).

Para proporcionar compatibilidad con la seguridad integrada, un paquete personalizado de seguridad SSP/AP debe proporcionar implementaciones para las [funciones implementadas por SSP/APS](authentication-functions.md). [Las funciones de LSA llamadas por SSP/APS](authentication-functions.md) describen las funciones de soporte técnico disponibles para los desarrolladores de SSP/AP que desean interactuar con la LSA.

Los paquetes de seguridad SSP/AP, para que se ejecuten como AP y SSP, pueden ejecutarse como parte del sistema operativo y como parte de una aplicación de usuario. Estos dos modos de ejecución se conocen como modo LSA y modo usuario, respectivamente. Para obtener más información sobre los paquetes de seguridad personalizados en el modo LSA, vea [inicialización del modo LSA](lsa-mode-initialization.md). Para obtener más información sobre el modo de usuario, consulte [inicialización del modo de usuario](user-mode-initialization.md).

Si un paquete de seguridad SSP/AP personalizado ofrece servicios para aplicaciones cliente/servidor, debe proporcionar implementaciones para las funciones descritas en [funciones implementadas por SSP/APS en modo de usuario](authentication-functions.md). [Las funciones de LSA llamadas por SSP/APS en modo de usuario](authentication-functions.md) describen las funciones de soporte técnico disponibles para un SSP/AP que se ejecutan en un proceso de cliente o servidor.

Para obtener información acerca del registro de un archivo DLL SSP/AP, consulte [registro de dll de SSP/AP](registering-ssp-ap-dlls.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones en relación con el registro y la instalación de un paquete de seguridad](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
