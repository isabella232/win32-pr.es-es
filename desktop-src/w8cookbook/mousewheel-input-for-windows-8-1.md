---
title: Entrada de la rueda del mouse para Windows 8.1
description: Entrada de la rueda del mouse para Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362823"
---
# <a name="mousewheel-input-for-windows-81"></a>Entrada de la rueda del mouse para Windows 8.1

## <a name="platform"></a>Plataforma

<dl> Clientes: Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

En Windows 8.1, los eventos de la rueda del mouse ya no se entregan en función del foco del teclado, como en versiones anteriores de Windows. En Windows 8.1, si el mouse mantiene el mouse sobre una aplicación de la tienda, la rueda del mouse se entregará a esa aplicación; Sin embargo, por motivos de compatibilidad, si el mouse mantiene el mouse sobre una aplicación de escritorio, la rueda del mouse se seguirá entregando en función del foco del teclado.

## <a name="manifestations"></a>Manifestaciones

Cuando el mouse mantiene el mouse sobre las aplicaciones de la Tienda, se desplaza cualquier contenido aplicable sin que el usuario tenga que hacer clic en la aplicación store. Esto también se aplica a la pantalla de inicio. Esto hace que el desplazamiento por la rueda del mouse sea una interacción más sencilla en Windows 8.1 que en Windows 8.

## <a name="mitigation"></a>Mitigación

En su mayor parte, este cambio no debería afectar a las aplicaciones existentes. Si una aplicación de la Tienda escuchaba eventos de rueda del mouse solo después de haber registrado un evento de clic del mouse, es probable que esa aplicación no respondiese a la rueda del mouse hasta que el usuario hubiera hecho clic en él activamente. Por lo tanto, lo más probable aquí es simplemente que una aplicación siga funcionando igual que en Windows 8. En el caso de las aplicaciones de escritorio, tener el foco de teclado ya no proporciona a la aplicación un favor sobre la entrada de la rueda del mouse, pero esto tampoco las interrumpirá de ninguna manera. Por lo tanto, no se requiere ninguna mitigación a corto plazo.

## <a name="solution"></a>Solución

Los desarrolladores de aplicaciones de la Tienda deben esperar recibir eventos de rueda del mouse sin un evento de clic del mouse. Por ejemplo, no deben escuchar eventos de rueda del mouse solo después de registrar un clic del mouse. De forma similar, las aplicaciones de escritorio no deben intentar capturar eventos de rueda del mouse (por ejemplo, estableciendo un enlace de bajo nivel) cuando tienen el foco de teclado.

## <a name="tests"></a>Pruebas

Los desarrolladores de aplicaciones de la tienda deben Windows 8.1 para comprobar que toda la funcionalidad de desplazamiento funciona siempre que el mouse mantiene el mouse sobre la aplicación. Los desarrolladores de aplicaciones de escritorio deben Windows 8.1 para comprobar que no capturan eventos de rueda del mouse (según las instrucciones anteriores).

 

 




