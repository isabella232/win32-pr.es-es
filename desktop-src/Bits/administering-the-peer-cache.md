---
title: Administrar la caché del mismo nivel
description: Nota a partir de Windows 7, el modelo de almacenamiento en caché del mismo nivel de Servicio de transferencia inteligente en segundo plano (BITS) 3,0 está en desuso.
ms.assetid: a33a43e5-02f9-4902-ad3a-ec65b0d80520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b3ea1dd19c9aca855ffd73e174dcb3b588a54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773909"
---
# <a name="administering-the-peer-cache"></a>Administrar la caché del mismo nivel

> [!Note]  
> A partir de Windows 7, el modelo de almacenamiento en caché del mismo nivel de Servicio de transferencia inteligente en segundo plano (BITS) 3,0 está en desuso. Si BITS 4,0 está instalado, el modelo de almacenamiento en caché del mismo nivel de BITS 3,0 no está disponible.

 

Para mejorar el rendimiento de la descarga, BITS permite descargar contenido de equipos del mismo nivel. Para habilitar esta característica, el administrador debe habilitar la configuración de directiva de grupo de EnablePeerCaching. Si está habilitada, el elemento del mismo nivel puede descargar el contenido de los elementos del mismo nivel y servir contenido a los elementos del mismo nivel. El administrador también puede usar la configuración de la Directiva DisablePeerCachingClient y DisablePeerCachingServer para evitar la descarga de contenido de un elemento del mismo nivel o el contenido del mismo a los equipos del mismo nivel, respectivamente.

Si no se configuran las opciones de directiva de grupo, una aplicación puede llamar al método [**IBitsPeerCacheAdministration:: SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) para establecer la preferencia de almacenamiento en caché del mismo nivel para el equipo. Tenga en cuenta que estas preferencias se invalidan mediante la configuración de directiva de grupo si se establecen posteriormente. Para determinar si el equipo habilita el almacenamiento en caché del mismo nivel, llame al método [**IBitsPeerCacheAdministration:: GetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-getconfigurationflags) .

Si el almacenamiento en caché del mismo nivel está habilitado, BITS solo almacenará en caché el contenido de un trabajo si el trabajo permite que el contenido se almacene en caché. BITS también descargará el contenido de un elemento del mismo nivel si el trabajo lo permite explícitamente. Para habilitar el almacenamiento en caché del mismo nivel para un trabajo, llame al método [**IBackgroundCopyJob4:: SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) .

Además de usar directiva de grupo o la interfaz [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) para habilitar el almacenamiento en caché del mismo nivel, también puede usar cualquiera de los métodos para cambiar el tamaño de caché predeterminado y la cantidad de tiempo que un archivo sin acceso permanece en la memoria caché. Para cambiar los valores predeterminados mediante la interfaz **IBitsPeerCacheAdministration** , llame a los métodos [**SetMaximumCacheSize**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcachesize) y [**SetMaximumContentAge**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcontentage) . Dado que estos métodos establecen la configuración de preferencias, se invalidan mediante la configuración de directiva de grupo.

Para enumerar los elementos del mismo nivel de los que BITS intentará descargar contenido, llame al método [**IBitsPeerCacheAdministration:: EnumPeers**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumpeers) .

Para enumerar los archivos de la memoria caché que los BITS atenderán a los elementos del mismo nivel, llame al método [**IBitsPeerCacheAdministration:: EnumRecords**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords) .

Nunca debe tener que administrar la caché del mismo nivel con respecto a la detección de elementos del mismo nivel o la eliminación de registros de caché. Esta funcionalidad se incluyó en la interfaz [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) para la integridad.

 

 




