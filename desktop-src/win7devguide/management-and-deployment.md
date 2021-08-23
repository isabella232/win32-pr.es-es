---
title: Administración e implementación
description: Los profesionales o desarrolladores de TI que se preparen para implementar Windows 7 tendrán una mayor confianza y experimentarán un ciclo de evaluación más corto debido a las mejoras en las características y herramientas de creación de imágenes.
ms.assetid: 217090c4-6385-4333-a380-f75f2c80e369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4a68a2c20f3ff765fcb9855afe1bd0455904088e3558562ec5c1cd0402e5c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964613"
---
# <a name="management-and-deployment"></a>Administración e implementación

Los profesionales o desarrolladores de TI que se preparen para implementar Windows 7 tendrán una mayor confianza y experimentarán un ciclo de evaluación más corto debido a las mejoras en las características y herramientas de creación de imágenes. Entre ellas se incluye la compatibilidad con la administración de aplicaciones, controladores y sistemas operativos en archivos de imagen sin conexión. Además, la creación y administración de imágenes será más fácil y estará disponible para una gama más amplia de organizaciones de TI. La implementación Windows 7 en equipos empresariales también será más fácil y rápida gracias a las nuevas herramientas de migración de IT y a las tecnologías de implementación automatizada.

## <a name="windows-powershell-20"></a>Windows PowerShell 2.0

PowerShell es un lenguaje de scripting Microsoft .NET administrado que tiene un shell de línea de comandos interactivo y un entorno de scripting integrado (ISE) gráfico. Admite bifurcaciones, bucles, funciones, depuración, control de excepciones e internacionalización. PowerShell 2.0 forma parte de Windows 7 y ofrece muchas mejoras y un conjunto creciente de *cmdlets* para Windows Diagnostics, Microsoft Active Directory, Microsoft Internet Information Services (IIS) y mucho más.

La característica de comunicación remota de PowerShell 2.0 ahora permite a los usuarios ejecutar comandos en uno o varios equipos remotos desde un solo equipo que ejecuta PowerShell. Los desarrolladores también pueden hospedar PowerShell en IIS para acceder a sus servidores y administrarlos.

PowerShell 2.0 admite la creación de particiones y la organización de scripts de PowerShell mediante módulos que se pueden distribuir e implementar como unidades reutilizables independientes. También incluye compatibilidad con transacciones en el motor y las API de PowerShell, lo que significa que los desarrolladores pueden iniciar, confirmar y revertir transacciones mediante cmdlets de transacción *integrados.* Además, el motor de PowerShell incluye compatibilidad con eventos para escuchar, reenviar y actuar en eventos de administración y del sistema. Las aplicaciones de PowerShell se pueden escribir para suscribirse a determinados eventos para el procesamiento sincrónico o asincrónico. (Vea [Windows PowerShell](https://msdn.microsoft.com/library/bb905330.aspx)).

![Captura de pantalla de Windows PowerShell ise](images/windows7-devguide-solidfig1-powershell.jpg)

Figura 1. Windows PowerShell es un lenguaje de scripting administrado de .NET completo que tiene un shell de línea de comandos interactivo y un ISE gráfico.

## <a name="windows-installer"></a>Windows Installer

Windows El instalador se ha actualizado para aumentar la eficacia del desarrollador al reducir la cantidad de código personalizado necesario para crear un paquete de instalación y crear verdaderas instalaciones de software por usuario.

Transacción de varios paquetes permite a los desarrolladores crear una única transacción a partir de varios paquetes mediante un "encadenador" para incluir dinámicamente paquetes en la transacción. Si uno o varios de los paquetes no se instalan según lo previsto, simplemente revierte la instalación.

El controlador de interfaz de usuario insertado facilita la integración de interfaces de usuario personalizadas mediante la inserción de un controlador de interfaz de usuario personalizado en Windows installer.

Embedded Multiple Package Chainer permite a los desarrolladores habilitar eventos de instalación en varios paquetes. Por ejemplo, pueden habilitar eventos de instalación a petición, reparar eventos y desinstalar eventos en varios paquetes.

Las nuevas características también permiten la creación de verdaderas instalaciones por usuario, incluida la compatibilidad con archivos de programa por usuario y la funcionalidad "Elevar ahora", y proporcionan compatibilidad con el inventario de software sin conexión y las comprobaciones de aplicabilidad de revisiones a través de Administración y mantenimiento de imágenes de implementación. (Vea [Novedades de Windows Installer 5.0).](../msi/what-s-new-in-windows-installer-5-0.md)

 

 