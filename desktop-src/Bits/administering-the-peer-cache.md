---
title: Administración de la caché del mismo nivel
description: Nota A partir de Windows 7, el modelo Servicio de transferencia inteligente en segundo plano almacenamiento en caché del mismo nivel (BITS) 3.0 está en desuso.
ms.assetid: a33a43e5-02f9-4902-ad3a-ec65b0d80520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3821cc0894754b8dbc2ee9f9a189381ac69030d39938c8f6cb4bc52625ef03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588755"
---
# <a name="administering-the-peer-cache"></a>Administración de la caché del mismo nivel

> [!Note]  
> A partir Windows 7, el modelo de almacenamiento en caché del mismo nivel Servicio de transferencia inteligente en segundo plano (BITS) 3.0 está en desuso. Si bits 4.0 está instalado, el modelo de almacenamiento en caché del mismo nivel de BITS 3.0 no está disponible.

 

Para mejorar el rendimiento de la descarga, BITS le permite descargar contenido de equipos del mismo nivel. Para habilitar esta característica, el administrador debe habilitar la configuración de directiva de grupo EnablePeerCaching. Si está habilitada, el elemento del mismo nivel puede descargar contenido de los pares y servir contenido a los pares. El administrador también puede usar las opciones de directiva DisablePeerCachingClient y DisablePeerCachingServer para evitar la descarga de contenido de un elemento del mismo nivel o el contenido de servicio a los pares, respectivamente.

Si la configuración de directiva de grupo no está configurada, una aplicación puede llamar al método [**IBitsPeerCacheAdministration::SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) para establecer la preferencia de almacenamiento en caché del mismo nivel para el equipo. Tenga en cuenta que estas preferencias se reemplazan por la configuración de directiva de grupo si se establecen más adelante. Para determinar si el equipo habilita el almacenamiento en caché del mismo nivel, llame al método [**IBitsPeerCacheAdministration::GetConfigurationFlags.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-getconfigurationflags)

Si el almacenamiento en caché del mismo nivel está habilitado, BITS solo almacenará en caché el contenido de un trabajo si el trabajo permite explícitamente que su contenido se almacene en caché. BITS también solo descargará contenido de un elemento del mismo nivel si el trabajo lo permite explícitamente. Para habilitar el almacenamiento en caché del mismo nivel para un trabajo, llame al [**método IBackgroundCopyJob4::SetPeerCachingFlags.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags)

Además de usar directiva de grupo o la interfaz [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) para habilitar el almacenamiento en caché del mismo nivel, también puede usar cualquiera de los métodos para cambiar el tamaño de caché predeterminado y el período de tiempo que un archivo sin acceso permanece en la memoria caché. Para cambiar los valores predeterminados mediante la interfaz **IBitsPeerCacheAdministration,** llame a los métodos [**SetMaximumCacheSize**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcachesize) y [**SetMaximumContentAge.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcontentage) Puesto que estos métodos establecen la configuración de preferencias, se reemplazan por la configuración de la directiva de grupo.

Para enumerar los elementos del mismo nivel de los que BITS intentará descargar contenido, llame al método [**IBitsPeerCacheAdministration::EnumPeers.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumpeers)

Para enumerar los archivos de la memoria caché que BITS va a servir a los elementos del mismo nivel, llame al método [**IBitsPeerCacheAdministration::EnumRecords.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords)

Nunca debe tener que administrar la caché del mismo nivel con respecto a la de descubrimiento de elementos del mismo nivel o la eliminación de registros de caché. Esta funcionalidad se incluyó en [**la interfaz IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) para mejorar la integridad.

 

 




