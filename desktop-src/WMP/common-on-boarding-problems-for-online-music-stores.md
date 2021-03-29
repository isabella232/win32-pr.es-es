---
title: Problemas comunes de incorporación para tiendas de música en línea
description: Problemas comunes de incorporación para tiendas de música en línea
ms.assetid: 4210aabb-d1ad-4f98-88e0-941933d77303
keywords:
- Windows Media Player tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f600d1035e0fd20be7786af4d4ffed4482138a72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793191"
---
# <a name="common-on-boarding-problems-for-online-music-stores"></a>Problemas comunes de incorporación para tiendas de música en línea

Esta es una lista de problemas comunes de Windows Media Player en la incorporación que debe intentar evitar. Cualquiera de estos problemas puede hacer que el almacén no supere las pruebas de validación. Si se produce un error en la fase RC2, se pospondrá el lanzamiento hasta la siguiente ventana de inicio disponible.

1.  No se pudo realizar la transición de los servidores de prueba a los servidores de producción
    -   Faltan páginas
    -   Configuración de IIS (Access, VRoots, https u otra configuración de seguridad)
    -   Las cuentas de prueba ya no funcionan.
    -   Las cuentas de prueba no tienen créditos aplicados.
    -   Los logotipos hospedados de servicio no se mueven.
    -   Restricciones de IP que se han solucionado con anterioridad. En concreto, los sistemas de comercio electrónico pueden tener un conjunto diferente de restricciones del sitio de música.
    -   El documento ServiceInfo no se actualiza para que apunte a producción.
2.  El vínculo comprar (o el vínculo de la tienda) del área reproducción en curso no es válido. Se trata de un problema que se suele pasar por alto y hará que se produzca un error en la tienda incluso cuando todo lo demás esté en orden de trabajo.
3.  Los evaluadores de Microsoft deben tener la capacidad de compra adecuada. El equipo de validación de Microsoft se ejecutará a través de varios escenarios de compra que van desde pequeñas compras hasta compras de gran tamaño. Debe proporcionar una manera recargable para que actúen como consumidores dentro de la tienda. Esto puede abarcar desde proporcionar una serie de cuentas a través de una tarjeta de crédito ficticia. Por ejemplo, un almacén producirá un error en RC2 si un evaluador de validación intenta comprar un álbum pero solo tiene un crédito suficiente para comprar una sola pista.
4.  Si usa controles ActiveX dentro de las páginas de servicio, asegúrese de que se instalan y desinstalan sin problemas en todas las versiones aplicables de Windows. Si no lo hace, es un problema típico. A menudo, los desarrolladores y evaluadores de una tienda en línea tienen los controles ActiveX registrados en sus propios equipos, pero se olvidan de instalar los controles en el equipo del usuario.

    Si el almacén instala un complemento o un control ActiveX, debe proporcionar al usuario una manera fácil de desinstalarlo. Por ejemplo, Microsoft ha descubierto recientemente que algunas tiendas en línea instalaron controles ActiveX en Windows Media Player 11 para Windows Vista que no se pudieron quitar a través del menú Agregar o quitar programas. Después de alguna investigación, Microsoft ha detectado que los controles ActiveX se pueden quitar a través del administrador de complementos en Internet Explorer. Es importante que se comunique (a través de un archivo de ayuda, al menos) la manera de instalar y desinstalar controles y complementos de ActiveX.

    Para obtener más información acerca de cómo integrar su almacén con la infraestructura de seguridad de Windows Vista, consulte el artículo titulado ["prácticas recomendadas para desarrolladores e instrucciones para aplicaciones en un entorno con menos privilegios"](/previous-versions/aa905330(v=msdn.10)).

 

 