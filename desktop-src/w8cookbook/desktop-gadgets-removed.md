---
title: Dispositivos de escritorio eliminados
description: Dispositivos de escritorio eliminados
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- gadgets
- escritorios de escritorio
- Windows Sidebar
- Barra lateral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254c4794c93c6afeeec9374e7c1c73f7d538c82b343ffaea984369a72231deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707015"
---
# <a name="desktop-gadgets-removed"></a>Dispositivos de escritorio eliminados

## <a name="platforms"></a>Plataformas

 **Clientes:** Windows 8  
**Servidores:** Windows Server 2012  



## <a name="description"></a>Descripción

Desde el punto de vista de la funcionalidad, ya están en desuso y se han superado por los nuevos iconos dinámicos y aplicaciones. Los dispositivos también presentan un riesgo de seguridad para los usuarios. Como plataforma, existen vulnerabilidades que incluso podrían aprovecharse de los benignos. Por lo tanto, para conservar Windows 8 como nuestro sistema operativo más moderno y seguro, hemos elegido quitar completamente los Elementos Desfasados del sistema operativo. Windows se notificará a los 7 usuarios que tienen Equipos de escritorio y se desinstalarán los dispositivos Desinstalados.

## <a name="manifestation"></a>Manifestación

Desktop Desktop Desktop no estará disponible en Windows Desktop.

## <a name="mitigation"></a>Mitigación

Desktop Desktop Desktop API y la estructura de carpetas permanecerán en su lugar para Windows 8. Las aplicaciones que instalan y ejecutan Con esta API mediante programación seguirán ejecándose sin errores (aunque no lo harán ellos mismos).

## <a name="solution"></a>Solución

Los desarrolladores de aplicaciones de escritorio no deben empaquetar Equipos de escritorio en sus instaladores. Estos Dispositivos simplemente ocuparán espacio para el usuario y no podrán ejecutarse en el sistema.

## <a name="tests"></a>Pruebas

Los desarrolladores pueden probar la compatibilidad de este cambio deshabilitando el componente opcional para Desktop Desktop Windows 7. Para deshabilitar los Dispositivos en un equipo Windows 7, siga estos pasos:

1.  Vaya a Turn Windows Features on or off from the Panel de control (Activar o desactivar las características de Panel de control).
2.  Desactive la casilla situada junto a "Windows Platform".
3.  Haga clic en Aceptar y siga las instrucciones adicionales en pantalla.

## <a name="resources"></a>Recursos

[Las vulnerabilidades de los Equipos podrían permitir la ejecución remota de código](https://support.microsoft.com/kb/2719662)

 

 




