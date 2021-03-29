---
title: Entrada MouseWheel para Windows 8.1
description: Entrada MouseWheel para Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903307"
---
# <a name="mousewheel-input-for-windows-81"></a>Entrada MouseWheel para Windows 8.1

## <a name="platform"></a>Plataforma

<dl> Clientes-Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

En Windows 8.1, los eventos MouseWheel ya no se entregan en función del foco del teclado como en versiones anteriores de Windows. En Windows 8.1, si se mantiene el mouse sobre una aplicación de la tienda, se entregará MouseWheel a esa aplicación; por motivos de compatibilidad, sin embargo, si el mouse se mantiene sobre una aplicación de escritorio, MouseWheel se seguirá entregando en función del foco del teclado.

## <a name="manifestations"></a>Manifestaciones

Cuando el mouse se mantiene sobre las aplicaciones de la tienda, MouseWheel desplazará cualquier contenido aplicable sin que el usuario tenga que hacer clic en la aplicación de la tienda. Esto también se aplica a la pantalla Inicio. Esto hace que el desplazamiento por MouseWheel sea una interacción más sencilla en Windows 8.1 que en Windows 8.

## <a name="mitigation"></a>Mitigación

En su mayor parte, este cambio no debe tener ningún impacto en las aplicaciones existentes. Si una aplicación de la tienda escucha eventos MouseWheel solo después de haber registrado un evento de clic del mouse, esa aplicación no podría responder a MouseWheel hasta que el usuario haga clic activamente en ella. Por lo tanto, la desventaja más probable es que una aplicación continúe funcionando igual que en Windows 8. En el caso de las aplicaciones de escritorio, tener el foco de teclado ya no proporciona a la aplicación un monopolio sobre la entrada MouseWheel, pero tampoco se rompe de ningún modo. Por tanto, no se requieren mitigaciones a corto plazo.

## <a name="solution"></a>Solución

Los desarrolladores de aplicaciones de la tienda deberían esperar recibir eventos MouseWheel sin un evento de clic del mouse precursor. Por ejemplo, no deberían escuchar los eventos MouseWheel solo después de registrar un clic del mouse. Del mismo modo, las aplicaciones de escritorio no deben intentar capturar eventos MouseWheel (por ejemplo, estableciendo un enlace de bajo nivel) cuando tienen el foco de teclado.

## <a name="tests"></a>Pruebas

Los desarrolladores de aplicaciones de la tienda deben probar Windows 8.1 para comprobar que todas las funciones de desplazamiento funcionan siempre que se mantiene el mouse sobre la aplicación. Los desarrolladores de aplicaciones de escritorio deben probar Windows 8.1 para comprobar que no capturan eventos MouseWheel (según las instrucciones anteriores).

 

 




