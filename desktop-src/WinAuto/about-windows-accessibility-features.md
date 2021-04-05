---
title: Características de accesibilidad de Windows
description: 'La accesibilidad de Windows admite dos categorías de características para los desarrolladores de Windows: API de Win32 y configuración de usuario.'
ms.assetid: 823bbc5b-062b-43ef-9f3e-822dc6f55c5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabd92ed8594d711ae9b744dc7f4a2622e8cb3d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077979"
---
# <a name="windows-accessibility-features"></a>Características de accesibilidad de Windows

La accesibilidad de Windows admite dos categorías de características para ayudar a los desarrolladores de Windows a diseñar aplicaciones accesibles, los desarrolladores de tecnologías de asistencia, como lectores de pantalla y ampliadores, e ingenieros de pruebas de software crean scripts automatizados para probar aplicaciones de Windows.

## <a name="settings"></a>Configuración

Hay dos tipos de opciones de configuración disponibles para los usuarios (a través del centro de accesibilidad en el panel de control) que también se exponen a los desarrolladores:

- [Parámetros de accesibilidad](accessibility-parameters.md). Cuando se establecen, estos parámetros indican que las aplicaciones deberían cambiar su comportamiento predeterminado. Las aplicaciones pueden comprobar el estado de un parámetro de accesibilidad para determinar si el usuario desea un comportamiento especial que se puede proporcionar de una manera específica de la aplicación. Por ejemplo, el parámetro ShowSounds indica que una aplicación que normalmente utiliza sonido para transmitir información importante también debe proporcionar la información de forma visual.
- [Características de accesibilidad integradas](built-in-accessibility-features.md). Estas características están integradas en el sistema o se proporcionan como una extensión del sistema. Afectan al modo en que el usuario proporciona la entrada del teclado y del mouse al equipo. Cuando está habilitada, su funcionalidad está disponible independientemente de las aplicaciones que se estén ejecutando. Un ejemplo es un filtro de teclado que facilita a los usuarios con dificultades de movimiento que escriban combinaciones de teclas como CTRL + ALT + SUPR.

Cada parámetro de accesibilidad y cada característica de accesibilidad integrada corresponde a un parámetro del sistema que se puede establecer o consultar con la función [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .

## <a name="win32-apis"></a>API de Win32

Las API de Win32 proporcionan características de accesibilidad y automatización para ayudar a los desarrolladores a crear aplicaciones y marcos de interfaz de usuario, herramientas de compilación de proveedores de tecnología de asistencia, los evaluadores garantizan implementaciones de calidad y las personas con discapacidades usan sus equipos y dispositivos.

## <a name="related-topics"></a>Temas relacionados

[Consideraciones de seguridad para las tecnologías de asistencia](uiauto-securityoverview.md)