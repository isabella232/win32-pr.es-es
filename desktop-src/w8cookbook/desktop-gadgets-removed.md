---
title: Escritorios eliminados
description: Escritorios eliminados
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- gadgets
- escritorios de escritorio
- Windows Sidebar
- Barra lateral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360988"
---
# <a name="desktop-gadgets-removed"></a>Escritorios eliminados

## <a name="platforms"></a>Plataformas

 **Clientes:** Windows 8  
**Servidores:** Windows Server 2012  



## <a name="description"></a>Descripción

Desde el punto de vista de la funcionalidad, ya están en desuso y se han superado en las nuevas aplicaciones y iconos dinámicos. Los usuarios también presentan un riesgo de seguridad. Como plataforma, existen vulnerabilidades de tal forma que incluso se podrían aprovechar las vulnerabilidades benignas. Por lo tanto, para conservar Windows 8 como nuestro sistema operativo más moderno y seguro, hemos elegido quitar completamente el sistema operativo. Windows se notificará a los usuarios de 7 usuarios con Equipos de escritorio y Se desinstalarán.

## <a name="manifestation"></a>Manifestación

Desktop Desktop Desktop no estará disponible en Windows Desktop.

## <a name="mitigation"></a>Mitigación

La API Desktop y la estructura de carpetas permanecerán en su lugar para Windows 8. Las aplicaciones que instalan y ejecutan Conmutación mediante programación con esta API seguirán ejecándose sin errores (aunque los propios Usuarios no lo harán).

## <a name="solution"></a>Solución

Los desarrolladores de aplicaciones de escritorio no deben empaquetar los paquetes en sus instaladores. Estos Dispositivos simplemente ocuparán espacio para el usuario y no podrán ejecutarse en el sistema.

## <a name="tests"></a>Pruebas

Los desarrolladores pueden probar la compatibilidad de este cambio deshabilitando el componente opcional para Desktop Windows 7. Para deshabilitar Lanes en un equipo Windows 7, siga estos pasos:

1.  Vaya a Turn Windows Features on or off from the Panel de control (Activar o desactivar las características de Panel de control).
2.  Desactive la casilla situada junto a "Windows Platform".
3.  Haga clic en Aceptar y siga las instrucciones adicionales en pantalla.

## <a name="resources"></a>Recursos

[Las vulnerabilidades de los artefactos podrían permitir la ejecución remota de código](https://support.microsoft.com/kb/2719662)

 

 




