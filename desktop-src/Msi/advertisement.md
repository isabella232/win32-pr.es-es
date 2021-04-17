---
description: El Windows Installer puede anunciar la disponibilidad de una aplicación a los usuarios u otras aplicaciones sin instalar realmente la aplicación.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Anuncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bb31f14fb4cd6f589e94939afdd5575df52c43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652621"
---
# <a name="advertisement"></a>Anuncio

El Windows Installer puede anunciar la disponibilidad de una aplicación a los usuarios u otras aplicaciones sin instalar realmente la aplicación. Si se anuncia una aplicación, solo se presentan al usuario u otras aplicaciones las interfaces requeridas para cargar e iniciar la aplicación. Si un usuario o una aplicación activa una interfaz anunciada, el instalador continúa con la instalación de los componentes necesarios, como se describe en [instalación a petición](installation-on-demand.md).

Los dos tipos de publicidad son la asignación y publicación. Una aplicación aparece instalada para un usuario cuando esa aplicación se asigna al usuario. El menú **Inicio** contiene los métodos abreviados adecuados, se muestran iconos, los archivos se asocian a la aplicación y las entradas del registro reflejan la instalación de la aplicación. Cuando el usuario intenta abrir una aplicación asignada, se instala a petición.

El instalador admite el anuncio de las aplicaciones y características según el sistema operativo. El instalador registra la información de la clase COM para las aplicaciones asignadas a partir de Windows XP. Esto permite al instalador instalar la aplicación al crear una instancia de una clase anunciada. Para obtener más información, vea [compatibilidad de la plataforma con el anuncio](platform-support-of-advertisement.md).

Puede publicar una aplicación desde el servidor a partir de Windows Server 2003. La aplicación publicada se instala a través de la Asociación de archivos o el tipo de extensión multipropósito de correo Internet (MIME). La publicación no rellena la interfaz de usuario con ninguno de los iconos de la aplicación. El sistema operativo cliente puede instalar una aplicación publicada a partir de Windows XP.

 

 



