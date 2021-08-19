---
title: Características de accesibilidad de Windows
description: 'Windows Accesibilidad admite dos categorías de características para Windows desarrolladores: API win32 y usuario Configuración.'
ms.assetid: 823bbc5b-062b-43ef-9f3e-822dc6f55c5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac63f4bf021888ee96cb180e423f55b07190959ad8c8b7966f1a4a7ae395119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994425"
---
# <a name="windows-accessibility-features"></a>Características de accesibilidad de Windows

Windows La accesibilidad admite dos categorías de características para ayudar Windows los desarrolladores a diseñar aplicaciones accesibles, los desarrolladores de tecnología de asistencia crean herramientas como lectores de pantalla y lupa, y los ingenieros de pruebas de software crean scripts automatizados para probar Windows aplicaciones.

## <a name="settings"></a>Configuración

Hay dos tipos de configuración disponibles para los usuarios (a través del Centro de accesibilidad en Panel de control) que también se exponen a los desarrolladores:

- [Parámetros de accesibilidad](accessibility-parameters.md). Cuando se establece, estos parámetros indican que las aplicaciones deben cambiar su comportamiento predeterminado. Las aplicaciones pueden comprobar el estado de un parámetro de accesibilidad para determinar si el usuario quiere un comportamiento especial que se pueda proporcionar de una manera específica de la aplicación. Por ejemplo, el parámetro ShowSounds indica que una aplicación que normalmente usa sonido para transmitir información importante también debe proporcionar la información visualmente.
- [Características de accesibilidad integradas.](built-in-accessibility-features.md) Estas características están integradas en el sistema o se proporcionan como una extensión del sistema. Afectan al modo en que el usuario proporciona entradas de teclado y mouse al equipo. Cuando se habilita, su funcionalidad está disponible independientemente de las aplicaciones que se ejecuten. Un ejemplo es un filtro de teclado que facilita a los usuarios con discapacidades de movimiento escribir combinaciones de teclas como CTRL+ALT+SUPR.

Cada parámetro de accesibilidad y cada característica de accesibilidad integrada corresponde a un parámetro del sistema que se puede establecer o consultar con la función [SystemParametersInfo.](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)

## <a name="win32-apis"></a>API de Win32

Las API de Win32 proporcionan características de accesibilidad y automatización para ayudar a los desarrolladores a crear aplicaciones y marcos de interfaz de usuario, proveedores de tecnología de asistencia que crean herramientas, evaluadores garantizan implementaciones de calidad y las personas con discapacidades usan sus equipos y dispositivos.

## <a name="related-topics"></a>Temas relacionados

[Consideraciones de seguridad para las tecnologías de asistencia](uiauto-securityoverview.md)