---
title: Administración e implementación
description: Los profesionales de ti o los desarrolladores que preparan la implementación de Windows 7 tendrán mayor confianza y experimentarán un ciclo de evaluación más corto debido a las mejoras en las características y herramientas de creación de imágenes.
ms.assetid: 217090c4-6385-4333-a380-f75f2c80e369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105b19ad01cb9208d05e77871be637fdadcb0532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995402"
---
# <a name="management-and-deployment"></a>Administración e implementación

Los profesionales de ti o los desarrolladores que preparan la implementación de Windows 7 tendrán mayor confianza y experimentarán un ciclo de evaluación más corto debido a las mejoras en las características y herramientas de creación de imágenes. Entre ellas se incluye la compatibilidad con la administración de aplicaciones, controladores y sistemas operativos en archivos de imagen sin conexión. Además, la creación y la administración de imágenes serán más fáciles y estarán disponibles para una gama más amplia de organizaciones de ti. La implementación de Windows 7 en equipos empresariales también será más fácil y rápido gracias a las nuevas herramientas de migración de ti y las tecnologías de implementación automatizadas.

## <a name="windows-powershell-20"></a>Windows PowerShell 2.0

PowerShell es un lenguaje de scripting administrado completo Microsoft .NET que tiene un shell de línea de comandos interactivo y un entorno de scripting integrado (ISE) gráfico. Admite la bifurcación, el bucle, las funciones, la depuración, el control de excepciones y la internacionalización. PowerShell 2,0 es parte de Windows 7 y ofrece muchas mejoras y un conjunto cada vez mayor de *cmdlets* para diagnósticos de Windows, Microsoft Active Directory, Microsoft Internet Information Services (IIS) y mucho más.

La característica de comunicación remota de PowerShell 2,0 ahora permite a los usuarios ejecutar comandos en uno o varios equipos remotos desde un único equipo que ejecute PowerShell. Los desarrolladores también pueden hospedar PowerShell en IIS para tener acceso a sus servidores y administrarlos.

PowerShell 2,0 admite la creación de particiones y la organización de scripts de PowerShell mediante el uso de módulos que se pueden distribuir e implementar como unidades reutilizables independientes. También incluye compatibilidad con transacciones en el motor de PowerShell y las API, lo que significa que los desarrolladores pueden iniciar, confirmar y revertir las transacciones mediante *cmdlets* de transacciones integrados. Además, el motor de PowerShell incluye compatibilidad de eventos para escuchar, reenviar y actuar en eventos de administración y del sistema. Las aplicaciones de PowerShell se pueden escribir para suscribirse a determinados eventos para el procesamiento sincrónico o asincrónico. (Consulte [Windows PowerShell](https://msdn.microsoft.com/library/bb905330.aspx)).

![captura de pantalla de Windows PowerShell ISE](images/windows7-devguide-solidfig1-powershell.jpg)

Figura 1. Windows PowerShell es un lenguaje de scripting administrado de .NET completo que tiene un shell de línea de comandos interactivo y un ISE gráfico

## <a name="windows-installer"></a>Windows Installer

Windows Installer se ha actualizado para aumentar la eficacia del desarrollador reduciendo la cantidad de código personalizado que se requiere para crear un paquete de instalación y crear instalaciones de software para cada usuario verdaderas.

Varias transacciones de paquetes permiten a los desarrolladores crear una única transacción desde varios paquetes mediante el uso de un "encadenador" para incluir de forma dinámica los paquetes en la transacción. Si uno o varios de los paquetes no se instalan como se esperaba, revierta la instalación.

El controlador de IU incrustada facilita la integración de interfaces de usuario personalizadas mediante la incrustación de un controlador de interfaz de usuario personalizado en el paquete de Windows Installer.

El encadenamiento de paquetes múltiples incrustado permite a los desarrolladores habilitar eventos de instalación en varios paquetes. Por ejemplo, pueden habilitar eventos de instalación a petición, reparar eventos y desinstalar eventos en varios paquetes.

Las nuevas características también permiten la creación de instalaciones por usuario verdaderas, incluida la compatibilidad con los archivos de programa por usuario y la funcionalidad "elevar ahora", y proporcionan compatibilidad con el inventario de software sin conexión y las comprobaciones de aplicabilidad de revisiones a través de administración y mantenimiento de imágenes de implementación. (Vea las novedades [de Windows Installer 5,0](../msi/what-s-new-in-windows-installer-5-0.md)).

 

 