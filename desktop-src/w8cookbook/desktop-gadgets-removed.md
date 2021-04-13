---
title: Gadgets de escritorio quitados
description: Gadgets de escritorio quitados
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- gadgets
- Gadgets de escritorio
- Windows Sidebar
- Barra lateral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104421502"
---
# <a name="desktop-gadgets-removed"></a>Gadgets de escritorio quitados

## <a name="platforms"></a>Plataformas

 **Clientes** : Windows 8  
**Servidores** : Windows Server 2012  



## <a name="description"></a>Descripción

Desde el punto de vista de la funcionalidad, los gadgets ya están en desuso y se configuran mediante nuevas aplicaciones y iconos dinámicos. Los gadgets también presentan un riesgo de seguridad para los usuarios. Como plataforma, existen vulnerabilidades en las que incluso se podrían aprovechar los gadgets benignos. Por lo tanto, para mantener Windows 8 como nuestro sistema operativo más moderno y seguro, hemos optado por quitar completamente los gadgets del sistema operativo. Se notificará a los usuarios de Windows 7 con gadgets en el escritorio y se desinstalarán los gadgets.

## <a name="manifestation"></a>Manifestación

Los gadgets de escritorio no estarán disponibles en el escritorio de Windows.

## <a name="mitigation"></a>Mitigación

La estructura de carpetas y la API de gadgets de escritorio permanecerán en su lugar para Windows 8. Las aplicaciones que instalan y ejecutan gadgets mediante programación con esta API seguirán ejecutándose sin errores (aunque los propios gadgets no lo están).

## <a name="solution"></a>Solución

Los desarrolladores de aplicaciones de escritorio no deben empaquetar gadgets en sus instaladores. Estos gadgets solo ocuparán espacio para el usuario y no podrán ejecutarse en el sistema.

## <a name="tests"></a>Pruebas

Los desarrolladores pueden probar la compatibilidad de este cambio deshabilitando el componente opcional para los gadgets de escritorio en Windows 7. Para deshabilitar los gadgets en un equipo con Windows 7, siga estos pasos:

1.  Navegue para activar o desactivar las características de Windows desde el panel de control.
2.  Desactive la casilla situada junto a "plataforma de gadgets de Windows".
3.  Haga clic en aceptar y siga las instrucciones en pantalla adicionales.

## <a name="resources"></a>Recursos

[Vulnerabilidades en los gadgets podrían permitir la ejecución remota de código](https://support.microsoft.com/kb/2719662)

 

 




