---
title: Accesibilidad y soporte técnico global
description: La Windows 7 facilita la compilación de soluciones que son accesibles para más usuarios y que cumplen o superan los estándares de cumplimiento de accesibilidad.
ms.assetid: bcad2f00-7885-461c-a2dc-0a0a176962b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320f6e52dba4f2a6d9c89a7bdea287e948a1bca048b0d3e88a2a8978e8085d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709122"
---
# <a name="accessibility-and-global-support"></a>Accesibilidad y soporte técnico global

La Windows 7 facilita la compilación de soluciones que son accesibles para más usuarios y que cumplen o superan los estándares de cumplimiento de accesibilidad. La comunidad de proveedores de tecnología de asistencia (ATV) ahora puede crear soluciones para una variedad más amplia de aplicaciones cliente, y a los desarrolladores de aplicaciones les será más fácil compilar y validar interfaces de usuario accesibles.

Windows 7 también facilita la compatibilidad con varios idiomas globales que en versiones anteriores de Windows. Desde el momento en que un usuario selecciona un idioma y una ubicación, Windows 7 presenta fechas, números, calendarios, intercalaciones y otra información mediante las convenciones culturales que esperan los clientes.

## <a name="windows-automation"></a>Windows Automatización

Windows 7 ofrece una capa de automatización completa basada en estándares que se extiende para aplicaciones nativas. Se basa en Microsoft Active Accessibility y Microsoft Automatización de la interfaz de usuario. También está diseñado para funcionar con estándares del sector, como W3C Web ARIA (Aplicación de Internet enriquecida accesible) y *Especificaciones de la sección 508.*

Automatización de la interfaz de usuario ofrece un rendimiento mejorado mediante la introducción de servidores proxy de automatización no administrados más rápidos para controles Win32 de Microsoft y aplicaciones de Microsoft Active Accessibility heredadas *(MSAA),* y registros de eventos y proxy de Automatización de la interfaz de usuario y más rápidos. Las nuevas características de extensibilidad amplían los patrones de control, las propiedades y los eventos personalizados. (Consulte [Windows Automation API: Información general).](../winauto/windows-automation-api-overview.md)

## <a name="accessibility-support-tools"></a>Herramientas de soporte técnico de accesibilidad

El Comprobador de accesibilidad de la interfaz de usuario es una práctica herramienta de interfaz gráfica de usuario que permite a los desarrolladores y evaluadores comprobar rápidamente si su interfaz de usuario se ajusta a los requisitos clave de accesibilidad, como *MSAA* (que comprueba las relaciones primarias secundarias o rectángulos delimitadores) y Automatización de la interfaz de usuario acceso mediante programación, generación de eventos, diseño y navegación mediante teclado. (Vea [Comprobador de accesibilidad de la interfaz de](https://www.codeplex.com/AccCheck)usuario).

UIA Verify es un marco de automatización de pruebas que facilita las pruebas manuales y automatizadas de la implementación Automatización de la interfaz de usuario proveedor de un control o aplicación. Estas dos nuevas herramientas permiten a los desarrolladores probar las implementaciones de accesibilidad y la funcionalidad en aplicaciones que usan *MSAA* o Automatización de la interfaz de usuario. Ambas herramientas están disponibles a través [de CodePlex,](https://www.codeplex.com/)un sitio web creado por Microsoft para hospedar proyectos de código abierto y para atender mejor a la comunidad de desarrolladores. (Vea [Automatización de la interfaz de usuario de automatización de pruebas (UIA Verify) .)](https://uiautomationverify.codeplex.com/)

## <a name="improved-multi-language-user-interface-support-and-linguistic-services"></a>Se ha mejorado la compatibilidad con Interfaz de usuario idiomas y los servicios lingüísticos

Windows 7 proporciona a los desarrolladores un método estándar para preparar sus aplicaciones para el mercado internacional proporcionando una compatibilidad mejorada con la interfaz de usuario multilingüe y los servicios lingüísticos que pueden usar en sus aplicaciones.

Extended Linguistic Services es una nueva característica de Windows 7 que permite a los desarrolladores usar el mismo pequeño conjunto de API para aprovechar una variedad de funcionalidades lingüísticas avanzadas. Mediante el uso de Extended Linguistic ServicesAPI en Windows 7, los desarrolladores pueden detectar automáticamente el idioma de cualquier fragmento de texto Unicode y usar esa información para ayudar a elegir una experiencia de usuario más inteligente para clientes de todo el mundo. Extended Linguistic Services también ofrece compatibilidad integrada con la transliteración que convierte texto de un sistema de escritura a otro. Por ejemplo, los desarrolladores ahora pueden convertir automáticamente texto entre chino simplificado y tradicional para ayudar a las personas a comunicarse entre sí a través de límites lingüísticos. Mediante el uso de Extended Linguistic ServicesAPI, los desarrolladores podrán usar los servicios lingüísticos extendidos existentes y seleccionar nuevos servicios en el futuro sin necesidad de aprender código nuevo. (Vea [Servicios lingüísticos extendidos).](../intl/extended-linguistic-services.md)

 

 