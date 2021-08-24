---
title: Problemas comunes de incorporación para las tiendas de Música en línea
description: Problemas comunes de incorporación para las tiendas de Música en línea
ms.assetid: 4210aabb-d1ad-4f98-88e0-941933d77303
keywords:
- Reproductor de Windows Media Tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c4cb38f088f463d6bea8ca15b3a92cea9610cc8541f27d55c48df07f9286d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763965"
---
# <a name="common-on-boarding-problems-for-online-music-stores"></a>Problemas comunes de incorporación para las tiendas de Música en línea

A continuación se muestra una lista de Reproductor de Windows Media problemas de incorporación que debe intentar evitar. Cualquiera de estos problemas puede hacer que el almacén no pueda realizar pruebas de validación. Si se genera un error en el paso RC2, se pospondrá el inicio hasta la siguiente ventana de inicio disponible.

1.  Error al realizar la transición de servidores de prueba a servidores de producción
    -   Páginas que faltan
    -   Configuración de IIS (Access, VRoots, https u otra configuración de seguridad)
    -   Las cuentas de prueba ya no funcionan.
    -   Las cuentas de prueba no tienen créditos aplicados.
    -   Los logotipos hospedados en el servicio no se mueven.
    -   Las restricciones de IP que se han trabajado previamente para que se vuelvan a producir. En concreto, los sistemas de comercio electrónico pueden tener un conjunto diferente de restricciones del sitio de música.
    -   El documento ServiceInfo no se actualiza para que apunte a producción.
2.  El vínculo Comprar (o Vínculo a la tienda) del área Reproducción ahora no es válido. Se trata de un problema que se pasa por alto normalmente y hará que la tienda no funcione aunque todo lo demás esté en funcionamiento.
3.  Los evaluadores de Microsoft deben tener el poder adquisitivo adecuado. El equipo de validación de Microsoft ejecutará varios escenarios de compra que van desde compras pequeñas hasta compras muy grandes. Debe proporcionar una manera fácil de actuar como consumidores dentro de su tienda. Esto puede abarcar desde proporcionar una variedad de cuentas hasta proporcionar una tarjeta de crédito ficticia. Por ejemplo, una tienda producirá un error en RC2 si un evaluador de validación intenta comprar un álbum, pero solo tiene crédito suficiente para comprar una sola pista.
4.  Si usa controles ActiveX dentro de las páginas de servicio, asegúrese de que se instalan y desinstalan correctamente, tanto en todas las versiones aplicables de Windows. No hacerlo es un problema típico. A menudo, los desarrolladores y evaluadores de una tienda en línea tienen los controles ActiveX registrados en sus propios equipos, pero olvidan instalar los controles en el equipo del usuario.

    Si la tienda instala un complemento o un control ActiveX, debe proporcionar al usuario una manera fácil de desinstalarlo. Por ejemplo, Microsoft ha descubierto recientemente que algunas tiendas en línea instalaron controles ActiveX en Reproductor de Windows Media 11 para Windows Vista que no se pudieron quitar mediante el menú Agregar o quitar programas. Después de una investigación, Microsoft ha descubierto que los ActiveX se pueden quitar a través del administrador de complementos de Internet Explorer. Es importante que comunique (al menos a través de un archivo de Ayuda) la manera de instalar y desinstalar ActiveX controles y complementos.

    Para obtener más información sobre cómo integrar su tienda con la infraestructura de seguridad en Windows Vista, consulte el artículo titulado "Procedimientos recomendados para desarrolladores e instrucciones para aplicaciones en un entorno con privilegios [mínimos".](/previous-versions/aa905330(v=msdn.10))

 

 