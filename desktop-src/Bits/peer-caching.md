---
title: Almacenamiento en caché del mismo nivel
description: A partir de Servicio de transferencia inteligente en segundo plano (BITS) 4,0, el servicio BITS se amplió para permitir el almacenamiento en caché del mismo nivel de subred para los datos de URL descargados mediante Windows BranchCache.
ms.assetid: 4197eed3-1812-4440-99e7-9462635ef6ad
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 3c87e6013bb37610e934c13414bd2636407108ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656367"
---
# <a name="peer-caching"></a>Almacenamiento en caché del mismo nivel

A partir de Servicio de transferencia inteligente en segundo plano (BITS) 4,0, el servicio BITS se amplió para permitir el almacenamiento en caché del mismo nivel de subred para los datos de URL descargados mediante Windows BranchCache. Los clientes de BITS pueden recuperar datos de otros equipos en su propia subred que ya han descargado los datos, en lugar de recuperar los datos de los servidores remotos. Para obtener más información acerca de Windows BranchCache, consulte la [información general de BranchCache](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).

Si un administrador habilita Windows BranchCache en equipos cliente y servidor de una organización a través de una directiva de grupo o una configuración local, BITS usará Windows BranchCache para las transferencias de datos.

-   [Configuración para el almacenamiento en caché del mismo nivel en BITS 4,0](#configuration-for-bits-40-peer-caching)
-   [Deshabilitar Windows BranchCache](#disabling-windows-branchcache)
-   [Comprobación y supervisión](#verification-and-monitoring)
-   [Almacenamiento en caché del mismo nivel en BITS 3,0](#peer-caching-in-bits-30)

## <a name="configuration-for-bits-40-peer-caching"></a>Configuración para el almacenamiento en caché del mismo nivel en BITS 4,0

La configuración siguiente es necesaria para que el almacenamiento en caché del mismo nivel en BITS 4,0 funcione:

-   Windows BranchCache debe estar habilitado en el cliente mediante una directiva de grupo o una configuración local. Para obtener más información, vea [BranchCache Client Configuration](/previous-versions/windows/it-pro/windows-7/dd637820(v=ws.10)).
    > [!Note]  
    > La característica Windows BranchCache está deshabilitada de forma predeterminada.

     

-   La característica Windows BranchCache es un componente opcional que se debe instalar en el servidor. Para obtener más información, vea [BranchCache Server Configuration](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).
-   El servidor también debe habilitar la característica Windows BranchCache a través de la Directiva de grupo o la configuración local. Para obtener más información, vea [BranchCache Server Configuration](/previous-versions/windows/it-pro/windows-7/dd637785(v=ws.10)).
    > [!Note]  
    > La característica Windows BranchCache está deshabilitada de forma predeterminada.

     

La Directiva de grupo BITS predeterminada permite el almacenamiento en caché del mismo nivel. Si Windows BranchCache está habilitado globalmente en un equipo, esta característica también está habilitada para trabajos de transferencia de BITS. Para obtener más información acerca de las directivas de Grupo específicas de BITS, consulte [directivas de grupo](group-policies.md).

## <a name="disabling-windows-branchcache"></a>Deshabilitar Windows BranchCache

Un administrador puede usar una directiva de grupo para deshabilitar el uso de Windows BranchCache. (Consulte [directivas de grupo](group-policies.md)). Si Windows BranchCache está deshabilitado, los clientes de BITS solo recuperarán datos de servidores remotos.

Una aplicación también puede deshabilitar Windows BranchCache en función de cada trabajo llamando al método [**IBackgroundCopyJob4:: SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) y estableciendo la marca **BG \_ Disable \_ Branch \_ Cache** .

> [!Note]  
> Esta configuración no afecta al uso de Windows BranchCache por parte de aplicaciones que no sean BITS. Esta configuración no se aplica a las transferencias de BITS a través de SMB. BITS no controla ningún valor para las transferencias de Windows BranchCache a través de SMB.

 

## <a name="verification-and-monitoring"></a>Comprobación y supervisión

Hay varias maneras de comprobar y supervisar las estadísticas de almacenamiento en caché del mismo nivel. Los administradores pueden llamar al método [**IBackgroundCopyFile4:: GetPeerDownloadStats**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibackgroundcopyfile4-getpeerdownloadstats) para consultar la cantidad de datos que se descargaron de los equipos del mismo nivel y de los servidores de origen. Los administradores también pueden buscar el ID. de [evento 60](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc734635(v=ws.10))en el registro de eventos, que proporciona información específica del trabajo.

La característica Windows BranchCache también proporciona una serie de mecanismos para comprobar y supervisar las estadísticas de almacenamiento en caché del mismo nivel. Para obtener más información, consulte [comprobación y supervisión](/previous-versions/windows/it-pro/windows-7/dd637782(v=ws.10)) y [contadores de rendimiento](/previous-versions/windows/it-pro/windows-7/dd637826(v=ws.10)).

El modelo de almacenamiento en caché del mismo nivel que usa Windows BranchCache reemplaza el modelo de almacenamiento en caché del mismo nivel usado en BITS 3,0. Para obtener más información acerca de Windows BranchCache, consulte lo siguiente:

-   [BranchCache](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj127252(v=ws.11))
-   [Información general sobre BranchCache](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))
-   [Servicios de Windows 7](../win7devguide/services.md)
-   [API de distribución del mismo nivel](../p2psdk/peer-distribution.md)

## <a name="peer-caching-in-bits-30"></a>Almacenamiento en caché del mismo nivel en BITS 3,0

> [!Note]  
> A partir de Windows 7, el modelo de almacenamiento en caché del mismo nivel de BITS 3,0 está en desuso. Si BITS 4,0 está instalado, el modelo de almacenamiento en caché del mismo nivel de BITS 3,0 no está disponible.

 

Si el administrador habilita el almacenamiento en caché del mismo nivel y el trabajo permite descargar contenido de un elemento del mismo nivel, BITS intentará descargar el contenido de uno o más elementos del mismo nivel. La descarga de un elemento del mismo nivel es mucho más rápida que la descarga de contenido desde Internet. El almacenamiento en caché del mismo nivel está deshabilitado de forma predeterminada y los trabajos deben permitir explícitamente la descarga de contenido del mismo nivel. Un administrador puede usar una directiva de grupo para habilitar el almacenamiento en caché del mismo nivel. Después de habilitar el almacenamiento en caché del mismo nivel, el administrador puede deshabilitar la descarga de un elemento del mismo nivel o el servicio en un elemento del mismo nivel.

Una aplicación también puede habilitar el almacenamiento en caché del mismo nivel llamando al método [**IBitsPeerCacheAdministration:: SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) . Sin embargo, esta configuración se reemplaza por la configuración de la Directiva de grupo, si se establece.

Cuando está habilitado el almacenamiento en caché del mismo nivel, BITS crea una lista de elementos del mismo nivel que se encuentran en la misma subred y pertenecen al mismo dominio. La lista no incluirá elementos del mismo nivel de un dominio de confianza. El almacenamiento en caché del mismo nivel solo se puede habilitar en un entorno de dominio.

BITS detecta los elementos del mismo nivel haciendo lo siguiente:

-   Escuchando servidores del mismo nivel que se anuncian a sí mismos. Un servidor del mismo nivel se anunciará cuando se inicie. BITS agregará el servidor del mismo nivel a la lista si el cliente necesita más elementos del mismo nivel en su lista.
-   Difundir una solicitud para los servidores del mismo nivel cuando necesita más elementos del mismo nivel en su lista de elementos del mismo nivel. Los servidores del mismo nivel que están disponibles para servir el contenido responden a la solicitud.

BITS quita los servidores del mismo nivel de la lista del mismo nivel si el servidor hace lo siguiente:

-   Error de autenticación
-   Está sin conexión (no disponible) durante demasiado tiempo
-   Proporciona un certificado con errores

Cuando un trabajo solicita contenido de un elemento del mismo nivel, BITS elige aleatoriamente un subconjunto de elementos del mismo nivel de la lista del mismo nivel y les pregunta si tienen el contenido. BITS solo puede descargar contenido de servidores del mismo nivel autenticados. El cliente y el servidor se autentican inicialmente entre sí mediante Kerberos y, a continuación, intercambian certificados autofirmados para la autenticación durante la detección y descarga de contenido.

BITS descarga el contenido del primer elemento del mismo nivel autenticado para responder a la solicitud. Si un elemento del mismo nivel no contiene todo el contenido, BITS descargará lo que puede hacer de uno o más de los elementos del mismo nivel antes de descargar el resto desde el servidor de origen. Si ninguno de los elementos del mismo nivel tiene el contenido o se produce un error durante la descarga de un elemento del mismo nivel, BITS descarga el contenido del servidor de origen.

El contenido descargado está disponible para atender a otros equipos del mismo nivel después de que la aplicación valide el contenido de los archivos. Si la aplicación no valida explícitamente el archivo, el archivo se valida implícitamente cuando la aplicación completa el trabajo.

De forma predeterminada, un servidor del mismo nivel puede servir contenido para solo tres clientes simultáneamente. Si el servidor está actualmente ocupado atendiendo a tres clientes, habrá un retraso en la respuesta a otras solicitudes. BITS limita el ancho de banda utilizado para servir contenido a 1 Mbps. Puede usar la Directiva de grupo [MaxBandwidthServed](group-policies.md) para cambiar el límite.

> [!Note]  
> Esta característica solo se admite en redes de dominio; no se admite el almacenamiento en caché del mismo nivel en grupos de trabajo o redes domésticas.

Consulte también [Administración de la caché del mismo nivel](/windows/desktop/Bits/administering-the-peer-cache)
 

 

 